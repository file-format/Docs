{
  "date" : "2019-10-11",
  "keywords" :[ "xpm dosyası", "xpm dosya biçimi", "xpm dosyası nedir", "dosya", "xpm örneği", "xpm dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap Dosya Biçimi",
  "description":"XPM dosya formatı ve XPM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## XPM dosyası nedir?

.xpm uzantılı bir dosya, X Windows Sistemi tarafından kullanılan bir görüntü dosyası biçimidir. Saydam pikselleri destekler ve genellikle simge piksel haritaları oluşturmayı hedefler. Tek renkli, gra ölçekli ve renkli Pixmap verilerini destekler. Bunlar elle düzenlenebilir olacak şekilde tasarlanmıştır ve [C](/tr/programming/c/) koduna dahil edilebilir. Bu amaçla, XPM dosyaları düz metin dosyası biçimindedir ve C programlama dili sözdizimini takip eder. XPM dosyaları, aşağıdakiler gibi çeşitli resim görüntüleme uygulamalarıyla açılabilir:
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView ve Canvas X.

## XPM Dosya Biçimi

XPM dosya formatı, bunların C ve C++ programlarına entegre edilmesi için C sözdizimini kullanır. Aşağıdaki altı farklı bölümden oluşmaktadır.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Bölümler aslında aşağıdaki gibi bir dizi dizidir.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Her bölümün ayrıntıları aşağıdadır.

`<Values> ` - Bu bölüm, 10 tabanında olan ve şuna karşılık gelen dört veya altı tamsayı içeren bir dizedir:

* pixmap genişliği ve yüksekliği
* Renk sayısı
* piksel başına karakter sayısı
* isteğe bağlı etkin nokta koordinatları ve XPMEXT etiketi

`<Colors> ` - Bu bölüm, renk sayısı kadar dize içerir. Her dize aşağıdaki gibidir:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Bu bölüm şunlardan oluşur:<height> dizeleri ve<width> \*<chars_per_pixel> karakterler. Her<chars_per_pixel> uzunluk dizesi, önceden tanımlanmış gruplardan biri olmalıdır.<Colors> bölüm.

`<Extension> ` - Uzantı bölümü boş değilse etiketlenmelidir.<Values> bölüm. Birkaç taneden oluşabilir<Extension> aşağıdaki iki türden olabilecek alt bölümler:

* aşağıdaki şekilde oluşan bağımsız bir dize: XPMEXT<extension-name><extension-data>
* veya birkaç diziden oluşan bir blok:XPMEXT<extension-name><related extension-data composed of several strings>

## Referanslar

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM Kılavuzu](http://www.xfree86.org/current/xpm.pdf)

