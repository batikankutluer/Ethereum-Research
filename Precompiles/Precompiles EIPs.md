# Precompiles EIPs

Ethereum'daki ön derlemeleri, bunların tarihsel gelişimini ve execution layer'a neden yerleştirildiklerini toplayan ana indeks notu.
Genel araştırma şeması için: [[Araştırma Planı]]

## Precompile Nedir?

[[Sözlük#Precompile / Ön Derleme|Ön Derleme]], EVM içinde sabit bir adreste çalışan yerleşik işlemdir. Amaç, `ecrecover`, eşleştirme tabanlı eğri işlemleri, `modexp` veya KZG doğrulaması gibi EVM içinde pahalı kalan hesaplamaları daha ucuz ve öngörülebilir hale getirmektir.

## Neden Varlar?

- kriptografik primitive'leri kontrat koduna göre daha verimli çalıştırmak
- doğrulama maliyetini düşürerek yeni kullanım alanları açmak
- opcode eklemeden execution layer'a yeni yetenek kazandırmak
- zk, DA, passkey ve imza doğrulama gibi alanlarda temel altyapı sunmak

## Geliştirici İçin Başlangıç Rotası

- [[Araştırma - Klasik EVM Precompile Haritası]] — temel aileleri, adres kümelerini ve tarihsel akışı görmek için
- [[EIP-4844]] — blob dönemi ve `0x0A` point evaluation precompile'ı için
- [[EIP-2537]] — BLS12-381 precompile ailesini anlamak için
- [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]] — P256 / passkey odaklı modern örnek için
- [[Karşılaştırma - P256 kontrat doğrulama vs EIP-7212]] — native doğrulama ile kontrat tabanlı doğrulama farkını görmek için

---

- `0x01-0x04` — ilk yerleşik yardımcılar: `ecrecover`, `sha256`, `ripemd160`, `identity`
- `EIP-198` — 2017 — `0x05` adresinde `modexp` ile büyük tamsayı modular exponentiation
- `EIP-196` — 2017 — `0x06` ve `0x07` adreslerinde `alt_bn128` toplama ve skaler çarpma
- `EIP-197` — 2017 — `0x08` adresinde `alt_bn128` pairing check
- `EIP-152` — 2016 / Istanbul — `0x09` adresinde `BLAKE2 F` compression function
- `EIP-1108` — 2018 / Istanbul — `alt_bn128` ön derlemelerinin gaz maliyetlerini aşağı çeker
- `EIP-2565` — 2020 / Berlin — `modexp` fiyatlamasını yeniden tanımlar
- [[EIP-4844]] — 2022 / Dencun — `0x0A` point evaluation precompile ve blob dönemi
- [[EIP-2537]] — 2020 / Pectra — `0x0B-0x11` aralığında BLS12-381 precompile ailesi
- [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]] — 2023 — P256 / secp256r1 için modern, zincir bazlı benimsenen precompile önerisi

## Araştırma Kümeleri

### Klasik EVM Ön Derlemeleri
- [[Araştırma - Klasik EVM Precompile Haritası]]
- `EIP-196`
- `EIP-197`
- `EIP-198`
- `EIP-152`
- `EIP-1108`
- `EIP-2565`

### Modern Kriptografik Ön Derlemeler
- [[EIP-2537]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-7212|EIP-7212]]

### Blob ve Data Availability Katmanı
- [[EIP-4844]]
- [[Wallet & Transaction UX/EIP, RIP & ERC/EIP-1559|EIP-1559]]
- [[Account Abstraction/EIP, RIP & ERC/EIP-2718|EIP-2718]]

### Uygulama ve Doğrulama Perspektifi
- [[Karşılaştırma - P256 kontrat doğrulama vs EIP-7212]]
- [[Account Abstraction/EIP, RIP & ERC/ERC-4337|ERC-4337]]
- [[Account Abstraction/EIP, RIP & ERC/ERC-7562|ERC-7562]]

## Bağlantılı Notlar

- [[Sözlük#Precompile / Ön Derleme|Sözlük: Ön Derleme]]
- [[Account Abstraction/Account Abstraction EIPs|Account Abstraction EIPs]]
- [[Wallet & Transaction UX/Wallet & Transaction UX EIPs|Wallet & Transaction UX EIPs]]
