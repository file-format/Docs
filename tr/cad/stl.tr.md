{
  "date" : "2020-03-16",
  "keywords" :[ "STL Dosyası", "Biçim", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"STL dosya formatı ve STL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"STL Dosya Biçimi",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## STL dosyası nedir?

Stereolitrografinin kısaltması olan STL, 3 boyutlu yüzey geometrisini temsil eden değiştirilebilir bir dosya formatıdır. Dosya formatı, hızlı prototipleme, 3D baskı ve bilgisayar destekli üretim gibi çeşitli alanlarda kullanım alanı bulur. Bir yüzeyi, her bir yüzün dikey bir yön ve üçgenin köşelerini temsil eden üç nokta ile tanımlandığı, yüzler olarak bilinen bir dizi küçük üçgen olarak temsil eder. Ortaya çıkan veriler, imalatçı tarafından oluşturulacak 3B şeklin enine kesitini belirlemek için uygulamalar tarafından kullanılır. Renk, doku veya diğer yaygın [CAD](/tr/cad/) model niteliklerinin temsili için STL dosya biçiminde hiçbir bilgi yoktur.

## Kısa Tarih ##

STL dosya formatının gelişimi 1987 yılına dayanmaktadır. 3D Systems tarafından ticari 3D yazıcılarda kullanılmak üzere geliştirilmiştir. STL 2.0 olarak bilinen STL dosya formatının revize edilmiş bir versiyonu, 2009 yılında dosya formatındaki güncellemelerle önerildi.

## Dosya Biçimi Özellikleri ##

Bir STL dosyası, yüzleri kullanan bir yüzey geometrisini temsil eder. Yüzler, bir 3B nesnenin yüzeyini tanımlar ve benzersiz bir şekilde, uzunluğu 1.0 olan üçgene dik bir çizgi olan normal bir birim ve üç köşe ile tanımlanır. Normal olarak her bir yüz için saklanan toplam 12 sayı vardır ve her tepe noktası, her biri üç koordinatla belirtilir. StL dosyası herhangi bir ölçek bilgisi içermez; koordinatlar isteğe bağlı birimlerdedir.

STL dosya formatının özellikleri aşağıdaki iki açıdan incelenebilir.

### Yön Yönelimi ###

Bir yüzün oryantasyonu, birim normalin yönü ve köşelerin listelenme sırası ile belirlenir. Yüzeylerin oryantasyonu aşağıdaki gibi iki şekilde belirtilir:

* Normalin yönü dışa doğrudur.
* Köşeler, sağ el kuralına uyularak dışarıdan saat yönünün tersine sıralanır.

### Vertex'ten Vertex'e Kural ###

Bu kurala göre, her üçgen komşu üçgenlerin her biri ile iki köşe paylaşır. Bu nedenle, bir üçgenin köşesi başka bir üçgenin kenarında olamaz.

## Dosya formatları ##

STL, kompakt dosya formatı için ASCII'nin yanı sıra İkili gösterimlerde mevcuttur.

### STL ASCII Formatı ###

STL dosya formatının ASCII versiyonu düz ASCII ile yazılmıştır. Ancak dosya formatı, boyutunun büyük olması nedeniyle kullanım için tercih edilen format olarak seçilmemiştir. Bir ASCII STL dosyasının sözdizimi aşağıdaki gibidir:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Kalın yazılmış sözcükler, her zaman küçük harf olması gereken anahtar sözcükleri temsil eder. İtalik semboller, kullanıcı tanımlı değerlerle değiştirilecek olan değişkenlerdir. **Faset normal** ve **vertex** satırlarındaki sayısal veriler, örneğin 1.23456E+789 gibi tek duyarlıklı değişkenlerdir. Bir **faset normal** koordinatının başında bir eksi işareti olabilir; **vertex** koordinatı olmayabilir.

### STL İkili Biçim ###

İkili biçim, IEEE tamsayı ve kayan noktalı sayısal gösterimi kullanır. Dosya formatı aşağıdaki gibi temsil edilir:

|Alan|Bilgi|
---|---|
|Başlık|80 karakter|
|Üçgen Sayısı|4 bayt küçük endian işaretsiz tamsayı|
|Her üçgen için veriler|12 adet 32 bit kayan noktalı sayı|

Dosya biçiminin daha ayrıntılı bir görünümü aşağıda gösterildiği gibidir.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referanslar ##

* [STL Formatı](http://www.fabbers.com/tech/STL_Format)
* [STL - Wikipedia'dan](https://en.wikipedia.org/wiki/STL_(file_format))

