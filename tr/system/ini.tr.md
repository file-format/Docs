{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "uzantı", "dosya", "biçim", "sistem", "Başlatma", "dizin uzantısı", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Başlatma Dosyası Biçimi",
  "description":"INI dosya formatı ve INI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## INI dosyası nedir? ##

Bir INI dosyası, nitelikleri bir çerçeve ve dilbilgisi içinde düzenleyen özellikler ve bölümler için ortak anahtarlar içeren bilgisayar programları için bir mesaj yapılandırma belgesidir. Bu sistem dosyası biçimi yapılandırma belgeleri, adlarını MS-DOS işletim sisteminin başlatma anlamına gelen dizin uzantısı INI'den alır. Bu yazılım kurulum biçimini popüler hale getirdi. Diğer yazılım uygulamalarındaki birçok program, biçim birçok yapılandırma durumunda resmi olmayan bir standart oluştursa da, CONF ve [CFG](/tr/system/cfg/) gibi çeşitli dosya adı eklemeleri kullanır.

## INI Dosyalarının Kısa Tarihi##

Başlangıçta, Windows'un temel program yapılandırma tekniği, her satırda önemli bir çift bulunan ve bölümlere ayrılmış metin satırlarından oluşan bir metin dosyası formatıydı. Aygıt sürücüleri, yazı biçimleri ve başlatıcıların tümü bu biçimde saklanıyordu. Bireysel ayarlar da genellikle uygulamalar tarafından INI dosyalarında depolanırdı.
Biçim, Windows 3.1x'e kadar 16 bit Microsoft Windows platformlarında destekleniyordu. Windows 95'ten başlayarak Microsoft, geliştiricileri yapılandırma için INI dosyaları yerine Windows Kayıt Defterini kullanmaya teşvik etmeye başladı.

## INI Dosyası - Dosya Biçimi Özellikleri

### Tuşlar/Özellikler ###

Anahtar/özellik, bir INI dosyasının en temel öğesidir. Eşittir simgesi (=), her anahtarın adını ve değerini ayırır. Eşittir işaretinin solunda adın görüntülendiği yer bulunur. Eşittir simgesi ve noktalı virgül, Windows sisteminde gizli harflerdir, bu nedenle anahtarda kullanılamaz. Değerde herhangi bir karakter kullanılabilir.

```
name=value
```

### Bölümler ###

Bölüm açıklaması, kendi satırında köşeli parantez ([]) içinde görünür. Bölüm tanımından sonra, tüm anahtarlar o bölüme bağlanır. Bölümler, bir sonraki bölüm atamasında veya belgenin sonunda biter; belirli bir "bölüm sonu" ayırıcısı yoktur. Bölümler istiflenemez; yalnızca bir kez adlandırılabilirler ve bağlantılı olmaları gerekmez.

```
[section]
a=a
b=b
```

### Özellikleri değiştirme ###

INI dosya biçiminin dünya çapında kabul görmüş bir tanımı yoktur. Birçok bilgisayar uygulaması, daha önce belirtilenlere ek işlevler içerir. Aşağıdaki liste, herhangi bir bireysel programa dahil edilebilecek veya edilmeyebilecek bazı ortak özellikleri içermektedir.

* Yorumlar
* Kaçış karakterleri
* Yinelenen isimler


## INI Örneği ##

Örnek INI dosyası aşağıdaki gibi görünür:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Referans ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

