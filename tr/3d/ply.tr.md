{
  "date" : "2019-12-12",
  "keywords" :[ "KAT", "dosya", "uzantı", "biçim", "3D dosya biçimi" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"PLY dosya formatı ve PLY dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PLY - Çokgen 3D Dosya Biçimi",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .pl dosyası nedir?

PLY, Çokgen Dosya Biçimi, bir çokgen koleksiyonu olarak tanımlanan grafik nesneleri depolayan 3B dosya biçimini temsil eder. Bu dosya biçiminin amacı, geniş bir model yelpazesi için yararlı olacak kadar genel olan basit ve kolay bir dosya türü oluşturmaktı. PLY dosya formatı, kompakt depolama ve hızlı kaydetme ve yükleme için ASCII ve Binary formatı olarak gelir. Dosya biçimi, 3B dosya okuma desteği sağlayan farklı uygulamalar tarafından kullanılır.

PLY biçimindeki nesneler, bu öğelere eklenebilecek renk ve normal yön gibi özelliklerin yanı sıra köşeler, yüzler ve diğer öğelerden oluşan bir koleksiyon tarafından tanımlanır. Nesneyle birlikte depolanabilecek diğer özellikler şunları içerir:

* Yüzey normalleri
* doku koordinatları
* şeffaflık
* aralık veri güveni
* bir çokgenin önü ve arkası için özellikler

PLY formatı ile temsil edilen bir nesne, elle sayısallaştırılmış nesneler, modelleme uygulamalarından çokgen nesneler, menzil verileri, yürüyen küplerden üçgenler, arazi verileri ve radyosite modelleri gibi çeşitli kaynakların sonucu olabilir.

## Kısa Tarihçe

PLY formatı 1990'larda Greg Turk ve diğerleri tarafından Stanford grafik laboratuvarında geliştirildi ve bu nedenle Stanford Üçgen Formatı olarak da biliniyor. Dosya formatı o zamandan beri 1.0 sürümüne sahiptir ve daha fazla değişiklik yapılmamıştır.

## PLY Dosya Biçimi

Basit bir PLY nesnesi, nesnenin temsili için öğelerin toplanmasından oluşur. Bir köşenin (x,y,z) üçlülerinin bir listesinden ve aslında köşeler listesinin dizinleri olan yüzlerin bir listesinden oluşur. Köşeler ve yüzler, iki öğe örneğidir ve PLY dosyasının çoğunluğu bu iki öğeden oluşur. Bir nesnenin elemanlarına yeni özellikler de oluşturulabilir ve eklenebilir, ancak bunlar, bu yeni özelliklerle karşılaşıldığında eski programların bozulmaması için eklenmelidir. Bu tür özellikler, uygulamaları okuyarak da atılabilir. Ayrıca bu eleman ile yeni elemanlar oluşturulabilir ve özellikler tanımlanabilir.

### Dosya Yapısı

Bir PLY dosya biçiminin dosya yapısı aşağıdaki gibidir:

|Alan
---|
|Dosya Başlığı
|Köşe Listesi
|Yüz Listesi
|Diğer öğelerin listesi

#### Örnek Yapı

Bir PLY dosya biçiminin çeşitli bölümleri için sonraki tartışmamızda aşağıdaki örneği kullanacağız.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Dosya Başlığı

PLY dosya formatı başlığı, hem ASCII hem de ikili format için ASCII metninden oluşur. Başlık bölümünün başlangıcı ve bitişi, kat ve bitiş başlığı anahtar kelimeleriyle tanımlanır. Başlığın başlangıcında, PLY dosya formatının okuyucular tarafından tanınması için kullanılan sihirli kelime katmanı vardır. Sonraki satır, bu dosyanın sürüm numarasını gösterir. PLY dosya biçimindeki yorumlar, her yorum satırının başında yorum anahtar sözcüğüyle başlar.

#### Öğe Anahtar Kelimesi

element anahtar sözcüğü daha sonra dosyanın içinde ne olduğunu söyler. Bunu, her bir özelliğin aşağıda gösterildiği gibi kendi özellik tipine ve sırasına sahip olduğu belirli bir eleman tipi için özellikler takip eder:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Bu özel örnekte, belirli köşe öğesi, sıraları belirtilen yüzer tipte 3 özelliğe sahiptir.

#### Veri Türleri Türleri

Bir özelliğin sahip olabileceği iki tür veri türü vardır.

`Scalar`: Skaler veri türleri aşağıda gösterildiği gibidir:

|#Ad|#Tür|#Bayt Sayısı
|karakter|karakter|1
|uchar|işaretsiz karakter|1
|kısa|kısa tamsayı|2
|kısa|işaretsiz kısa tamsayı|2
|int|Tamsayı|4
|uint|işaretsiz Tamsayı|4
|kayan|tek hassasiyetli kayan nokta|4
|çift|çift duyarlıklı kayan nokta|8

`Liste`: Liste veri türünü kullanan özel bir özellik tanımları vardır. Bunun bir örneği yukarıdaki küp dosyasındandır:

"özellik listesi uchar int vertex_index"

Bu, "vertex_index" özelliğinin önce özelliğin kaç tane dizin içerdiğini belirten işaretsiz bir karakter içerdiği ve ardından o kadar tamsayı içeren bir liste içerdiği anlamına gelir. Bu değişken uzunluklu listedeki her tamsayı, bir tepe noktasının indeksidir.

## Referanslar ##

* [PLY Dosya Biçimi](http://paulbourke.net/dataformats/ply/)
* [PLY - Wikipedia Tarafından](https://en.wikipedia.org/wiki/PLY_(file_format))

