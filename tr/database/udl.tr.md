{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "uzantı", "udl dosyası", "udl dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "udl dosyası nedir" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"UDL dosya biçimi ve UDL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"UDL - Microsoft Evrensel Veri Bağlantısı Dosyası",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## UDL dosyası nedir?
.udl uzantılı dosya Microsoft Universal Data Link dosyası olarak adlandırılır; bağlantı özniteliklerinin belirtilmesi; veritabanıyla bağlantı kurmak için Windows uygulamaları tarafından kullanılır. UDL dosyası, bir OLE DB veri kaynağı için bağlantı dizesini içerir; kullanıcı adı ve şifre ve temel bağlantı dizesi özellikleri ile. Özellikleri bir bağlantı dizesinde doğrudan elle belirtmekten kaçınmak için, alternatif olarak bağlantı bilgilerini bir .udl dosyasına kaydetmek için bir Veri Bağlantısı Özellikleri iletişim kutusu kullanılabilir.

## UDL Dosya Biçimi
Temel olarak, bir UDL (Evrensel Veri Bağlantısı) dosyası, belirli niteliklere veya özelliklere sahip bir veritabanı bağlantı dizesinden oluşan basit bir metin dosyasıdır. UDL dosyası oluşturulduktan sonra, bağlantıyı doğrulamak için SQL Server Management Studio kullanılarak test edilebilir.

### Bağlantı dizesi özellikleri
Uygun bağlantıyı sağlamak için bir UDL'de aşağıdaki özellikler ayarlanabilir:

- **Sunucu Adı**: erişmek istediğiniz veritabanının bulunduğu sunucunun konumu.
- **Kimlik Doğrulama Seçenekleri**
- **Windows Kimlik Doğrulaması**: Geçerli olarak oturum açmış kullanıcının Windows hesabı kimlik bilgilerini kullanarak SQL Server'da kimlik doğrulama.
- **SQL Server Kimlik Doğrulaması**: Oturum açma kimliği ve parola kullanılarak kimlik doğrulama.
- **Active Directory - Integrated**: Azure Active Directory kimliğiyle tümleşik kimlik doğrulaması; SQL Server'da Windows kimlik doğrulaması için de kullanılabilir.
- **Active Directory - Parola**: Azure Active Directory kimliğiyle Kullanıcı Kimliği ve parola kimlik doğrulaması.
- **Active Directory - MFA destekli evrensel**: Azure Active Directory kimliğiyle etkileşimli kimlik doğrulama.
- **Active Directory - Hizmet Sorumlusu**: Azure Active Directory hizmet sorumlusu ile kimlik doğrulama.
- **Sunucu SPN'si**: Güvenilir bir bağlantı kullanıyorsanız, sunucu için bir hizmet asıl adı (SPN) belirleyebilirsiniz.
- **Kullanıcı adı**: Veri kaynağında oturum açtığınızda kimlik doğrulama için kullanılacak Kullanıcı Kimliğini yazın.
- **Parola**: Veri kaynağında oturum açtığınızda kimlik doğrulama için kullanılacak parolayı yazın.
- **Boş parola**: İşaretlendiğinde, belirtilen sağlayıcının bağlantı dizesinde boş bir parola kullanmasını sağlar.
- **Parolayı kaydetmeye izin ver**: Parolanın bağlantı dizesiyle kaydedilmesine izin verir.
- **Veriler için güçlü şifreleme kullanın**: Bağlantı üzerinden iletilen veriler şifrelenir.
- **Güven sunucusu sertifikası**: Sunucunun sertifikası doğrulanacaktır.
- **Veritabanı**: Erişmek istediğiniz veritabanı adı.
- **Attach a database file as an database name**: Eklenebilir bir veritabanı için birincil dosyanın adını belirtir.

## Referanslar ##

* [Microsoft Veri Erişim Bileşenleri](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Evrensel Veri Bağlantısı (UDL) yapılandırması](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

