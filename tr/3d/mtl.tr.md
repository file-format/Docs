{
"tarih":"2023-10-11",
   "keywords":[
"mtl",
"mtl dosyası",
"mtl obj malzeme şablon kitaplığı dosyası",
"mtl dosyası nasıl açılır",
"dosya",
"mtl dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"MTL Dosya Formatı - OBJ Malzeme Şablonu Kitaplığı Dosyası",
   "description":"MTL OBJ Malzeme Şablonu Kitaplığı dosya formatı ve MTL dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## .MTL dosyası nedir?

**Malzeme Şablon Kütüphanesi**'nin kısaltması olan MTL dosyası, 3D bilgisayar grafikleri ve modellemede kullanılan yardımcı dosya formatıdır. Genellikle 3D modelleri ve bunlarla ilişkili malzemeleri ve dokuları depolamak için kullanılan yaygın format olan **Wavefront OBJ dosya formatı** ile ilişkilendirilir.

## Malzeme Şablonu Kütüphanesi

MTL dosyaları hakkında önemli bilgiler:

1. **Malzeme Tanımları**: ".mtl" dosyası, ilgili OBJ dosyasındaki 3B nesnelere uygulanan malzemelerin tanımlarını içerir. Her malzeme tanımı renk, parlaklık, şeffaflık ve doku haritaları gibi çeşitli özellikleri belirtir.
    





2. **Metin Tabanlı Format**: ".mtl" dosyaları genellikle düz metin dosyalarıdır; bu, bunların metin düzenleyiciyle kolayca düzenlenebileceği anlamına gelir. Her malzeme tanımı bir takım ifadelerden oluşur ve bu ifadeler malzemenin özelliklerini tanımlar.
    





3. **Doku Eşleme**: ".mtl" dosyasının temel işlevlerinden biri, dokuların (görüntü dosyalarının) 3D modelin yüzeylerine nasıl eşlendiğini tanımlamaktır. Doku dosyasının yolunu ve modele nasıl sarılması veya uygulanması gerektiğini belirtir.
    





4. **Örnek MTL İfadeleri**: Bir ".mtl" dosyasında bulabileceğiniz bazı örnek ifadeleri burada bulabilirsiniz:
    





- `newmtl MalzemeAdı`: Bu, "MalzemeAdı" adındaki yeni malzemeyi tanımlar.
- `Ka rgb`: Malzemenin ortam rengi, RGB değerlerinde belirtilir.
- `Kd rgb`: Malzemenin yaygın rengi, RGB değerlerinde belirtilir.
- `Ks rgb`: Malzemenin RGB değerlerinde belirtilen özel rengi.
- 'Ns değeri': Malzemenin parlaklığı veya aynasal üssü.
- `map_Kd doku dosyası.jpg`: Malzeme için dağınık doku haritasını belirtir.
5. **Birden Fazla Malzeme**: Bir OBJ dosyası birden fazla malzemeye referans verebilir ve her malzeme ".mtl" dosyası içinde tanımlanır. Bu, farklı parçalara uygulanan farklı malzemelerle karmaşık 3 boyutlu modellerin oluşturulmasına olanak tanır.
    





6. **Uyumluluk**: ".mtl" dosyaları, 3D modelleme yazılımı ve işleme motorları tarafından geniş çapta desteklenir; bu, 3D modellerin ve materyallerinin farklı yazılım uygulamaları arasında aktarılmasını mümkün kılar.

## MTL dosyası nasıl açılır?

MTL dosyaları metin tabanlı dosyalar olduğundan herhangi bir metin düzenleyiciyle açılabilirler.

- Not Defteri (Windows)
- Not Defteri++ (Windows)
- Visual Studio Kodu
- Yüce metin
- Atom
- TextEdit (macOS)

MTL dosyalarını açan veya referans veren programlar şunları içerir:

-AdobePhotoshop2023
- Autodesk Maya 2023
-MeshLab
- Çita3D

**Alt Tür:** 3D Görüntü Dosyaları

## Referanslar
* [Wavefront .obj dosyası](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

