# Karşılaştırma - P256 kontrat doğrulama vs EIP-7212

## Soru

P256 imza doğrulaması kontrat içinde yapılınca ne kazanılır, `EIP-7212` ile native precompile olarak sunulunca ne değişir?

## Kısa Cevap

Kontrat tabanlı P256 doğrulama bugün daha taşınabilir bir yoldur; hedef zincirde özel precompile beklemez ve uygulama seviyesinde hemen kullanılabilir. Buna karşılık gaz maliyeti daha yüksektir, doğrulama kodu daha karmaşıktır ve audit yüzeyi büyür.

`EIP-7212` ise P256 doğrulamasını yerleşik hale getirir. Bu, [[Sözlük#Passkey|passkey]] ve cihaz tabanlı kimlik doğrulama akışlarını çok daha pratik hale getirir. Bedeli ise zincir desteğine bağımlılık ve henüz tüm execution ortamlarında aynı derecede yaygın olmamasıdır.

## Neden Önemli

P256 konusu sadece bir kriptografi tercihi değildir; onboarding, wallet UX, akıllı hesap doğrulaması ve [[Sözlük#Verification Gas Limit|verification gas]] sınırlarıyla doğrudan ilişkilidir. Özellikle [[Account Abstraction/EIP, RIP & ERC/ERC-4337|ERC-4337]] ve [[Account Abstraction/EIP, RIP & ERC/ERC-7562|ERC-7562]] bağlamında, doğrulama maliyeti tasarım kararını doğrudan etkiler.

## Bağlantılı Notlar

- [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]]
- [[Account Abstraction/EIP, RIP & ERC/ERC-4337|ERC-4337]]
- [[Account Abstraction/EIP, RIP & ERC/ERC-7562|ERC-7562]]
- [[Precompiles EIPs]]
- [[Araştırma - Klasik EVM Precompile Haritası]]

## Teknik Notlar

### Zincir Desteği

- kontrat tabanlı yaklaşım: zincirden bağımsızdır; EVM uyumlu ortamda uygulanabilir
- `EIP-7212`: zincir desteği gerektirir; benimsenme arttıkça ürün tasarımını sadeleştirir

### Gaz ve Operasyonel Maliyet

- kontrat tabanlı doğrulama: daha pahalıdır; yoğun doğrulama akışlarında kullanıcı maliyetini ve bundler simülasyon yükünü artırır
- `EIP-7212`: aynı primitive'i native seviyeye alarak maliyeti belirgin biçimde düşürür

### Güvenlik ve Audit Yüzeyi

- kontrat tabanlı doğrulama: uygulama tarafında daha fazla kod ve daha geniş audit alanı demektir
- `EIP-7212`: mantığın execution layer'a taşınmasıyla uygulama kodunu sadeleştirir, ama zincir implementasyonuna güveni artırır

### Ürün ve UX Etkisi

- kontrat tabanlı yol: daha hızlı deney yapılmasını sağlar
- `EIP-7212`: passkey tabanlı wallet akışlarını daha düşük maliyetle ve daha öngörülebilir gas davranışıyla mümkün kılar

### AA Perspektifi

[[Account Abstraction/EIP, RIP & ERC/ERC-7562|ERC-7562]] açısından bakınca konu yalnızca işlem maliyeti değildir. Doğrulama aşamasında pahalı kriptografi kullanmak, bundler ve simülasyon katmanında daha sıkı sınır yönetimi gerektirir. Bu yüzden native P256 doğrulama, özellikle akıllı hesap ekosisteminde stratejik bir fark yaratır.

## Açık Sorular

- `EIP-7212` Ethereum L1'de ne kadar yaygın ve kalıcı biçimde benimsenecek?
- Wallet geliştiricileri zincir bazlı destek varken hibrit model mi kurmalı, yoksa tek bir doğrulama stratejisinde mi kalmalı?
- L2'ler P256 doğrulamasında L1'den daha hızlı mı ayrışacak?

## Kaynaklar

- Resmi spesifikasyon: [EIP-7212](https://github.com/ethereum/EIPs/pull/7212)
- Referans uygulama: [daimo-eth/p256-verifier](https://github.com/daimo-eth/p256-verifier)
- Bağlantılı standart: [ERC-7562](https://eips.ethereum.org/EIPS/eip-7562)
