{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK Dosyası - ArcGIS Harita Paketi Dosya Formatı",
  "description":"MPK dosya formatı ve MPK dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-tr",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## .MPK dosyası nedir?

MPK dosyası, ArcGIS ile oluşturulan bir ArcGIS Harita paket dosyasıdır. Bir .mxd harita belgesi ve ilgili verileri içerir. Ayrıca başvurulan katmanlar, semboller ve diğer kaynaklar gibi ek bilgiler içerir. MPK dosyası, haritaları ve verileri diğer kullanıcılarla paylaşmak için kullanılır. Bu, orijinal veri kaynağına sahip olan diğer kişilerin kullanılabilirliğini ortadan kaldırır ve aynı zamanda bir mobil cihazda kullanılacak haritaların dağıtılmasına da yardımcı olur.

## MPX Dosya Formatı

MPX dosyalarının dahili dosya biçimi ayrıntıları, geliştiricinin referansı için kamuya açık değildir.

### ArcGIS Kullanarak MPK Dosyası Oluşturun

MPK dosyaları ArcGIS kullanılarak oluşturulabilir. Harita Paketi menüsündeki Farklı Paylaş seçeneği, harita belgesini ve onun tüm referanslı verilerini ve kaynaklarını içeren bir .mpk dosyası oluşturmak için kullanılabilir. Bu MPK dosyası daha sonra başkalarıyla paylaşılabilir ve haritayı ve verileri görüntülemek için ArcMap ve ArcGIS Pro'da açılabilir.

### Python kullanarak MPK Dosyası Oluşturun

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Bir klasördeki tüm Harita Belgeleri için Harita Paketleri Oluşturmak amacıyla Python'u Kullanma

Aşağıdaki Python kodu, belirtilen bir klasörde bulunan tüm harita belgeleri için harita paketleri bulur ve oluşturur.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## Referanslar

* [Paket Haritası](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


