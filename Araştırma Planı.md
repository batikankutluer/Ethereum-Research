# Araştırma Planı

Bu not, vault içindeki tüm araştırmalar için genel çalışma şemasını tanımlar.
Amaç: her yeni konuda sıfırdan dağınık notlar açmak yerine, aynı mantıkla ilerlemek ve araştırma çıktısını kalıcı bilgiye dönüştürmek.

## 1. Amaç

- araştırmayı soru odaklı başlatmak
- kaynak toplamayı sistematik yapmak
- notları tekrar kullanılabilir hale getirmek
- yeni konuları mevcut bilgi ağına bağlamak

## 2. Temel Araştırma Akışı

1. Soruyu tanımla.
   Bu araştırma tam olarak neyi cevaplıyor?
2. Kapsamı daralt.
   Tarihsel çerçeve mi, teknik detay mı, karşılaştırma mı, implementasyon mu?
3. Kaynakları topla.
   Önce resmi kaynaklar, sonra implementasyon, sonra tartışmalar.
4. İlk notu çıkar.
   Kısa cevap, ana kavramlar, kritik linkler.
5. Yapılandır.
   Notu ilgili standartlara, kavramlara ve diğer araştırmalara bağla.
6. Açık soruları bırak.
   Henüz net olmayan noktaları ayrıca işaretle.
7. Sonraki adımı tanımla.
   Bu araştırmadan sonra hangi konu doğal devam niteliğinde?

## 3. Oturum Davranışı

Bir araştırma isteği geldiğinde çıktı mümkün olduğunca tek seferde tam bırakılmalı.

Bu şu anlama gelir:

- tek bir soruya karşılık yalnızca taslak değil, mümkün olan en tamamlanmış çıktı üretilmeli
- araştırma, not açma, indeks güncelleme, sözlük güncelleme ve gerekli linkleme aynı akış içinde bitirilmeli
- kullanıcı daha önce yapı hakkında düzeltme yaptıysa, yeni araştırmada bu düzeltmeler varsayılan kural sayılmalı
- aynı konu için yarım kalan ara yapı bırakmak yerine mevcut notlar güncellenmeli
- ayrı klasör planları üretilmemeli; plan / şema notu kökte tekil kalmalı

Kısacası hedef, "tek soru -> güncellenmiş ve kullanılabilir bütün çıktı" olmalıdır.

## 4. Not Türleri

### İndeks Notu
Bir alanın veya klasörün giriş kapısıdır.

Görevi:
- ana başlıkları toplamak
- alt notlara yol vermek
- hızlı yön bulma sağlamak

### Konu Notu
Tek bir soruya veya probleme odaklanır.

Örnek:
- `Araştırma - Bundler Doğrulama Riski.md`
- `Araştırma - Passkey ile Cüzdan Girişi.md`

### Karşılaştırma Notu
İki veya daha fazla yaklaşımı kıyaslar.

Örnek:
- `Karşılaştırma - X vs Y.md`
- `Karşılaştırma - İki SDK'nın Farkları.md`

### Kavram Notu
Tekrarlayan terimleri açıklar.

Örnek:
- `Sözlük`
- `Kavram - Mempool.md`

### Kaynak Notu
Belirli bir döküman, repo veya spesifikasyon için kısa özet notudur.

Örnek:
- `Kaynak - EIP-4337.md`
- `Kaynak - Viem Docs.md`

### Açık Sorular Notu
Henüz netleşmemiş noktaları ve takip edilmesi gereken başlıkları toplar.

Örnek:
- `Açık Sorular - Konu Adı.md`

## 5. Kaynak Öncelik Sırası

Araştırmada mümkünse şu sırayı takip et:

1. resmi spesifikasyon veya resmi dokümantasyon
2. referans implementasyon veya resmi repo
3. tartışma başlıkları, issue'lar, forum yazışmaları
4. proje dokümantasyonu veya SDK dokümantasyonu
5. teknik blog yazıları ve açıklayıcı içerikler
6. özet / ikinci el içerikler

## 6. Yeni Not Açma Standardı

Her yeni araştırma notunda mümkünse şu iskelet kullanılsın:

```md
# Başlık

## Soru

Bu not hangi soruya cevap veriyor?

## Kısa Cevap

1-3 paragrafta ana sonuç.

## Neden Önemli

Bu konunun pratik değeri ne?

## Bağlantılı Notlar

- ilgili indeks notu
- ilgili standart / konu notları

## İlgili Terimler

- [[Sözlük#...]]

## Teknik Notlar

Mimari, akış, sınırlamalar, trade-off'lar.

## Açık Sorular

- belirsiz kalan noktalar

## Kaynaklar

- resmi kaynaklar
- implementasyon
- tartışmalar
```

## 7. Linkleme Kuralları

Her notta mümkünse:

- ilk geçen önemli kavram `[[Sözlük#...]]` ile bağlanmalı
- ilgili standart veya konu notları linklenmeli
- eğer not bir karşılaştırma ise kıyaslanan iki taraf da doğrudan linklenmeli
- eğer not bir kaynağa dayanıyorsa, kaynak notu veya doğrudan link bırakılmalı
- ayrı bir `İlgili Terimler` bloğu yerine, mümkün olduğunda terimler doğrudan cümle içinde bağlanmalı

## 8. Araştırma Çıktısı Standardı

İyi bir araştırma notu en az şu soruları cevaplamalı:

- bu konu nedir?
- hangi problemi çözüyor?
- neden şimdi önemli?
- alternatifleri neler?
- riskleri veya sınırlamaları neler?
- bir geliştirici buradan nereye gitmeli?

İyi bir araştırma çıktısı ayrıca şunları da yapmalı:

- mevcut klasör yapısına düzgün oturmalı
- daha önce açılmış indeks ve referans notlarıyla çelişmemeli
- gerekiyorsa mevcut notları güncelleyerek tekilleşmeli
- araştırma sonunda kullanıcıya ayrı bir eksik iş listesi bırakmamalı
- sonraki oturumda başka bir agent geldiğinde bağlamı notların içinden anlayabileceği kadar düzenli olmalı

## 9. Adlandırma Standardı

Karışıklığı azaltmak için not adlarında şu desenler tercih edilsin:

- `Araştırma - ...`
- `Karşılaştırma - ...`
- `Kaynak - ...`
- `Açık Sorular - ...`
- `Uygulama - ...`

## 10. Araştırma Yaparken Karar Ağacı

Yeni bir konu geldiğinde:

1. önce bunun bir kavram mı, standart mı, ürün mü, karşılaştırma mı olduğuna karar ver
2. eğer tek konuysa konu notu aç
3. eğer iki şey kıyaslanıyorsa karşılaştırma notu aç
4. eğer cevap çok dağınıksa önce açık sorular notu aç
5. eğer kavram tekrar edecekse sözlüğe ekle

## 11. Yapısal Kurallar

- genel plan / şema notu kökte tek bir dosya olarak tutulur: `[[Araştırma Planı]]`
- konu klasörleri bilgi, indeks, referans ve araştırma notları içerir; ayrı plan notu içermez
- aynı ada sahip standart notu zaten başka klasörde varsa, mümkünse kopya açmak yerine mevcut nota referans verilir
- sözlük tekildir ve yeni konular geldikçe aynı dosya güncellenir
- kullanıcı bir yapısal tercih belirttiyse bu tercih sonraki araştırmalarda korunur

## 12. Klasör Bağımsız Kullanım

Bu plan tek bir klasöre bağlı değildir.
İster `Account Abstraction`, ister başka bir Ethereum konusu, ister tamamen farklı bir araştırma alanı olsun, aynı şema uygulanabilir.

Kısacası bu not, yeni araştırmaları başlatmak ve düzenli tutmak için genel çerçevedir.
