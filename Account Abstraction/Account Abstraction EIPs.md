# Account Abstraction EIPs / ERCs / RIPs

Kronolojik sırayla, Ethereum'da hesap soyutlamasına dair tüm önemli öneriler.
Her notun sonunda resmi spesifikasyon, tartışma başlığı ve mümkünse uygulama / geliştirici dokümantasyonu bağlantıları var.
Genel araştırma şeması için: [[Araştırma Planı]]

## Geliştirici İçin Başlangıç Rotası

- [[ERC-4337]] — Bugün üretimde kullanılan temel [[Sözlük#AA (Account Abstraction / Hesap Soyutlaması)|AA]] standardı
- [[ERC-7562]] — [[Sözlük#Bundler|Bundler]] ve [[Sözlük#Validation / Doğrulama|doğrulama]] kurallarını anlamak için kritik tamamlayıcı standart
- [[EIP-7702]] — 7 Mayıs 2025'te Pectra ile ana ağa gelen [[Sözlük#EOA (Externally Owned Account)|EOA]] programlanabilirliği
- [[RIP-7560]] — [[Sözlük#Yerleşik AA (Enshrined / Native AA)|yerleşik AA]] yönünü görmek için
- [[EIP-8141]] — 2026 itibarıyla çerçeve işlem yaklaşımını takip etmek için

---

- [[EIP-101]] — 2015 — İlk kavramsal [[Sözlük#AA (Account Abstraction / Hesap Soyutlaması)|AA]] önerisi
- [[EIP-86]] — 2017 — İşlem kökeni ve imza soyutlaması
- [[EIP-2718]] — 2020 — Tipli işlem zarfı (temel)
- [[EIP-2938]] — 2020 — [[Sözlük#Contract Account / Kontrat Hesabı|kontrat hesapları]] için [[Sözlük#Yerleşik AA (Enshrined / Native AA)|yerleşik AA]] girişimi
- [[EIP-3074]] — 2021 — AUTH / AUTHCALL işlem kodları ile [[Sözlük#EOA (Externally Owned Account)|EOA]] yetki devri
- [[EIP-3607]] — 2021 — Geçiş sonrası imzalama anahtarının iptali
- [[ERC-4337]] — 2021 — Uygulama katmanı [[Sözlük#AA (Account Abstraction / Hesap Soyutlaması)|AA]] ([[Sözlük#Bundler|bundler]], [[Sözlük#Paymaster|paymaster]], [[Sözlük#EntryPoint|EntryPoint]])
- [[EIP-5003]] — 2022 — AUTHUSURP ile EOA → CA migrasyonu
- [[EIP-5806]] — 2022 — EOA'dan DELEGATECALL ile kod çalıştırma
- [[ERC-6900]] — 2023 — Modüler [[Sözlük#Smart Account / Akıllı Hesap|akıllı hesap]] standardı
- [[EIP-6913]] — 2023 — SETCODE ile EOA kendi kodunu set eder
- [[EIP-7212]] — 2023 — P256 ön derlemesi (Passkey / WebAuthn desteği)
- [[EIP-7377]] — 2023 — EOA → akıllı cüzdan geçiş tx tipi
- [[ERC-7562]] — 2023 — ERC-4337 [[Sözlük#Validation / Doğrulama|doğrulama]] kapsam kuralları
- [[RIP-7560]] — 2024 — [[Sözlük#Yerleşik AA (Enshrined / Native AA)|Yerleşik AA]], L2'leri de kapsıyor
- [[EIP-7702]] — 2025 — [[Sözlük#EOA (Externally Owned Account)|EOA]]'ya kod delegasyonu / programlanabilir cüzdan modeli (Pectra, **canlı**)
- [[EIP-8141]] — 2026 — [[Sözlük#Frame Transaction|Frame Transactions]], [[Sözlük#Yerleşik AA (Enshrined / Native AA)|yerleşik AA]] çatı önerisi (Hegota hedefi)
