# Sözlük

Ethereum araştırmalarındaki temel terimlerin, geliştirici gözüyle kısa ve net açıklamaları.
İlgili standartlara hızlı gitmek için mümkün olan yerlerde Obsidian bağlantıları eklendi.

## A

### Allowance
Bir hesabın, başka bir hesaba veya kontrata kendi token bakiyesinden ne kadar harcama yetkisi verdiğini gösteren değerdir. Özellikle [[Token/EIP, RIP & ERC/ERC-20|ERC-20]] içindeki `approve` / `allowance` modeliyle ilişkilidir.

### Access List / Erişim Listesi
Bir işlemin hangi adres ve storage alanlarına erişeceğini önceden beyan eden listedir. Özellikle [[EIP-2930]] ile standartlaşır ve gelişmiş işlem türleri için altyapı sağlar.

### Account Exposure / Hesap Erişimi
Bir dapp'in kullanıcı hesabını görebilmesi durumudur. Modern wallet UX'te bu erişim varsayılan değil, kullanıcı onayı sonrası verilir; bunun temel referansı [[EIP-1102]]'dir.

### AA (Account Abstraction / Hesap Soyutlaması)
Kullanıcı hesabının doğrulama, yetkilendirme, ücret ödeme ve işlem yürütme mantığını sabit EOA kurallarından çıkarıp programlanabilir hale getirme yaklaşımıdır. Pratikte bunun bugünkü en yaygın karşılığı [[ERC-4337]], EOA tarafındaki en önemli adımı ise [[EIP-7702]]'dir.

### Aggregator
Birden fazla imzayı veya doğrulama sonucunu daha verimli biçimde birleştiren yardımcı kontrattır. Özellikle [[ERC-4337]] akışında bazı hesap türlerinde doğrulama maliyetini azaltmak için kullanılır.

### Alt Mempool
Ethereum'un normal işlem havuzundan ayrı çalışan, `UserOperation` nesnelerinin yayıldığı ağ katmanıdır. [[ERC-4337]]'nin temel parçalarından biridir.

### Authorization List / Yetkilendirme Listesi
[[EIP-7702]] içindeki, bir EOA'nın hangi kodu yetkilendirdiğini belirten veri yapısıdır. Geliştirici tarafında çoğunlukla cüzdan veya kütüphane tarafından hazırlanır.

## B

### Batch İşlem / Toplu İşlem
Birden fazla çağrının tek kullanıcı eylemiyle veya tek zincir üstü işlemle yapılmasıdır. AA cüzdanlarının en çok kullanılan UX kazanımlarından biridir.

### BLOB
Kısa süre saklanan ama ucuz data availability alanını temsil eden veri paketidir. Özellikle [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]] ile rollup verisini calldata dışında taşımak için kullanılır.

### BLS12-381
Pairing tabanlı modern kriptografi için kullanılan eğri ailesidir. Ethereum execution layer tarafında bunun yerleşik karşılığı [[Precompiles/EIP, RIP & ERC/EIP-2537|EIP-2537]] ile gelir.

### Bundler
[[ERC-4337]] dünyasında `UserOperation` toplayan, bunları simüle eden ve zincire gönderen aktördür. Teknik olarak bir nevi özel işlem toplayıcıdır.

## C

### CallData
Bir kontrat çağrısına gönderilen ham girdi verisidir. AA sistemlerinde hem doğrulama hem yürütme aşamasında ne yapılacağını belirleyen temel girdilerden biridir.

### Crosschain Mint / Burn
Bir token'ın, köprü veya benzeri yetkili bir kontrat tarafından başka zincirde temsil edilmek üzere mint ya da burn edilmesidir. Token tarafındaki minimal arayüz standardizasyonu için [[Token/EIP, RIP & ERC/ERC-7802|ERC-7802]] öne çıkar.

### Custom Error
Solidity'nin yapılandırılmış hata tipidir; revert string yerine daha ucuz ve daha kolay ayrıştırılabilir hata yüzeyi sunar. Token standartlarında bunun ortak hata dili [[Token/EIP, RIP & ERC/ERC-6093|ERC-6093]] ile tanımlanır.

### Chain ID
Bir Ethereum zincirini diğerlerinden ayıran kimlik değeridir. İşlem güvenliği, ağ değiştirme ve cüzdanın doğru ağa bağlanması açısından kritiktir; [[EIP-155]], [[EIP-3085]] ve [[EIP-3326]] ile sık ilişkilidir.

### Contract Account / Kontrat Hesabı
Üzerinde kod bulunan Ethereum hesabıdır. AA mantığının büyük kısmı, hesabın davranışını bu kod üzerinden tanımlamaya dayanır.

## D

### Delegatecall
Başka bir kontratın kodunu, çağıran hesabın depolama alanında çalıştıran EVM mekanizmasıdır. [[EIP-5806]] ve bazı akıllı hesap mimarilerini anlamak için önemlidir.

### DoS (Denial of Service)
Sistemi pahalı, verimsiz veya çalışamaz hale getirmeyi hedefleyen saldırı sınıfıdır. [[ERC-7562]] tam olarak bu riskleri azaltmak için vardır.

## E

### EntryPoint
[[ERC-4337]]'de tüm `UserOperation` akışının geçtiği merkezi kontrattır. Hesap doğrulaması, paymaster çağrısı ve yürütme akışı burada başlar.

### EOA (Externally Owned Account)
Private key ile kontrol edilen klasik Ethereum hesabıdır. AA tartışmalarının önemli kısmı, EOA'ların sınırlarını aşmakla ilgilidir.

### ERC
Ethereum uygulama katmanı standartlarını tanımlayan teklif ailesidir. [[ERC-4337]], [[ERC-6900]] ve [[ERC-7562]] bu gruptadır.

### Ethereum Provider / Wallet Provider
Wallet'ın web sayfasına sunduğu JavaScript arayüzüdür. Dapp bu nesne üzerinden istek atar, event dinler ve wallet ile konuşur; modern karşılığı [[EIP-1193]] ile standardize edilir.

## F

### Factory
Yeni akıllı hesapları oluşturan kontrattır. [[ERC-4337]] içinde ilk kullanımda hesap oluşturma akışlarında sıkça yer alır.

### Fungible Token
Her biriminin diğer birimlerle aynı kabul edildiği token türüdür. Bu modelin Ethereum üzerindeki temel standardı [[Token/EIP, RIP & ERC/ERC-20|ERC-20]]'dir.

### Frame Transaction
[[EIP-8141]] ile önerilen yeni işlem modelidir. İşlemi doğrulama, ödeme ve yürütme çerçevelerine ayırarak yerleşik hesap soyutlaması hedefler.

## G

### Gas / Gaz
EVM üzerinde işlem yapmak için harcanan hesaplama maliyetidir. AA sistemleri çoğu zaman "gazı kimin ödediği" sorusunu esnek hale getirir.

### Gas Sponsorluk
Kullanıcının gazı doğrudan kendisinin ödememesi durumudur. Genelde paymaster veya benzeri bir sponsor mantığı ile sağlanır.

### Gas UX
Kullanıcının işlem ücreti ekranlarında gördüğü ücret modeli, tahmin mantığı ve onay deneyimidir. Özellikle [[EIP-1559]] sonrası modern wallet tasarımında ayrı bir araştırma alanı haline gelmiştir.

## H

### Hook / Kanca
Bir işlemden önce veya sonra otomatik çalışan genişletme noktasıdır. Özellikle [[ERC-6900]] gibi modüler hesap standartlarında sık görülür.

## I

### Invoker
[[EIP-3074]] bağlamında, EOA'nın yetki verdiği ve onun adına işlem yapan kontrattır. Bu terim özellikle `AUTH` ve `AUTHCALL` tasarımında önemlidir.

## K

### KZG
Blob verisine dair commitment ve doğrulama modelini kuran polynomial commitment ailesidir. Execution layer tarafında bunun en görünür yansıması [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]] içindeki point evaluation precompile'ıdır.

## M

### Mempool
Henüz bloklara girmemiş işlemlerin beklediği ağ havuzudur. [[ERC-4337]] kendi alternatif mempool yapısını kullanır; yerleşik AA önerileri ise bunu protokol seviyesine taşımayı hedefler.

### Modüler Hesap
Hesap mantığının tek parça yerine eklenti, doğrulayıcı ve kanca gibi modüllere ayrıldığı akıllı hesap yaklaşımıdır. [[ERC-6900]] bunun standartlaşma tarafını temsil eder.

### Multi Token Standard
Tek bir kontrat içinde birden fazla token tipini barındırabilen yaklaşımı ifade eder. Ethereum'daki en yaygın standart karşılığı [[Token/EIP, RIP & ERC/ERC-1155|ERC-1155]]'tir.

### Multi Injected Wallet
Aynı tarayıcıda birden fazla wallet uzantısının provider enjekte etmesi durumudur. Bu keşif ve seçim problemini çözmeye çalışan standart [[EIP-6963]]'tür.

## N

### NFT (Non-Fungible Token)
Birbirinin yerine geçmeyen, her bir örneği ayrı kimlik taşıyan token türüdür. Ethereum'da bunun temel standart yüzeyi [[Token/EIP, RIP & ERC/ERC-721|ERC-721]] ile yaygınlaştı; daha esnek çoklu varlık modeli ise [[Token/EIP, RIP & ERC/ERC-1155|ERC-1155]] ile geldi.

### Nonce
Bir hesabın işlemlerini sıralamak ve tekrar oynatmayı engellemek için kullanılan sayaçtır. AA sistemlerinde klasik tek sayaç modeli yerine daha esnek nonce yapıları görülebilir.

## O

### Operator
Bir kullanıcının token'ları üzerinde, belirli kurallar dahilinde onun adına işlem yapabilen yetkili aktördür. ERC-20 allowance modelinden farklı operator yüzeyleri [[Token/EIP, RIP & ERC/ERC-777|ERC-777]] ve [[Token/EIP, RIP & ERC/ERC-6909|ERC-6909]] gibi standartlarda görülür.

### Opcode / İşlem Kodu
EVM'in temel komutlarıdır. [[EIP-3074]] ve [[EIP-5003]] gibi bazı öneriler yeni işlem kodları eklemeyi amaçlar.

## P

### Passkey
Genelde cihaz veya tarayıcı destekli, kullanıcı dostu açık anahtar kimlik doğrulama yaklaşımıdır. AA cüzdanlarında özellikle [[EIP-7212]] ile birlikte önem kazanır.

### Paymaster
[[ERC-4337]] içinde kullanıcı adına gaz ödeyebilen yardımcı kontrattır. Uygulama tarafından sponsorlu işlem akışlarının merkezinde yer alır.

### Permit
Kullanıcının token onayını ayrı bir zincir üstü `approve` işlemi yerine imza ile vermesini sağlayan akıştır. ERC-20 tarafındaki standart karşılığı [[ERC-2612]]'dir.

### Plugin / Eklenti
Bir akıllı hesaba sonradan davranış ekleyen modüldür. [[ERC-6900]] ekosisteminin temel kavramlarından biridir.

### Precompile / Ön Derleme
EVM içinde özel adreslerde sunulan, sık kullanılan ama pahalı hesaplamaları daha verimli yapan yerleşik işlemlerdir. Genel harita için [[Precompiles/Precompiles EIPs|Precompiles EIPs]] notuna bakılabilir; modern örnekler arasında [[Precompiles/EIP, RIP & ERC/EIP-2537|EIP-2537]], [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]] ve [[EIP-7212]] bulunur.

### Provider Discovery
Bir dapp'in kullanıcının tarayıcısındaki wallet provider'ları bulma sürecidir. Tek provider varsayımından çoklu provider keşfine geçişte [[EIP-6963]] öne çıkar.

## R

### Replay Attack / Tekrar Oynatma Saldırısı
Bir imzanın veya işlemin yeniden kullanılarak istenmeyen şekilde tekrar çalıştırılmasıdır. Nonce ve alan ayrımı bu riskin ana savunmalarıdır.

### RIP (Rollup Improvement Proposal)
Özellikle rollup ekosistemine odaklanan standart / teklif ailesidir. [[RIP-7560]] bunun AA tarafındaki en önemli örneklerinden biridir.

## S

### Safe Transfer
Bir token transferinin, alıcı kontratın ilgili receiver arayüzünü gerçekten desteklediği doğrulanarak yapılması yaklaşımıdır. ERC-20 tarafındaki önemli örnekler [[Token/EIP, RIP & ERC/ERC-4524|ERC-4524]], daha erken reaksiyonlar ise [[Token/EIP, RIP & ERC/ERC-223|ERC-223]] ve [[Token/EIP, RIP & ERC/ERC-1363|ERC-1363]] hattında görülebilir.

### Session Key / Oturum Anahtarı
Ana anahtardan daha sınırlı yetkilere sahip, kısa ömürlü veya amaca özel anahtardır. Oyun, otomasyon ve uygulama içi deneyimlerde çok değerlidir.

### SETCODE
[[EIP-6913]] bağlamında, bir hesabın kodunu yerinde değiştirmeyi amaçlayan yaklaşımın merkezindeki komuttur.

### Sign-In with Ethereum (SIWE)
Bir kullanıcının Ethereum hesabıyla offchain servislere standart mesaj biçimi üzerinden giriş yapmasıdır. Bunun standart referansı [[ERC-4361]]'dir.

### Smart Account / Akıllı Hesap
Davranışı kod ile tanımlanan, özel doğrulama ve yürütme mantığına sahip kullanıcı hesabıdır. Güncel AA ürünlerinin çoğu aslında akıllı hesap cüzdanlarıdır.

### Sponsorlu İşlem
Gazı son kullanıcı yerine uygulamanın, paymaster'ın veya başka bir tarafın ödediği işlem modelidir.

## T

### Temporary Approval
Yalnızca tek transaction süresince geçerli olan geçici token harcama yetkisidir. Kalıcı allowance bırakmadan işlem yapmayı hedefleyen standart uzantı [[Token/EIP, RIP & ERC/ERC-7674|ERC-7674]]'tür.

### Token Metadata
Bir token'ın adı, sembolü, URI'si, görseli veya açıklaması gibi insan dostu tanımlayıcı verileridir. [[Token/EIP, RIP & ERC/ERC-20|ERC-20]], [[Token/EIP, RIP & ERC/ERC-721|ERC-721]] ve [[Token/EIP, RIP & ERC/ERC-1155|ERC-1155]] ekosistemlerinde farklı biçimlerde kullanılır.

### Tokenized Vault
Temel bir ERC-20 varlığı yöneten ve kullanıcıya bunun üstünde pay temsil eden share token veren vault yapısıdır. Bu modelin standart yüzeyi [[Token/EIP, RIP & ERC/ERC-4626|ERC-4626]] ile tanımlanır.

### Transfer Reference / Odeme Referansi
Bir token transferine invoice, siparis veya mutabakat baglami eklemek icin tasinan referans verisidir. ERC-20 transferlerine bu katmani ekleyen standart [[Token/EIP, RIP & ERC/ERC-7699|ERC-7699]]'dur.

### Transient Storage / Gecici Depolama
Yalnizca bir transaction suresince var olan ve transaction sonunda silinen depolama alanidir. Tek seferlik token approval akislari icin [[Token/EIP, RIP & ERC/ERC-7674|ERC-7674]] baglaminda onem kazanir.

### Type 4 İşlem
[[EIP-7702]] ile gelen yeni işlem türüdür. EOA'nın bir yetkilendirme listesi üzerinden kod delegasyonu yapmasını sağlar.

### Typed Data
Kullanıcının imzaladığı verinin alan alan anlamlı biçimde tanımlanmasıdır. Wallet'ın daha okunabilir imza ekranı göstermesini sağlar; temel standart [[EIP-712]]'dir.

## U

### UI Multiplier / Goruntuleme Carpani
Bir token'in ham bakiyesini degistirmeden, kullaniciya gosterilen miktari olceklendiren carpandir. Ozellikle hisse bolunmesi benzeri durumlar icin [[Token/EIP, RIP & ERC/ERC-8056|ERC-8056]] ile standartlastirilir.

### UserOperation
[[ERC-4337]]'de kullanıcının niyetini taşıyan üst seviye işlem nesnesidir. Zincire doğrudan klasik işlem olarak değil, bundler aracılığıyla gider.

## V

### Validation / Doğrulama
Bir işlemin veya `UserOperation`'ın geçerli olup olmadığını kontrol eden aşamadır. AA sistemlerinde bu mantık hesap koduna taşındığı için çok daha esnek, ama aynı zamanda daha risklidir.

### Verification Gas Limit
Doğrulama aşamasında harcanabilecek gaz sınırıdır. Özellikle [[ERC-4337]] entegrasyonlarında yanlış ayarlanırsa işlemler gereksiz yere başarısız olabilir.

## W

### Wallet RPC
Cüzdanın dapp'e sunduğu, wallet davranışını tetikleyen RPC metodlarıdır. `wallet_addEthereumChain`, `wallet_switchEthereumChain`, `wallet_watchAsset` ve `wallet_sendCalls` bunun tipik örnekleridir.

## Y

### Yerleşik AA (Enshrined / Native AA)
Hesap soyutlamasının uygulama katmanında değil, doğrudan protokolün içine yerleştirilmesi yaklaşımıdır. [[RIP-7560]] ve [[EIP-8141]] bu yönün başlıca örnekleridir.

## Z

### Zincir Üstü / Zincir Dışı
Bir işlemin veya mantığın blok zincirin içinde mi dışında mı gerçekleştiğini anlatır. AA sistemleri genelde ikisini birlikte kullanır: doğrulamanın bir kısmı zincir dışında simüle edilir, asıl yürütme zincir üstünde olur.
