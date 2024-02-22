{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE Dosyası - .gcode dosyası nedir ve nasıl açılır?",
   "description":"GCODE dosya formatı ve GCODE dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-tr",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## GCODE dosyası nedir?

**GCODE dosyası**, bilgisayarlı takım tezgahlarını ve 3D yazıcıları kontrol etmeye yönelik talimatlar içeren düz bir metin dosyasıdır; G kodu veya Geometrik Kod, **CNC (Bilgisayar Sayısal Kontrolü)** makinelerinin hareketlerini ve eylemlerini kontrol etmek için kullanılan bir dildir; CNC makineleri arasında freze makineleri, torna tezgahları, yönlendiriciler ve 3D yazıcılar bulunur.

G kodu komutları, genellikle harflerden ve rakamlardan oluşan belirli bir sözdizimiyle yazılır; her komut makineye, takımı belirli bir konuma hareket ettirme, takımı değiştirme veya hızı ayarlama gibi belirli eylemleri gerçekleştirme talimatını verir.

G kodu genellikle **CAM (Bilgisayar Destekli Üretim)** yazılımı tarafından oluşturulur; CAM yazılımı 3D modeli veya 2D tasarımı alır ve ilgili takım yollarını ve G kodu talimatlarını oluşturur; G kodu dosyası daha sonra yürütülmek üzere CNC makinesine veya 3D yazıcıya yüklenir.

G kodu dosyaları genellikle .nc veya .gcode dosya uzantısına sahiptir; örneğin, program.nc veya print.gcode.

## GCODE Dosya Yapısı:

GCODE dosyaları, her satırı belirli bir komut içeren düz metin dosyalarıdır; Bu komutlar, makinenin hareketinin kontrol edilmesinden sıcaklığın, hızın ve bir nesnenin imalatı için önemli olan diğer parametrelerin ayarlanmasına kadar uzanır.

GCODE'un sözdizimi harf ve sayıların birleşimini içerir; her biri farklı eylemi veya parametreyi temsil eder; ortak komutlar arasında sırasıyla hareket için G0 ve G1, iş mili kontrolü için M3 ve M5 ve hız ve ilerleme hızı ayarları için S ve F bulunur.

## GCODE Oluşturma:

**Simplify3D** ve **Slic3r** gibi dilimleme yazılımları, Bilgisayar Destekli Tasarım (CAD) çizimlerini GCODE'a çevirir; CAD yazılımı, daha sonra STL gibi formatlarda dışa aktarılan 3 boyutlu modeller oluşturmak için kullanılır; dilimleme yazılımı bu modelleri alır ve katman yüksekliği, yazdırma hızı ve sıcaklık ayarları gibi ayrıntıları belirten GCODE dosyası oluşturur.

## GCODE Örneği

CNC makinesini hareket ettirmek için G kodunun basit bir örneği:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## GCODE dosyası nasıl açılır?

Bir G kodu dosyasını açmak için ihtiyaçlarınıza bağlı olarak farklı yazılım türlerini kullanabilirsiniz.

3D yazıcı için G-code oluşturduysanız; 3D yazıcınızla birlikte gelen yazılımı veya özel dilimleme yazılımını kullanarak açabilirsiniz; örnekler arasında **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** veya **Repetier-Host** yer alır; bu programlar genellikle G kodunu yüklemenize ve görselleştirmenize olanak tanıyan kullanıcı dostu bir arayüze sahiptir.

GCODE dosyaları düz metin olduğundan bunları herhangi bir metin düzenleyiciyle açabilirsiniz; yaygın metin düzenleyicileri arasında **Notepad (Windows'ta)**, **TextEdit (macOS'ta)** veya **Gedit (Linux'ta)** yer alır; G kodu dosyasına **sağ tıklayın**, **Birlikte aç** seçeneğini seçin ve bir metin düzenleyici seçin.

