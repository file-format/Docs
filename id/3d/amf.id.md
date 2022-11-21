{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "file amf", "format file amf", "format file", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file AMF dan API yang dapat membuka dan membuat file AMF.",
  "title" :"AMF - File Manufaktur Aditif",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file AMF?
File AMF terdiri dari pedoman deskripsi objek untuk digunakan oleh proses Manufaktur Aditif. Ini berisi pembukaan<amf> tag XML dan diakhiri dengan a</amf> elemen. Ini didahului oleh baris deklarasi XML yang menentukan versi XML dan penyandian file. Deklarasi dapat menyertakan informasi satuan pengukuran dan, jika tidak ada informasi tersebut, milimeter digunakan sebagai satuan default.


## Format File AMF

Format file Manufaktur Aditif (**AMF**) menentukan standar terbuka untuk deskripsi objek agar dapat digunakan oleh proses manufaktur aditif seperti Pencetakan 3D. Program CAD menggunakan format file AMF dengan memanfaatkan informasi seperti geometri, warna dan bahan objek. AMF berbeda dari format STL karena lateral tidak mendukung warna, bahan, kisi, dan konstelasi.

### Elemen File AMF

Lima elemen tingkat atas didefinisikan dengan<AMF> tag adalah sebagai rinci di bawah ini. Kehadiran elemen objek tunggal adalah keharusan untuk file AMF yang berfungsi penuh.

`<object> ` - Elemen objek menentukan volume atau volume material, yang masing-masing dikaitkan dengan ID material untuk pencetakan. Setidaknya satu elemen objek harus ada dalam file. Objek tambahan bersifat opsional.

`<material> ` - Elemen bahan opsional menentukan satu atau lebih bahan untuk dicetak dengan ID bahan terkait. Jika tidak ada elemen material yang disertakan, satu material standar diasumsikan.

`<texture> ` - Elemen tekstur opsional menentukan satu atau lebih gambar atau tekstur untuk pemetaan warna atau tekstur, masing-masing dengan ID tekstur terkait.

`<constellation> ` - Elemen konstelasi opsional secara hierarki menggabungkan objek dan konstelasi lainnya ke dalam pola relatif untuk dicetak.

`<metadata> ` - Elemen metadata opsional menentukan informasi tambahan tentang objek dan elemen yang terkandung dalam file.

## Contoh AMF

Berikut adalah contoh file AMF yang dapat disalin ke file [text](/id/word-processing/txt/) dan disimpan sebagai file [zip](/id/compression/zip/) terkompresi untuk dibuka.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referensi

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Spesifikasi AMF pada ISO](https://www.iso.org/standard/67472.html)

