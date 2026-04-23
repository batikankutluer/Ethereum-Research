# ERC-20

**Yıl:** 2015 (oluşturuldu) / 2017 (nihai hale geldi)
**Durum:** Final
**Kategori:** Fungible Token Standardı

## Özet
ERC-20, Ethereum üzerinde fungible token üretmek için ortak bir arayüz tanımlar. `transfer`, `transferFrom`, `approve`, `allowance` ve `balanceOf` gibi fonksiyonlarla wallet, borsa, protokol ve dapp'lerin aynı token yüzeyiyle konuşmasını mümkün kılar.

## Neden Önemli
Ethereum'da token ekonomisinin gerçek başlangıç noktası budur. ERC-20 olmadan her proje kendi özel arayüzünü kullanmak zorunda kalırdı; bu da wallet entegrasyonu, borsa listeleme, likidite havuzları ve DeFi birleştirilebilirliğini ciddi biçimde zorlaştırırdı.

## Temel Bileşenler
- `transfer` / `transferFrom` — token taşıma akışı
- `approve` / `allowance` — üçüncü taraf harcama yetkisi
- `Transfer` / `Approval` event'leri — cüzdanlar ve indeksleyiciler için ortak gözlem yüzeyi
- `name`, `symbol`, `decimals` — zorunlu olmayan ama pratikte yaygın metadata alanları

## Tarihsel Bağlam
ERC-20'nin kökü 2015'te açılan `Issue #20` tartışmasına gider. Standardın asıl etkisi, 2017'de EIP reposunda nihai hale gelmesiyle birlikte farklı token uygulamalarının ortak bir minimum davranış kümesinde buluşması oldu.

Bu standart, Ethereum'un yalnızca akıllı kontrat platformu değil, aynı zamanda zincir üstü varlık çıkarma ve taşımaya uygun bir uygulama katmanı olduğunu pratikte kanıtladı. Sonraki NFT ve multi-token standartları da büyük ölçüde ERC-20'nin yarattığı bu ortak arayüz fikrinin üstüne inşa edildi.

## Sınırlamalar
- Tüm token'lar aynı değildir; kilitli, vergili veya rebase yapan token'lar ERC-20 yüzeyine sığsa da davranışları farklı olabilir.
- `approve` / `allowance` modeli UX ve güvenlik açısından sürtünme yaratır; bu yüzden daha sonra [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]] geliştirildi.
- Standart temel taşınabilirliği çözer, ama metadata, izin ergonomisi ve güvenli transfer alıcısı kontrolü gibi alanları ayrı standardlara bırakır.

## Bağlantılı EIP'ler
- [[ERC-777]] — daha zengin hook ve operator modeli sunan fungible alternatif
- [[ERC-1363]] — callback tabanlı ödeme uzantısı
- [[ERC-4626]] — ERC-20 tabanlı vault share standardı
- [[ERC-4524]] — safe transfer odaklı güvenli alıcı uzantısı
- [[ERC-6093]] — standard custom errors
- [[ERC-6864]] — kullanıcı onaylı upgrade / downgrade hattı
- [[ERC-7674]] — geçici approval uzantısı
- [[ERC-7699]] — ödeme referansı ekleyen transfer uzantısı
- [[ERC-7802]] — crosschain mint/burn arayüzü
- [[ERC-8056]] — UI amount scaling uzantısı
- [[ERC-721]] — fungible olmayan varlıklar için ayrışan standart
- [[ERC-1155]] — tek kontratta çoklu token tipi yaklaşımı
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]] — ERC-20 için `permit` uzantısı
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]] — token görünürlüğünü wallet tarafında iyileştiren akış

## İlgili Terimler
- [[Sözlük#Fungible Token|Fungible Token]]
- [[Sözlük#Allowance|Allowance]]
- [[Sözlük#Permit|Permit]]

## Teknik Notlar
ERC-20'nin gücü, çok küçük bir ortak paydaya dayanmasındadır. Bu sadelik sayesinde wallet, DEX, lending protokolü veya köprü gibi farklı sistemler token kontratını detaylıca tanımadan temel işlemleri yapabilir.

Aynı sadelik bazı tasarım boşlukları da bırakır. Özellikle `approve` akışının iki adımlı olması, allowance yarış durumları ve özel davranışlı token implementasyonları; sonraki yıllarda hem wallet UX standardı hem de token uzantıları için ayrı bir araştırma hattı doğurdu.

## ERC-20'ye Gelen Başlıca Uzantılar

ERC-20 sonrası çizgi, tek bir “yeni token standardı” ile değil, farklı sorunlara cevap veren birkaç ayrı halka ile büyüdü:

### 1. Erken Tasarım Tepkileri
- [[ERC-223]] — plain `transfer` ile kontratlara token gönderirken oluşan kayıp riskine erken tepki
- [[ERC-777]] — hook ve operator modeliyle daha zengin bir fungible token yüzeyi önerir

### 2. İmza ve Yetkilendirme Katmanı
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-712|EIP-712]] — typed structured data imzalama; sonraki imzalı token akışlarının temel altyapısı
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]] — allowance tabanlı `permit` uzantısı
- [[ERC-3009]] — allowance yerine imzalı transfer / authorization yaklaşımı

### 3. Ödeme ve Protokol Entegrasyonu
- [[ERC-1363]] — `transferAndCall` ve `approveAndCall` ile callback tabanlı ödeme akışı
- [[ERC-4626]] — ERC-20 tabanlı vault share modeli; modern DeFi'de fungible token semantiğini genişletir
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]] — token'ın wallet içinde görünür ve izlenebilir hale gelmesi

### 4. 2021 Sonrası Operasyonel Uzantılar
- [[ERC-4524]] — ERC-20 için safe transfer ve receiver doğrulama hattı
- [[ERC-6093]] — token hata yüzeyini standardize eden custom errors
- [[ERC-6864]] — kullanıcı onaylı upgrade / downgrade modeli
- [[ERC-7674]] — tek transaction'lık temporary approval
- [[ERC-7699]] — transferlere invoice / sipariş referansı ekleyen uzantı
- [[ERC-7802]] — token-bridge mint/burn arayüzünü standardize eden crosschain hat
- [[ERC-8056]] — UI miktarını ölçekleyen, raw amount'ı bozmayan kurumsal uzantı

## Hangi Notlar En Yüksek Değerde?

ERC-20 hattını büyütürken ilk bakılması gereken üç yeni standart:

- [[ERC-777]] — neden ekosistemin yalın ERC-20 tabanında kaldığını anlamak için
- [[ERC-1363]] — token ödemesi ile kontrat callback'ini tek akışta birleştirdiği için
- [[ERC-4626]] — ERC-20'nin DeFi çağındaki en güçlü genişleme noktası olduğu için

İkinci dalga / bağlamsal derinlik olarak [[ERC-223]], [[ERC-3009]] ve [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-712|EIP-712]] izlenebilir.

## Kaynaklar
- Resmi spesifikasyon: [ERC-20](https://eips.ethereum.org/EIPS/eip-20)
- Orijinal tartışma: [ethereum/EIPs Issue #20](https://github.com/ethereum/EIPs/issues/20)
- Nihai hale taşıyan PR: [ethereum/EIPs PR #610](https://github.com/ethereum/EIPs/pull/610)
- Referans uygulama ailesi: [OpenZeppelin ERC20](https://docs.openzeppelin.com/contracts/api/token/erc20)
