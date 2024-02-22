{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DSN dosyalarını oluşturabilen ve açabilen DSN dosya formatı ve API'ler hakkında bilgi edinin.",
  "title" : "DSN Dosya Formatı - Veritabanı Kaynak Adı Dosyası",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-tr",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## DSN dosyası nedir?

DSN, Veri Kaynağı Adı anlamına gelir ve veritabanı bağlantı bilgilerini depolamak için kullanılan bir dosya formatıdır. DSN dosyaları genellikle ODBC (Açık Veritabanı Bağlantısı) ile birlikte kullanılır ve belirli bir veritabanına bağlanmak için sunucu adı, kullanıcı adı ve şifre gibi gerekli bilgileri sağlayarak bu veritabanına kolay erişim sağlar. Dosya genellikle düz metin halindedir ve bir metin düzenleyici kullanılarak oluşturulabilir ve düzenlenebilir. Windows, Linux ve Mac gibi çeşitli işletim sistemlerinde kullanılabilir.

## DSN dosyası nasıl oluşturulur?

DSN dosyası oluşturma yöntemi, işletim sistemine ve mevcut araçlara göre değişiklik gösterebilir. Aşağıdaki adımlar, Windows sisteminde bir DSN dosyası oluşturma sürecine genel bir bakış sağlar.

1. Başlat menüsünde ODBC Veri Kaynakları ifadesini arayarak ODBC Veri Kaynağı Yöneticisini açın.
2. Sistem DSN sekmesini seçin ve Ekle düğmesini tıklayın.
3. Bağlanmak istediğiniz veritabanı için uygun sürücüyü seçin ve Sona tıklayın.
4. Veritabanına bağlanmak için sunucu adı, kullanıcı adı ve şifre gibi gerekli bilgileri girin.
5. DSN dosyasını kaydetmek için Tamamı tıklayın.

Alternatif olarak, .dsn uzantılı bir düz metin dosyası oluşturarak ve gerekli bağlantı bilgilerini şu biçimde girerek manuel olarak bir DSN dosyası oluşturabilirsiniz:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Daha sonra bu dosyanın yolunu, veritabanına bağlanmak için kodunuz/komut dosyanızda DSN olarak kullanabilirsiniz.

## DSN dosyasını açan programlar

DSN dosyası, sunucu adı, kullanıcı adı ve şifre gibi bir veritabanına bağlanmak için kullanılan bilgileri saklayan düz metin dosyasıdır. Belirli bir veritabanına kolay erişim sağlamak için genellikle ODBC (Açık Veritabanı Bağlantısı) ile birlikte kullanılır.

Bir DSN dosyasının içeriğini açmak ve görüntülemek için Notepad, Sublime Text, Atom vb. gibi herhangi bir metin düzenleyiciyi kullanabilirsiniz. Bu programlar, DSN dosyasını açmanıza ve içinde saklanan bağlantı bilgilerini görüntülemenize olanak tanır.

Ancak DSN dosyasını bir veritabanına bağlanmak ve SELECT, INSERT, UPDATE, DELETE vb. işlemleri yürütmek için kullanmak için Python, Java, C# gibi bir programlama dili veya Microsoft Access gibi bir veritabanı yönetim aracı gibi ODBC desteği olan bir program , SQL Server Management Studio gereklidir. Bu programlar, veritabanına bağlanmak ve istenen işlemi gerçekleştirmek için DSN dosyasındaki bilgileri kullanabilir.

## Referanslar

* [DSN (Veri Kaynağı Adı) nedir?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



