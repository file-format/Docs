{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Gömülü dil","dosya", "uzantı", "dosya formatı", "Maya 3D", "Programlama Kılavuzu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Gömülü Dil Dosya Formatı",
  "description":"MEL dosya formatı ve MEL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## .mel dosyası nedir?

.mel (Maya Gömülü Dil) uzantılı bir dosya, Autodesk Maya tarafından grafik arayüzler oluşturmak için kullanılan bir betik dilidir. Maya'nın grafik arabirimine ek olarak yürütülebilir betikler kullanarak grafik öğelerin oluşturulmasını otomatikleştirmenize olanak tanır. MEL, programlama öğrenmeden grafik arayüzler oluşturmanıza olanak tanır. Bu, yinelenen görevleri hızlandıran Makrolar ve özel eylemler oluşturarak elde edilir. Bu prosedürler ve komut dosyaları, özel modelleme, animasyonlar, dinamikler ve görev oluşturma oluşturmanıza olanak tanır. Autodesk Maya 2020, bir EML dosyasının içeriğini açmak ve görüntülemek için kullanılabilir.

## MEL Dosya Biçimi - Daha Fazla Bilgi

Bir programcının [referans kılavuzuna](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) Maya'nın dokümantasyon bölümünden geliştiriciler tarafından kullanılabilir. MEL, bir şeyleri başarmak için UINX'e benzer kabuk betik komutlarına dayanır. Komut dosyası tabanlı komutlar, onu geleneksel ve nesne yönelimli programlama (OOP) ile alakasız hale getirerek, diğer dillerdeki gibi veri yapılarının, çağırma işlevlerinin veya OOP'nin kullanılmamasına neden olur.

MEL ile ilgili bazı önemli noktalar aşağıdaki gibidir.

`Yorumlar` - MEL'deki her ifade, blok sonunda olsa bile noktalı virgülle (;) bitmelidir.

`Değerleri Döndürmek` - Bir değer döndüren bir ifade belirtmek, değeri MEL'de otomatik olarak yazdırmaz. Bunun yerine bir hataya neden olur.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Oluşturma, Düzenleme ve Silme Komutları` - Aynı komut, bir şeyler oluşturmak, bir şeyleri düzenlemek veya var olan şeyler hakkında bilgi sorgulamak için kullanılır. Ancak bir bayrak, komutun ne yaptığını (oluşturma, düzenleme veya sorgulama) denetler.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
"İşlevden Değer Döndür" - İşlev sözdizimi otomatik olarak bir değer döndürür. Komut sözdizimini kullanarak bir dönüş değeri elde etmek için, komutu ters tırnak içine almalısınız.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referanslar

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

