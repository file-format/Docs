{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "uzantı", "dosya", "biçim", "sistem", "Sürücü", "Windows Aygıt Sürücüsü", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows Aygıt Sürücüsü",
  "description":"DRV dosya formatı ve DRV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## DRV dosyası nedir? ##

.drv uzantılı dosyalar Windows Aygıt Sürücüsüne aittir. Windows İşletim Sistemi, dahili ve harici sabit aygıtları bağlamak için bu dosyaları kullanır. DRV dosyaları, bir cihazın ve işletim sisteminin birbirine nasıl bağlandığına ilişkin talimatlar ve parametrelerden oluşur. Bu dosyalar, Windows ile düzgün çalışması için aygıt sürücülerinin yüklenmesine yardımcı olur. Ayrıca, PC'nin ana kartına veri yolu veya kablo ile bağlanan cihazlar DRV dosyaları gerektirir.


## DRV Dosya Biçimi ##

DRV dosyaları genellikle dinamik kitaplıklar ([DDL](/tr/system/dll/) dosyaları) veya [EXE](/tr/executable/exe/) dosyaları olarak paketlenir. Bu dosyalar, akıllı telefonlar gibi tüm sistem platformlarında desteklenebilir ve her platformun bu dosyaları uygun şekilde destekleyeceğinin garantisi yoktur. Ancak, .drv dosya uzantısını kullanan en yaygın cihazlardan bazıları şunlardır:

* Ses kartları
* Grafik kartları
* Yazıcılar
* Depolama aygıtları
* Ağ bağdaştırıcıları
* Bilgisayar donanımı aksesuarları

E-posta yoluyla gönderilen DRV dosyalarının açılmaması önerilir çünkü bu dosya biçimi virüsler ve diğer kötü amaçlı programlar içerir. Herhangi bir bilinmeyen DRV dosyasını açmadan önce kapsamlı bir tarama yaptığınızdan emin olun.


## DRV Örneği ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

