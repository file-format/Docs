{
  "date" : "2020-03-16",
  "keywords" :["PAT Dosyası", "Biçim", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"PAT dosya formatı ve PAT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PAT Dosya Biçimi",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## PAT dosyası nedir?

.pat uzantılı bir dosya, AutoCAD yazılımı tarafından kullanılan bir CAD dosyasıdır. PAT dosyalarını açabilen uygulamalar, bu dosyalarda saklanan tarama desenini kullanır ve bir alanın dokusu/doldurulması hakkında bilgi alır. İçerdiği desenler, çizilen nesnelere malzemenin görünümü hakkında bilgi verir. PAT dosyaları, Autodesk AutoCAD, CorelDRAW Graphics Suite ve Ketron Software gibi uygulamalarda açılabilir. PAT dosyaları JPG, PNG, BMP vb. gibi farklı görüntü formatlarına dönüştürülebilir.

## PAT Dosya Biçimi

PAT dosyaları düz metin biçiminde yazılır ve herhangi bir metin düzenleyicide açılabilir. Bu dosyalardaki tarama desenleri vektör tabanlıdır ve AutoCAD belgelerinde belirtilen sözdizimini takip eder.

Tüm desenler 0,0 noktasında başlar, desen tarama sınırını kapsayacak şekilde hesaplanır.

### Model Tanımı

Tüm desen tanımları aşağıdaki alanlardan oluşur:
* Başta bir '\*'
* Bir isim - İsimde boşluk, noktalama işareti, parantez veya eğik çizgi olamaz.
* Bir tanım

Tarama desenleri için standart biçim `<\*> şeklindedir.<name> <, açıklama>`. Ad ve açıklama virgülle ayrılır ve açıklamalar seksen karakter satır uzunluğunu aşamaz. Tarama desenleri bu bilgilerden sonra tanımlanır.

### Tarama Modeli Örnekleri
Aşağıda bir kare desen örneği verilmiştir.
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Paralelkenar desenini gösteren başka bir örnek aşağıdaki gibidir.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referanslar ##

* [Autodesk'ten Karma Kalıplar](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

