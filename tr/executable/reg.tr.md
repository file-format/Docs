{
  "date" : "2021-08-02",
  "keywords" :[ "reg dosyası", "reg dosyası biçimi", "reg dosyası nedir", "dosya", "reg örneği", "reg dosyası uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"REG dosya formatı ve REG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"REG - Windows Kayıt Defteri Dosyası",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## .reg dosyası nedir?
Bir REG dosyası, .reg uzantılı bir metin dosyasıdır. Bu dosyalar genellikle Kayıt Defterinden tipik anahtarlar dışa aktarılarak oluşturulur. Bu dosyalar ayrıca kayıt defterinin yedeği olarak da kullanılabilir (Özellikle bu adım, değişiklik yapmadan önce önemlidir!). Bazılarının bunları, bir Kayıt Defteri hacklemeyi nasıl gerçekleştireceğinizi gösteren aynı sitelerde indirilebilir dosyalar olarak kullanıma sunduğunu görebilirsiniz. Bir REG dosyası, Kayıt Defterinde manuel değişiklikler yapmak ve bu değişiklikleri dışa aktarmak için kullanışlıdır. Dosyayı biraz temizleyin ve ardından başkalarıyla paylaşın.

## REG dosya formatı
REG dosya biçimi, INI tabanlı bir sözdizimi kullanılarak Windows kayıt defterinin bazı kısımlarını dışa ve içe aktarmak için tasarlanmıştır. Windows Kayıt Defteri, Microsoft Windows işletim sistemi ve Windows kayıt defterini kullanan diğer uygulamalar için alt düzey ayarları tutan ilişkisel veya hiyerarşik bir veritabanıdır. Alternatif olarak, kayıt defteri veya Windows Kayıt Defteri, Microsoft Windows işletim sistemlerinin tüm sürümlerinde kurulu programlar ve donanımlar için bilgiler, seçenekler, ayarlar ve diğer değerlerden oluşur diyebiliriz.
### REG dosyasının sözdizimi
REG dosyası sözdiziminin parçası olarak bazı temel öğeler şunlardır:
- **RegistryEditorVersion**: Örneğin, Windows 2000, Windows XP ve Windows Server 2003 için "Windows Kayıt Defteri Düzenleyicisi Sürüm 5.00".
- **Boş satır**: Yeni bir kayıt defteri yolunun başlangıcını tanımlar.
- **RegistryPathx**: İçe aktardığınız ilk değeri tutan alt anahtarın yolu.
- **DataItemNamex**: İçe aktarmak istediğiniz veri öğesinin adı.
- **DataTypex**: Kayıt defteri değeri için veri türü.

Anahtarlar, aşağıdaki söz dizimi kullanılarak .reg dosyalarında depolanır:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
"Değer Adı" yerine "@" kullanarak bir anahtarın Varsayılan Değerini düzenleyebilirsiniz:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Örnek
İşte bir REG dosyası örneği
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Referanslar

* [Windows Kayıt Defteri - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Registry)
* [Bir .reg dosyası kullanılarak kayıt defteri alt anahtarları ve değerleri nasıl eklenir, değiştirilir veya silinir](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- kayıt defteri-alt anahtarları-ve-değerleri-by-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


