{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Mengubah Format File",
  "description":"Pelajari tentang format file OSC dan API yang dapat membuat dan membuka file OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-id",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Apa itu file OSC?

File OSC adalah Ubah Format File yang berisi data peta jalan yang dimodifikasi untuk peta jalan .osm yang ada. Berisi informasi tentang perubahan yang akan terjadi pada [OSM file](/gis/osm/). File OSC dapat memiliki tiga kemungkinan jenis operasi modifikasi pada data OSM yaitu `masukkan`, `modifikasi`, atau `hapus`. File perubahan ini biasanya digunakan untuk mengekspor data keluar dari editor OSM dan mengimpor ke editor lain.

Anda dapat membuka file OSC dengan perangkat lunak Merkaartar dan osmchange.

## Format Berkas OSC

File OSC biasanya disimpan dalam format file JOSM dimana perubahannya diwakili oleh tag. Ini dimulai dengan tag `osmChange` yang menunjukkan awal file. Sub-tag menentukan apakah operasi penyisipan, modifikasi, atau penghapusan akan dilakukan pada node terkait dalam file OSM. Isi dari sebuah node sebenarnya berisi isi dari tag osm.

### Contoh Format File OSC

Berikut adalah contoh operasi modifikasi pada sebuah node. Setiap elemen harus memiliki ID set perubahan dan nomor versi.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referensi

* [Format Berkas JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


