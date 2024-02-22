{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Dosya Formatını Değiştir",
  "description":"OSC dosya formatı ve OSC dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-tr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## .OSC dosyası nedir?

Bir OSC dosyası, mevcut bir .osm sokak haritası için değiştirilmiş sokak haritası verilerini içeren bir Değişiklik Dosyası Formatıdır. [OSM file](/gis/osm/)'da yapılacak değişiklikler hakkında bilgi içerir. OSC dosyası, OSM verileri üzerinde üç olası değişiklik işlemine sahip olabilir; yani 'ekleme', 'değiştirme' veya 'silme'. Bu değişiklik dosyaları genellikle verileri OSM düzenleyicisinden dışarı aktarmak ve başka bir düzenleyiciye aktarmak için kullanılır.

OSC dosyalarını Merkaartar ve osmchange yazılımıyla açabilirsiniz.

## OSC Dosya Formatı

OSC dosyaları genellikle değişikliklerin etiketlerle temsil edildiği JOSM dosya biçiminde kaydedilir. Dosyanın başlangıcını belirten `osmChange` etiketiyle başlar. Alt etiketler, OSM dosyasındaki ilgili düğümde gerçekleştirilecek işlemin ekleme, değiştirme veya silme işlemi olup olmadığını belirtir. Bir düğümün içeriği aslında bir osm etiketinin içeriğini içerir.

### OSC Dosya Formatı Örneği

Aşağıda bir düğümdeki değişiklik işleminin bir örneği verilmiştir. Her öğenin bir değişiklik kümesi kimliği ve sürüm numarası olmalıdır.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referanslar

* [JOSM Dosya Formatı](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


