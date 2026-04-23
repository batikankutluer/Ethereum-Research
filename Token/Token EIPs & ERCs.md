# Token EIPs / ERCs

Ethereum'daki token standardizasyonunu, [[Sözlük#Fungible Token|fungible token]]'dan [[Sözlük#NFT (Non-Fungible Token)|NFT]] ve [[Sözlük#Multi Token Standard|multi-token]] modeline kadar tarihsel sırayla toplayan ana indeks notu.
Genel araştırma şeması için: [[Araştırma Planı]]

## Geliştirici İçin Başlangıç Rotası

- [[ERC-20]] — [[Sözlük#Fungible Token|fungible token]] arayüzünün temel standardı
- [[ERC-6093]] — modern token implementasyonlarında standart [[Sözlük#Custom Error|custom error]] yüzeyi
- [[ERC-721]] — [[Sözlük#NFT (Non-Fungible Token)|NFT]] standardizasyonunun ana kırılma noktası
- [[ERC-1155]] — tek kontratta çoklu token tipi yaklaşımı
- [[ERC-6909]] — ERC-1155 sonrası minimal [[Sözlük#Multi Token Standard|multi-token]] yaklaşımı
- [[ERC-7802]] — multi-chain token arayüzü için [[Sözlük#Crosschain Mint / Burn|mint/burn]] standardizasyonu
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]] — `permit` ile token onay UX'ini iyileştiren uzantı
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]] — cüzdana token ekletme akışını standardize eden wallet RPC

---

- [[ERC-20]] — 2015 / 2017 — [[Sözlük#Fungible Token|fungible token]] standardı
- [[ERC-223]] — 2017 — ERC-20 transfer modeline erken kontrat-alıcı tepkisi
- [[ERC-777]] — 2017 / 2019 — hook ve [[Sözlük#Operator|operator]] tabanlı ileri fungible token standardı
- [[ERC-721]] — 2018 — [[Sözlük#NFT (Non-Fungible Token)|NFT]] standardı
- [[ERC-1363]] — 2018 / 2020 — `transferAndCall` / `approveAndCall` uzantısı
- [[ERC-1155]] — 2018 / 2019 — [[Sözlük#Multi Token Standard|multi-token]] standardı
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]] — 2018 — cüzdana token izletme akışı
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]] — 2019 — imzalı token onayı (`permit`)
- [[ERC-3009]] — 2020 — imzalı transfer / authorization hattı
- [[ERC-4626]] — 2021 — [[Sözlük#Tokenized Vault|vault share]] standardı
- [[ERC-4524]] — 2021 — ERC-20 için [[Sözlük#Safe Transfer|safe transfer]] / receiver hattı
- [[ERC-6093]] — 2022 / 2023 — token [[Sözlük#Custom Error|custom error]] standardizasyonu
- [[ERC-6864]] — 2023 — upgradable fungible token uzantısı
- [[ERC-6909]] — 2023 / 2025 — minimal [[Sözlük#Multi Token Standard|multi-token]] standardı
- [[ERC-7674]] — 2024 — tek işlem süreli [[Sözlük#Temporary Approval|temporary approval]] uzantısı
- [[ERC-7699]] — 2024 — [[Sözlük#Transfer Reference / Odeme Referansi|transfer reference / ödeme referansı]] uzantısı
- [[ERC-7802]] — 2024 — [[Sözlük#Crosschain Mint / Burn|crosschain mint/burn]] token arayüzü
- [[ERC-8056]] — 2025 — [[Sözlük#UI Multiplier / Goruntuleme Carpani|UI amount scaling]] / stock split görünüm katmanı

## ERC-20 Genişleme Hattı

ERC-20 tek başına token ekonomisinin tabanını kurdu; ama onu izleyen yıllarda asıl genişleme üç eksende geldi:

- erken tasarım tepkileri: [[ERC-223]] ve [[ERC-777]]
- ödeme / callback uzantıları: [[ERC-1363]]
- imza ve yetkilendirme katmanı: [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]], [[ERC-3009]], altyapıda [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-712|EIP-712]]
- protokol ve DeFi soyutlaması: [[ERC-4626]] ve [[Sözlük#Tokenized Vault|tokenized vault]] modeli
- operasyonel ve implementasyon ergonomisi: [[ERC-4524]], [[ERC-6093]], [[ERC-6864]], [[ERC-7674]], [[ERC-7699]]
- multi-chain ve kurumsal uzantılar: [[ERC-7802]], [[ERC-8056]]
- wallet görünürlüğü: [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]]

Bu çizgi, ERC-20'nin neden yalnızca “ilk token standardı” değil, aynı zamanda sonraki token UX ve DeFi tasarımlarının merkez arayüzü olduğunu gösterir.

## Araştırma Kümeleri

### Fungible Token Temeli
- [[ERC-20]]
- [[ERC-223]]
- [[ERC-777]]
- [[ERC-1363]]
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]]
- [[ERC-3009]]
- [[ERC-4524]]
- [[ERC-6093]]
- [[ERC-6864]]
- [[ERC-4626]]
- [[ERC-7674]]
- [[ERC-7699]]
- [[ERC-7802]]
- [[ERC-8056]]

### NFT ve Dijital Mülkiyet
- [[ERC-721]]
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]]

### Çoklu Token Mimarisi
- [[ERC-1155]]
- [[ERC-6909]]
- [[ERC-20]]
- [[ERC-721]]

### Wallet ve Token UX Katmanı
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-747|EIP-747]]
- [[Wallet & Transaction UX/EIP, RIP & ERC/ERC-2612|ERC-2612]]
- [[Wallet & Transaction UX/Wallet & Transaction UX EIPs|Wallet & Transaction UX EIPs]]

## Bağlantılı Notlar

- [[Tarihçe]]
- [[Sözlük#Fungible Token|Sözlük: Fungible Token]]
- [[Sözlük#Custom Error|Sözlük: Custom Error]]
- [[Sözlük#NFT (Non-Fungible Token)|Sözlük: NFT]]
- [[Sözlük#Multi Token Standard|Sözlük: Multi Token Standard]]
- [[Sözlük#Safe Transfer|Sözlük: Safe Transfer]]
- [[Sözlük#Temporary Approval|Sözlük: Temporary Approval]]
- [[Sözlük#Tokenized Vault|Sözlük: Tokenized Vault]]
- [[Sözlük#Crosschain Mint / Burn|Sözlük: Crosschain Mint / Burn]]
- [[Wallet & Transaction UX/Wallet & Transaction UX EIPs|Wallet & Transaction UX EIPs]]
