# crypto-exchange-db-design
Bir kripto para borsası için geliştirilmiş, bire-çok (one-to-many) kullanıcı-cüzdan ilişkisine ve entegre saklı yordamlara (stored procedure) sahip ilişkisel veritabanı mimarisi.

# Kripto Para Borsası Veritabanı Mimarisi

Bu depo, bir kripto para borsa sistemi için hazırlanan temel ilişkisel veritabanı tasarımını içermektedir. Sistem; kullanıcı verilerini, varlık yönetimini ve karmaşık işlem/emir süreçlerini verimli ve güvenli bir şekilde yönetecek yapıda kurgulanmıştır.

## Temel Özellikler

* **Optimize Edilmiş İlişkisel Tasarım:** Veri bütünlüğü ve normalizasyon kuralları gözetilerek kurgulanmış, birbirine bağlı 6 temel tablodan oluşur.
* **Bire-Çok (One-to-Many) Mimari:** Tek bir kullanıcı profilinin birden fazla farklı kripto para cüzdanını güvenli bir şekilde yönetmesine olanak tanıyan, özel olarak tasarlanmış `Kullanıcı` - `Cüzdan` ilişkisi.
* **Saklı Yordamlar (Stored Procedures):** İş mantığını (business logic) veritabanı seviyesinde kapsülleyen; bakiye kontrolü, emir iptali ve oluşturulması gibi işlemleri güvenli (transaction bazlı) ve tutarlı hale getiren özelleştirilmiş yordamlar içerir.

## Teknolojiler ve Araçlar

* **Dil:** Transact-SQL (T-SQL)
* **Ortam:** SQL Server Management Studio (SSMS)
* **Tasarım Deseni:** Varlık-İlişki (ER) Modellemesi

## Depo İçeriği

* `kripto_borsa_sistemi.sql`: Tablo oluşturma kodlarını, CHECK/DEFAULT kısıtlamalarını, birincil/yabancı anahtar (primary/foreign key) ilişkilerini ve saklı yordamları içeren eksiksiz veritabanı betiği.
