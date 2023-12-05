{
"tarih": "2023-06-12",
  "keywords": [
"bak",
"bak dosyası",
"Microsoft SQL Server Veritabanı Yedekleme",
"bak dosyası nedir",
"bak dosyası nasıl açılır",
"dosya",
"bak dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK Dosya Formatı - Microsoft SQL Server Veritabanı Yedeklemesi",
  "description":"BAK SQL Server Yedekleme formatı ve BAK dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"sonmod": "2023-06-12"
}

## BAK dosyası nedir?

Microsoft SQL Server bağlamında ".bak" dosyası, SQL Server veritabanının kopyalarını depolamak için kullanılan bir yedekleme dosyası biçimidir. Bu dosyalar, şeması, verileri ve diğer ilgili bilgiler de dahil olmak üzere, veritabanının belirli bir andaki anlık görüntüsünü içerir. Bunlar, SQL Server'ın yerleşik yedekleme ve geri yükleme işlevi kullanılarak oluşturulur ve birkaç önemli amaca hizmet eder:

1. **Veri Kurtarma:** .bak dosyaları, veri kaybı, bozulması veya diğer sorunlar durumunda veritabanını kurtarmak için bir araç sağlar. Bir veritabanını .bak dosyasından geri yükleyerek, onu önceki durumuna döndürebilir, kesinti süresini ve veri kaybını en aza indirebilirsiniz.

2. **Taşıma ve Klonlama:** Yedekleme dosyaları genellikle veritabanlarını sunucular arasında taşımak veya test, geliştirme veya raporlama amacıyla veritabanlarının kopyalarını oluşturmak için kullanılır. Veritabanlarını ortamlar arasında taşımak için tutarlı ve etkili bir yol sunarlar.

3. **Belirli Bir Noktaya Kurtarma:** SQL Server, .bak dosyalarını kullanarak belirli bir noktaya kurtarma gerçekleştirmenize olanak tanır. Bu, bir veritabanını zaman içinde belirli bir ana geri yükleyebileceğiniz anlamına gelir; bu, mevzuata uygunluk veya veri denetimi açısından çok önemli olabilir.

4. **Olağanüstü Durum Kurtarma:** .bak dosyaları olağanüstü durum kurtarma planlamasının kritik bir parçasıdır. Verilerinizin güvende olmasını ve donanım arızaları, doğal afetler veya diğer yıkıcı olaylar durumunda hızlı bir şekilde geri yüklenebilmesini sağlarlar.

## SQL Server'da bir .BAK dosyası oluşturun

SQL Server'da bir .bak dosyası oluşturmak için genellikle SQL Server Management Studio (SSMS) veya BACKUP DATABASE veya BACKUP LOG gibi Transact-SQL (T-SQL) komutlarını kullanırsınız. T-SQL kullanarak nasıl veritabanı yedeği oluşturabileceğinize dair basitleştirilmiş bir örnek:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## SQL Server'da bir .BAK dosyasını geri yükleme

Bir veritabanını .bak dosyasından geri yüklemek için RESTORE DATABASE komutunu kullanabilirsiniz:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## BAK dosyası SQL Server'da nasıl açılır?

Bir ".bak" dosyasında saklanan verileri açmak ve bunlara erişmek için genellikle dosyayı bir Microsoft SQL Server örneğine geri yüklemeniz gerekir. SQL Server Management Studio'yu (SSMS) kullanarak bir ".bak" dosyasını açmak için genel adımlar şunlardır:

1. **SQL Server Management Studio'yu başlatın**: Bilgisayarınızda SSMS'yi açın. Bunu genellikle Başlat Menünüzde veya "SQL Server Management Studio"yu arayarak bulabilirsiniz.

2. **SQL Server Örneğine Bağlan**: SSMS'de, veritabanını geri yüklemek istediğiniz SQL Server örneğine bağlanın. Bu işlemi gerçekleştirmek için gerekli izinlere ihtiyacınız olacak.

3. **Veritabanını Geri Yükle**:

A. Sol taraftaki Nesne Gezgini bölmesinde SQL Server örneğini genişletin.

B. "Veritabanları" düğümünü genişletin.

C. "Veritabanları"na sağ tıklayın ve "Veritabanını Geri Yükle"yi seçin.

4. **Kaynak ve Hedefi Belirtin**:

A. "Veritabanını Geri Yükle" iletişim kutusunun "Genel" sayfasında, "Veritabanına" alanına yeni veritabanı için bir ad girin. Bu, geri yüklenen veritabanının adı olacaktır.

B. "Kaynak" bölümünde, yedekleme ortamı türü olarak "Cihaz"ı seçin.

C. Geri yüklemek istediğiniz ".bak" dosyasına göz atmak için "Cihaz" alanının yanındaki "..." düğmesini tıklayın.

D. Açmak istediğiniz ".bak" dosyasını seçin ve "Tamam"ı tıklayın.

5. **Geri Yükleme Seçenekleri**: Gerektiğinde geri yükleme seçeneklerini inceleyin ve yapılandırın. Mevcut bir veritabanının üzerine yazılıp yazılmayacağını belirtebilir, kurtarma seçeneklerini ayarlayabilir ve daha fazlasını yapabilirsiniz. Bu seçenekleri gereksinimlerinize göre ayarladığınızdan emin olun.

6. **Geri Yüklemeyi Başlatın**: Geri yükleme seçeneklerini yapılandırdıktan sonra, "Veritabanını Geri Yükle" iletişim kutusunda "Tamam" düğmesini tıklayın. SQL Server geri yükleme işlemine başlayacaktır.

7. **Geri Yüklenen Veritabanına Erişim**: Başarılı bir geri yükleme işleminden sonra, geri yüklenen veritabanına SQL Server Management Studio'da diğer herhangi bir veritabanı gibi erişebilirsiniz. Sorguları çalıştırabilir, tabloları görüntüleyebilir ve veritabanındaki verilerle çalışabilirsiniz.

## Diğer BAK dosyaları

**.bak** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Veri tabanı**
- [BAK - Veritabanı Yedekleme Dosyası](/tr/database/bak/)
- [BAK - Hızlı Sayfa Yasası! Veritabanı Yedeklemesi](/tr/database/bak-act/)

**Oyun**
- [BAK - Terraria Dünyası veya Oyuncu Yedeklemesi](/tr/game/bak-terraria/)

**Çeşitli**
- [BAK - Yedekleme Dosyası](/tr/misc/bak-backup/)
- [BAK - Chromium Yer İmleri Yedeklemesi](/tr/misc/bak-chromium/)
- [BAK - Final 2012 Puan Yedeklemesi](/tr/misc/bak-finale/)
- [BAK - MobileTrans Yedeklemesi](/tr/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Projesi Yedeklemesi](/tr/misc/bak-vegas/)

**Ayarlar**
- [BAK - Holo Başlatıcı Yedeği](/tr/settings/bak-holo/)

## Referanslar
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
