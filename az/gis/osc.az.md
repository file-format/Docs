{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap fayl formatını dəyişdirin",
  "description":"OSC fayl formatı və OSC faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-az",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## OSC faylı nədir?

OSC faylı mövcud .osm küçə xəritəsi üçün dəyişdirilmiş küçə xəritəsi məlumatlarını ehtiva edən Dəyişiklik Fayl Formatıdır. O, [OSM file](/gis/osm/) üçün ediləcək dəyişikliklər haqqında məlumatı ehtiva edir. OSC faylı OSM məlumatlarında üç mümkün modifikasiya əməliyyatına malik ola bilər, yəni `daxil et`, `dəyişiklik et` və ya `silmək`. Bu dəyişiklik faylları adətən OSM redaktorundan məlumatları ixrac etmək və başqa redaktora idxal etmək üçün istifadə olunur.

OSC fayllarını Merkaartar və osmchange proqramı ilə aça bilərsiniz.

## OSC fayl formatı

OSC faylları adətən JOSM fayl formatında saxlanılır, burada dəyişikliklər teqlərlə təmsil olunur. Faylın başlanğıcını göstərən `osmChange` etiketi ilə başlayır. Alt etiketlər bunun OSM faylında müvafiq node üzərində yerinə yetirilməli olan daxil etmə, dəyişdirmə və ya silmə əməliyyatı olub olmadığını müəyyənləşdirir. Bir qovşağın məzmunu əslində osm etiketinin məzmununu ehtiva edir.

### OSC fayl formatı nümunəsi

Aşağıda bir qovşaqda dəyişdirmə əməliyyatının nümunəsi verilmişdir. Hər bir elementdə dəyişiklik dəsti ID-si və versiya nömrəsi olmalıdır.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## İstinadlar

* [JOSM Fayl Formatı](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


