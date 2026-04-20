# Tarihçe

Ethereum'un tarihini, büyük kırılma anlarını ve bugün araştırdığımız standartların hangi bağlamda ortaya çıktığını kronolojik olarak toplayan giriş notu.
Genel araştırma şeması için: [[Araştırma Planı]]

## Nasıl Okunmalı?

Bu not bir fork listesi değil; Ethereum'un ürün, protokol ve standart evrimini kısa bir harita halinde sunar. Gerekli yerlerde ilgili notlara geçiş verir:

- hesap modeli ve akıllı cüzdan yönü için [[Account Abstraction/Account Abstraction EIPs|Account Abstraction EIPs]]
- cüzdan, imza ve işlem deneyimi için [[Wallet & Transaction UX/Wallet & Transaction UX EIPs|Wallet & Transaction UX EIPs]]
- execution layer kriptografisi için [[Precompiles/Precompiles EIPs|Precompiles EIPs]]

## Kronolojik Akış

### 2013-2014: Fikir, whitepaper ve ilk finansman

- **11.2013** — Vitalik Buterin Ethereum whitepaper'ını yayımladı; zincirin genel amaçlı kontrat yürütme katmanı olması fikri burada netleşti.
- **22.07.2014** — Ethereum crowdsale başladı.
- **02.09.2014** — crowdsale sona erdi ve erken finansman dönemi tamamlandı.
- Bu dönem, sonraki tüm tartışmaların temelini kurar: hesap modeli, execution ortamı, gas, kontrat güvenliği ve state büyümesi.

### 2015: Mainnet başlangıcı

- **30.07.2015** — Ethereum mainnet `Frontier` ile canlıya geçti.
- Bu dönem daha çok temel execution modelinin ve erken geliştirici ekosisteminin oluştuğu dönemdir.
- Daha sonra [[Account Abstraction/EIP, RIP & ERC/EIP-101|EIP-101]] gibi erken AA fikirleri de bu ilk nesil tasarım sınırlarını görünür hale getirdi.

### 2016: Homestead, DAO krizi ve zincir ayrışması

- **14.03.2016** — `Homestead` aktif oldu; Ethereum daha kararlı üretim evresine geçti.
- **17.06.2016** — `The DAO` saldırısı gerçekleşti.
- **20.07.2016** — DAO hard fork'u uygulandı; bu olay Ethereum ve Ethereum Classic ayrışmasının temel anı oldu.
- Zincir ayrışması sonrası replay koruması ve zincir kimliği daha merkezi hale geldi; bunun standart tarafındaki en önemli izi [[EIP-155]] notunda görülebilir.
- Aynı dönemde mesaj imzalama ve cüzdan tarafındaki güvenli yüzeyler için [[ERC-191]] gibi temel taşlar oluştu.

### 2017: Byzantium ve ilk büyük execution genişlemesi

- **16.10.2017** — `Byzantium` aktif oldu.
- Execution layer'a yeni kriptografik yetenekler kazandırıldı; özellikle zk doğrulama için gerekli primitive'ler bu dönemde önem kazandı. Bunun precompile tarafındaki haritası [[Precompiles/Araştırma - Klasik EVM Precompile Haritası|Araştırma - Klasik EVM Precompile Haritası]] içinde detaylandırılıyor.
- Aynı yıl [[EIP-86]] ve [[EIP-712]] gibi öneriler, iki farklı ama etkili hattı güçlendirdi:
  - işlem ve hesap mantığını daha esnek kılma
  - imza deneyimini daha anlamlı ve güvenli hale getirme

### 2018-2019: Wallet standardizasyonu ve Istanbul

- **2018** — [[EIP-1102]], [[EIP-1193]] ve [[ERC-1271]] gibi notlarla modern wallet-provider ve akıllı hesap imza yüzeyi şekillenmeye başladı.
- **28.02.2019** — `Constantinople / St. Petersburg` aktif oldu.
- **08.12.2019** — `Istanbul` aktif oldu.
- Bu dönem, fee market ve modern gas tartışmalarını güçlendirdi; bunun en önemli kırılma noktası daha sonra devreye girecek [[EIP-1559]] oldu.
- Istanbul ve devamındaki iyileştirmeler, precompile'ların sadece var olmasını değil, ekonomik olarak kullanılabilir hale gelmesini sağladı; bu çizgi [[Precompiles/Precompiles EIPs|Precompiles EIPs]] altında izlenebilir.

### 2020: Beacon Chain ve typed transaction dönemi

- **01.12.2020** — `Beacon Chain` genesis'i gerçekleşti; proof-of-stake geçişinin ayrı konsensüs katmanı ayağı fiilen başladı.
- [[Account Abstraction/EIP, RIP & ERC/EIP-2718|EIP-2718]] ile typed transaction envelope yaklaşımı geldi.
- [[EIP-2930]] access list işlemleriyle daha gelişmiş işlem biçimleri görünür hale geldi.
- Aynı yıllarda [[Account Abstraction/EIP, RIP & ERC/EIP-2938|EIP-2938]] gibi yerleşik AA girişimleri de protokol seviyesinde hesap soyutlamasının nasıl görünebileceğine dair ilk ciddi çerçeveyi sundu.

### 2021: Berlin ve London

- **15.04.2021** — `Berlin` aktif oldu.
- **05.08.2021** — `London` aktif oldu ve [[EIP-1559]] ile gas piyasası kullanıcı deneyimi açısından kökten değişti.
- [[EIP-3074]] ve [[ERC-4337]] bu dönemin iki çok önemli ama farklı yönünü temsil eder:
  - `EOA` davranışını genişletme
  - uygulama katmanında akıllı hesap tabanlı yeni işlem modeli kurma
- Wallet tarafında [[EIP-3326]] ve [[ERC-4361]] gibi notlar, zincir değiştirme ve offchain kimlik doğrulama deneyimini şekillendirdi.

### 2022: The Merge

- **15.09.2022** — `The Merge` tamamlandı; Ethereum proof-of-work'ten proof-of-stake'e geçti.
- Bu kırılma yalnızca konsensüs değişimi değildi; sonraki veri erişilebilirliği ve rollup odaklı yol haritası için de yeni temel oluşturdu.
- [[EIP-5792]] gibi wallet capability yönü ve [[Account Abstraction/EIP, RIP & ERC/EIP-5003|EIP-5003]] / [[Account Abstraction/EIP, RIP & ERC/EIP-5806|EIP-5806]] gibi hesap evrimi tartışmaları da aynı genişleme döneminin parçalarıdır.

### 2023: Shanghai/Capella, AA ürünleşmesi ve passkey hattı

- **12.04.2023** — `Shanghai / Capella` aktif oldu; stake çekimleri açıldı.
- [[ERC-4337]] üretimde görünür hale geldi ve akıllı hesap mimarisi daha somut bir ürün katmanına dönüştü.
- [[ERC-7562]] doğrulama sınırları ve bundler güvenliği açısından kritik tamamlayıcı katmanı getirdi.
- [[ERC-6900]] modüler hesap yaklaşımını öne çıkardı.
- [[EIP-7212]] ile passkey / WebAuthn uyumlu P256 doğrulama execution layer tartışmasının parçası oldu.
- Wallet tarafında [[EIP-6963]] çoklu injected provider keşfini standartlaştırarak modern browser wallet deneyimindeki önemli bir problemi hedefledi.

### 2024: Dencun ve blob dönemi

- **13.03.2024** — `Dencun` aktif oldu.
- [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]] ile blob transaction modeli geldi.
- Bu, Ethereum tarihindeki en önemli L2 maliyet kırılmalarından biridir; data availability alanı ve blob gas ayrı bir ekonomik yüzey haline geldi.
- Precompile perspektifinden bakınca da bu dönem önemlidir, çünkü `0x0A` point evaluation precompile execution layer ile DA tasarımını birbirine bağlar.

### 2025: Pectra ve programlanabilir EOA

- **07.05.2025** — `Pectra` aktif oldu.
- [[EIP-7702]] canlıya geldi; bu, klasik `EOA` modeline kod delegasyonu ve programlanabilirlik getiren çok önemli bir kırılmadır.
- Aynı geniş çizgide [[Precompiles/EIP, RIP & ERC/EIP-2537|EIP-2537]] gibi daha güçlü kriptografik primitive'ler de execution layer kapasitesini büyüttü.
- Bu dönem, Ethereum'un yalnızca bir kontrat platformu değil, daha esnek hesap ve daha güçlü yerleşik kriptografi platformu haline geldiğini gösterir.

### 2026 ve sonrası: Yerleşik AA ve daha derin soyutlama arayışı

- [[RIP-7560]] ve [[EIP-8141]] gibi notlar, uygulama katmanı AA'dan daha yerleşik modellere giden yönü temsil eder.
- Bu başlıklar henüz tarih değil, takip edilen yol haritasıdır.
- Aynı şekilde precompile, wallet UX ve hesap modeli tarafındaki yeni ayrışmalar da burada doğal olarak birleşir.

## Büyük Tema Özeti

Ethereum tarihine bugünden bakınca dört büyük çizgi görülüyor:

### 1. İşlem ve hesap modeli genişlemesi

- [[EIP-86]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-3074|EIP-3074]]
- [[Account Abstraction/EIP, RIP & ERC/ERC-4337|ERC-4337]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-7702|EIP-7702]]
- [[RIP-7560]]

### 2. Wallet ve imza deneyiminin olgunlaşması

- [[EIP-1102]]
- [[EIP-1193]]
- [[EIP-712]]
- [[ERC-1271]]
- [[ERC-4361]]
- [[EIP-6963]]

### 3. Execution layer kriptografisinin büyümesi

- [[Precompiles/Precompiles EIPs|Precompiles EIPs]]
- [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]]
- [[Precompiles/EIP, RIP & ERC/EIP-2537|EIP-2537]]
- [[EIP-7212]]

### 4. Fee market ve veri erişilebilirliği dönüşümü

- [[EIP-1559]]
- [[Precompiles/EIP, RIP & ERC/EIP-4844|EIP-4844]]

## Bağlantılı Notlar

- [[Sözlük]]
- [[Account Abstraction/Account Abstraction EIPs|Account Abstraction EIPs]]
- [[Wallet & Transaction UX/Wallet & Transaction UX EIPs|Wallet & Transaction UX EIPs]]
- [[Precompiles/Precompiles EIPs|Precompiles EIPs]]
