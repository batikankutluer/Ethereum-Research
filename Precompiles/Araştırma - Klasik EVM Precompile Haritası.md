# Araştırma - Klasik EVM Precompile Haritası

## Soru

Ethereum'daki klasik ön derleme seti nasıl oluştu ve bugünkü modern precompile EIP'lerinin zemini nedir?

## Kısa Cevap

Ön derlemeler, belirli hesaplamaları opcode seviyesine çıkarmadan, sabit adreslerde çalışan yerleşik sözleşmeler gibi sunar. Ethereum'un ilk seti `ecrecover`, `sha256`, `ripemd160` ve `identity` ile başladı; Byzantium döneminde `alt_bn128` ve `modexp` geldi; Istanbul ve Berlin'de bu hattın hash ve gaz fiyatlaması düzeltildi. Bugünkü [[EIP-4844]], [[EIP-2537]] ve [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]] gibi modern örnekler bu temelin üstüne inşa ediliyor.

## Neden Önemli

Bir geliştirici için precompile'ları yalnızca adres listesi olarak bilmek yetmez. Hangi precompile'ın neden eklendiğini, hangilerinin yeni primitive eklediğini, hangilerinin sadece fiyatlama düzelttiğini ve hangilerinin execution layer'a yeni kullanım alanları açtığını anlamak gerekir. Bu tarihçe olmadan `EIP-4844` veya `EIP-2537` gibi modern notlar parçalı görünür.

## Bağlantılı Notlar

- [[Precompiles EIPs]]
- [[EIP-2537]]
- [[EIP-4844]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]]
- [[Karşılaştırma - P256 kontrat doğrulama vs EIP-7212]]

## Teknik Notlar

### Precompile ile Opcode Arasındaki Fark

[[Sözlük#Precompile / Ön Derleme|Ön Derleme]], EVM içine gömülü ama sabit bir adreste çağrılan yerleşik işlemdir; [[Sözlük#Opcode / İşlem Kodu|opcode]] ise doğrudan VM komutu olarak çalışır. Bu ayrım, pahalı kriptografi veya hashing fonksiyonlarını yeni opcode ailesi tasarlamadan execution layer'a eklemeyi mümkün kılar.

### Başlangıç Seti

Ethereum'un en eski precompile seti `0x01-0x04` aralığında yer alır:

- `0x01` — `ecrecover`
- `0x02` — `sha256`
- `0x03` — `ripemd160`
- `0x04` — `identity`

Bu setin ortak amacı, sık kullanılan ama EVM içinde pahalı kalan doğrulama ve hashing işlemlerini temel seviyede ucuzlatmaktır.

### Byzantium Dalgası

Byzantium, precompile tarihinin ilk büyük genişleme anıdır:

- `EIP-198` ile `0x05` adresinde `modexp`
- `EIP-196` ile `0x06` ve `0x07` adreslerinde `alt_bn128` toplama ve skaler çarpma
- `EIP-197` ile `0x08` adresinde `alt_bn128` pairing check

Bu dönem, özellikle zkSNARK doğrulamasını blok gaz sınırı içinde pratik hale getirmeye çalışır. Yani yeni kullanım alanı sadece “daha hızlı kripto” değil; gizlilik ve ölçeklenebilirlik için zincir üstü kanıt doğrulamasını mümkün kılmaktır.

### Istanbul ve Berlin Düzeltmeleri

İkinci aşama yeni primitive eklemekten çok mevcut precompile hattını daha kullanılabilir hale getirir:

- `EIP-152` — `0x09` adresinde `BLAKE2 F` compression function eklenir
- `EIP-1108` — `alt_bn128` precompile'larının gaz maliyetleri düşürülür
- `EIP-2565` — `modexp` fiyatlaması yeniden tanımlanır

Bu grup, precompile tarihçesinde önemli bir ayrım gösterir: bazı EIP'ler yeni adres açar, bazıları ise mevcut precompile'ların ekonomik olarak gerçekten kullanılabilir hale gelmesini sağlar.

### Modern Dalga

Modern precompile dönemi iki ayrı çizgide ilerler:

1. yeni kriptografik aileler:
   - [[EIP-2537]] — BLS12-381 precompile ailesi
   - [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]] — P256 / secp256r1 doğrulaması
2. daha geniş protokol hedefleri:
   - [[EIP-4844]] — blob transaction modeliyle birlikte `0x0A` point evaluation precompile

Bu aşamada ön derlemeler artık sadece “hash ve imza yardımcıları” değil; DA, blob, passkey, BLS ve yeni execution-layer kriptografisinin omurgası haline gelir.

### Geliştirici İçin Okuma Mantığı

Precompile alanını verimli anlamak için sıra şu şekilde okunabilir:

1. `0x01-0x04` temel seti
2. Byzantium trio'su: `EIP-198`, `EIP-196`, `EIP-197`
3. repricing / iyileştirme hattı: `EIP-152`, `EIP-1108`, `EIP-2565`
4. modern genişleme: [[EIP-4844]], [[EIP-2537]], [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]]

## Açık Sorular

- Ethereum L1 bundan sonra yeni precompile eklemeye mi yoksa daha dar uzmanlaşmış primitive'leri farklı katmanlara bırakmaya mı daha yakın?
- L2'ler ve farklı EVM zincirleri kendi precompile setleriyle ne kadar ayrışacak?
- `EIP-7212` gibi zincir bazlı benimsenen öneriler ne zaman ortak L1 standardına dönüşür?

## Kaynaklar

- Resmi spesifikasyon: [EIP-196](https://eips.ethereum.org/EIPS/eip-196)
- Resmi spesifikasyon: [EIP-197](https://eips.ethereum.org/EIPS/eip-197)
- Resmi spesifikasyon: [EIP-198](https://eips.ethereum.org/EIPS/eip-198)
- Resmi spesifikasyon: [EIP-152](https://eips.ethereum.org/EIPS/eip-152)
- Resmi spesifikasyon: [EIP-1108](https://eips.ethereum.org/EIPS/eip-1108)
- Resmi spesifikasyon: [EIP-2565](https://eips.ethereum.org/EIPS/eip-2565)
