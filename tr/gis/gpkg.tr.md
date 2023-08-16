{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg dosyası", "gpkg dosya biçimi", "gpkg dosyası nedir", "dosya", "gpkg örneği", "gpkg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage Format Dosyaları",
  "description":"GPKG dosya formatı ve GPKG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## GPKG dosyası nedir?
.gpkg uzantılı bir dosya, tipik tanımlara, biçim sınırlamalarına, bütünlük iddialarına ve içerik kısıtlamalarına sahip verileri ve meta veri tablolarını içeren bir SQLite veritabanı kabı olarak uygulanan bir coğrafi bilgi sisteminden oluşur. 2014 yılında yayınlandı; ABD ordusu adına OGC (Open Geospatial Consortium) tarafından tanımlanmıştır. Çeşitli hükümetler, ticari ve açık kaynak kuruluşları GeoPackage'ı geniş ölçüde desteklemektedir.

## GPKG dosya formatı
Bir GeoPackage, genişletilmiş bir SQLite 3 veritabanı dosyası olarak oluşturulur; bir standart, aşağıdakiler için bir dizi kural (gerekli sözleşmeler) tanımlar:
- Karo matris görüntü kümelerinin saklanması
- Vektör özellikleri
- Çeşitli ölçeklerde raster haritalar
- Meta veriler ve şema

Standardın 2.3 maddesinde tanımlanan uzantı kurallarını kullanarak bir GeoPackage'ı genişletebilirsiniz. Bir GeoPackage tasarlamanın amacı, olabildiğince hafif bir veritabanı yapmak ve onu kullanıma hazır tek bir dosyaya dahil etmekti. Bu, çevrimdışı moddaki mobil uygulamalar ve bulut depolama veya USB depolama cihazları vb. üzerinde hızlı paylaşım için idealdir.

### GPKG İçeriği
GeoPackages, diğer ilişkisel veritabanları gibi bir dizi tablo içerir. Bu tablolar, kullanıcı tanımlı veya meta veri tabloları olabilir. GeoPackages iki zorunlu meta veri tablosundan oluşur:

#### gpkg_contents
Bir GeoPackage için içindekiler tablosu. Bu tablodaki zorunlu sütunlar şunlardır:

- **tablo_adı**: kullanıcı tanımlı veri tablosunun gerçek adı;
- **data_type**: veri türü, örneğin başlıklar, özellikler ve öznitelikler;
- **tanımlayıcı ve açıklama**: okunabilir metin ;
- **last_change**: ISO 8601 formatında son değişikliğin bilgilendirme tarihi;
- **min_x, min_y, max_x ve max_y**: içeriğin uzamsal uzantıları. ;
- **srs_id**: uzamsal referans sistemi .

#### gpkg_spatial_ref_sys
Mekansal referans içeriği için; kutucuklar ve özellikler dahil ancak bunlarla sınırlı olmamak üzere içeriklerdeki her satır bir koordinat referans sistemine başvurmalıdır; **gpkg_spatial_ref_sys** tablosunda saklanır. Bu tablodaki zorunlu sütunlar şunlardır:

- **srs_name, description**: SRS için okunabilir bir ad ve açıklama;
- **srs_id**: SRS için benzersiz bir tanımlayıcı; ayrıca tablo için birincil anahtar;
- **kuruluş**: Tanımlayıcı kuruluşun büyük/küçük harfe duyarsız adı.
- **organization_coordsys_id**: SRS'nin kuruluş tarafından atanan sayısal kimliği;
- **tanım**: SRS'nin İyi Bilinen Metin tanımı.


## Referanslar

* [GeoPackage - Wikipedia'dan](https://en.wikipedia.org/wiki/GeoPackage)
* [GeoPackage'a Başlarken](http://www.geopackage.org/guidance/getting-started.html)

