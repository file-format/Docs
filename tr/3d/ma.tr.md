{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma dosyası", "ma dosya biçimi", "dosya biçimi", "3d","ma dosyası indirme", ".ma dosyası", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"MA dosya formatı ve MA dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"MA Dosya Biçimi",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## MA dosyası nedir?

.ma uzantılı bir dosya, Autodesk Maya uygulaması ile oluşturulmuş bir 3D proje dosyasıdır. Dosya hakkında bilgi belirtmek için geniş bir metinsel komut listesi içerir. Bir dosyanın bozulması durumunda komutlarla ilgili sorunları düzeltmek için bir **.ma dosyası** herhangi bir metin düzenleyicide açılıp düzenlenebilir. Bu dosyalar, geometri, ışıklandırma, animasyon ve işleme gibi 3B Sahne bilgilerini tanımlamaya yönelik bilgiler içerir.

## MA Dosya Biçimi

MA dosyaları, diske ikili dosya biçiminde kaydedilen MB dosyalarının aksine ASCII metin biçiminde diske kaydedilir. MA dosya biçimi için ayrıntılı bir referans [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) içinde mevcuttur ve başvurulabilir geliştiricinin referansı için.

### MA Dosya Başlığı

MA dosya başlığı, dosyanın oluşturulma bilgilerini ve değiştirilme tarihini veren bir yorum bölümüyle başlar. Maya dosya okuyucuları, yalnızca bilgi amaçlı kullanıldığından bu bloğu yok sayar. Yine de bir başlık ilk altı karakterle "//Maya" olarak başlamalıdır.

ASCII dosya başlığı aşağıdaki gibi görünür.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Dosya Referansları

Bir .ma dosyasının dosya başvuruları bölümü, bu dosyada başvurulan diğer tüm Maya dosyaları hakkında bilgi içerir. Başvurulan her dosya, aynı dosyada bulunan tek bir dosya komutu kullanılarak okunabilir. Başvuru için kullanıldığında file komutunun sözdizimi şöyledir:

```
file -r -rpr prefixString fileName;
```
veya

```
file -r -ns nameSpace fileName
```
İşte bir örnek dizi.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Bu örnek, "solar" dosyasında yer alan sun nesnesine bu dosyada "solar_sun" adı kullanılarak erişilebileceğini göstermektedir.

### Gereksinimler

Bir .ma dosyasının Gereksinimler bölümü, bir dizi gerekli komuttan oluşur ve dosyaları okumak için gerekli olan sürüm ve eklenti bilgileri gibi Mayıs bilgilerini söyler. Gereksinimler bölümünün bir örneği aşağıdaki gibidir.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Bir sonraki bölüm gereksinimleri belirtir. Bu, bir dizi gereksinim komutundan oluşur. Dosyanın bu bölümü, Maya'ya dosyayı düzgün bir şekilde yüklemek için hangi yazılımın gerekli olduğunu söyler. Spesifik olarak, Maya'nın hangi sürümü ve hangi eklentiler.

## MA dosyası indir
Bir 3d modelin MA dosyasını bulup indirmek biraz zor. Bu nedenle, örnek bir MA dosyasını buradan indirebilirsiniz:

- [Sample.ma](../sample.ma)


## Referanslar

* [Maya ASCII Dosyalarının Düzenlenmesi - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

