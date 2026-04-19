# Wallet & Transaction UX EIPs / ERCs

Ethereum cüzdan deneyimi, imzalama akışları, işlem formatları ve wallet RPC standartlarını kronolojik sırayla toplayan ana indeks notu.
Genel araştırma şeması için: [[Araştırma Planı]]

## Geliştirici İçin Başlangıç Rotası

- [[EIP-1193]] — modern wallet provider arayüzünün temel standardı
- [[EIP-1102]] — hesap erişimi için izinli bağlantı modelinin başlangıcı
- [[EIP-3085]] — uygulamanın cüzdana yeni ağ ekletme akışı
- [[EIP-3326]] — uygulamanın cüzdanda ağ değiştirtme akışı
- [[EIP-712]] — kullanıcıya anlaşılır imza deneyimi için typed data standardı
- [[ERC-1271]] — akıllı hesapların imza doğrulama standardı
- [[ERC-4361]] — Sign-In with Ethereum akışı
- [[EIP-5792]] — modern toplu çağrı / wallet capability akışı
- [[EIP-6963]] — çoklu injected wallet keşfi

---

- [[ERC-191]] — 2016 — imzalı veri standardı
- [[EIP-155]] — 2016 — zincir kimliği ile replay koruması
- [[EIP-712]] — 2017 — typed structured data imzalama
- [[EIP-1102]] — 2018 — opt-in hesap erişimi
- [[EIP-1193]] — 2018 — Ethereum Provider JavaScript API
- [[ERC-1271]] — 2018 — kontrat hesapları için imza doğrulama
- [[EIP-747]] — 2018 — `wallet_watchAsset` ile token ekletme
- [[EIP-2255]] — 2019 — wallet permission sistemi
- [[ERC-2612]] — 2019 — `permit` ile imzalı token onayı
- [[EIP-1559]] — 2019 — fee market değişimi ve modern gas UX
- [[Account Abstraction/EIP, RIP & ERC/EIP-2718|EIP-2718]] — 2020 — typed transaction envelope
- [[EIP-2930]] — 2020 — access list işlemleri
- [[EIP-3085]] — 2020 — `wallet_addEthereumChain`
- [[EIP-3326]] — 2021 — `wallet_switchEthereumChain`
- [[ERC-4361]] — 2021 — Sign-In with Ethereum
- [[EIP-5792]] — 2022 — Wallet Call API
- [[EIP-6963]] — 2023 — multi injected provider discovery

## Araştırma Kümeleri

### Cüzdan Provider ve İzin Katmanı
- [[EIP-1102]]
- [[EIP-1193]]
- [[EIP-2255]]
- [[EIP-6963]]

### İmzalama ve Kimlik Doğrulama
- [[ERC-191]]
- [[EIP-712]]
- [[ERC-1271]]
- [[ERC-2612]]
- [[ERC-4361]]

### İşlem Biçimi ve Gas UX
- [[EIP-155]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-2718|EIP-2718]]
- [[EIP-2930]]
- [[EIP-1559]]

### Wallet RPC ve Uygulama UX
- [[EIP-3085]]
- [[EIP-3326]]
- [[EIP-5792]]
- [[EIP-747]]
