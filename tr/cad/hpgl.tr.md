{
  "date" : "2020-07-28",
  "keywords" :["HPGL", "Dosya Formatı", "Aç", "Oku", "Oluştur", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"HPGL dosya formatı ve HPGL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"HPGL Dosya Formatı - Dosya Formatı Uzmanlarından Öğrenin!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## HPGL dosyası nedir?

Bir HPGFL(Hewlett-Packard Graphics Language) dosyası, HP tarafından geliştirilen çizici denetimi için yönerge seti içerir. HP çiziciler, kağıda vektör ve raster içeriği çizmek ve yazdırmak için bu dosyayı kullanır.

### HPGL Komutu

Bir HPGL komutu aşağıdakilerden oluşur.
* İki karakterden oluşan alfabenin bir komut bölümü
* Bir parametre bölümü
* Terminatör bölümü

Birden fazla parametre olması durumunda dosyadaki her parametre bir ayırıcı ile ayrılmalıdır.

### HPGL Komut Örneği

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinat sistemi

Koordinat sistemleri, herhangi bir belirli konumu bulmak için 2 boyutlu ölçüm göstergelerinden oluşur. HPGL, bu amaçla hem Plotter koordinatını hem de kullanıcı koordinat sistemini kullanır.

#### Çizici Koordinat Sistemi

Bu koordinat sistemi, çizici hareketine dayalı çizimleri çizmek için kullanılır. Minimum çizici hareketinin tipik bir XY birimi 0,025 mm'dir. Olası çizim aralığı çizici çeşitlerine göre değişir.

#### Kullanıcı koordinat sistemi

Kullanıcı tarafından belirlenen koordinat sistemi, ölçek ve orijin kullanılarak ayarlanabilir. Bunlar, IP komutu ve SC komutu kullanılarak çizici koordinatlarına dönüştürülür. Bu dönüştürme gerçekleştirilmezse çizici sistem koordinatları varsayılan olarak kullanılır.

## HPGL Dosya Biçimi
HPGL dosyaları ASCII (metin dosyası) biçimindedir ve birkaç kurulum komutuyla başlar. Bu, çizim için çizici için belirli parametreleri ayarlar. Tipik bir HPGL dosyası aşağıdaki gibi görünür.

|Komut|Anlam
---|---|
|IN;|başlat, bir çizim işini başlat|
|IP;|ölçeklendirme noktalarını (P1 ve P2) varsayılan konumlarına ayarlayın|
|SP1;|kalem 1'i seçin|
|PU0,0;|Kalemi Kaldırın ve sonraki eylem için başlangıç noktasına gidin|
|PD100,0,100,100,0,100,0,0;|Pen Down'a koyun ve aşağıdaki konumlara gidin (sayfanın etrafına bir kutu çizin)|
|PU50,50;|Kalem Açın ve X,Y koordinatlarına taşıyın 50,50|
|CI25;|yarıçapı 25 olan bir çember çiz|
|SS;|standart karakter setini seçin|
|DT*,1;|metin sınırlayıcıyı yıldız olarak ayarlayın ve bunları yazdırmayın ("doğru" anlamına gelen 1)|
|PU20,80;|kalemi kaldırın ve 20,80'e geçin|
|LBMerhaba Dünya*;|bir etiket çiz|

## Referanslar
* [Wikipedia'dan HPGL](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL Başvuru Kılavuzu](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

