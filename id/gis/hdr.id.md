{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDR- Format File Header ESRI BIL",
  "description":"Apa itu file HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Apa itu file HDR?

File HDR adalah file header GIS yang berisi informasi header untuk file Band yang disisipkan demi baris (.BIL). Ini mendeskripsikan data gambar dan memiliki nama yang sama dengan file gambar. File HDR terdiri dari sekumpulan entri, yang masing-masing menjelaskan atribut tertentu dari gambar. File HDR menjelaskan tata letak dan format file BIL untuk diterjemahkan ke koordinat dunia nyata dalam kombinasi dengan file georeferensi terpisah.

## Format Berkas HDR

File HDR disimpan dalam format file teks ASCII. Ini berisi sekumpulan entri di mana setiap entri menjelaskan atribut tertentu dari gambar. Setiap file HDR memiliki format berikut:

```
<keyword> <value>
```

`<keyword> ` - Ini menunjukkan atribut tertentu yang sedang disetel
`<value> ` - Ini adalah nilai atribut yang ditetapkan

Tidak ada batasan pada urutan entri di header. Namun, setiap entri harus berada pada baris terpisah untuk mematuhi metode penguraian yang digunakan oleh pembaca HDR.

## Ringkasan Kata Kunci yang digunakan dalam File HDR

|Kata Kunci |Nilai yang Dapat Diterima |Default|
---|---|---|
|nrows |bilangan bulat apa pun > 0| tidak ada
|ncols |bilangan bulat apa pun > 0| tidak ada
|nbands |bilangan bulat apa pun > 0| 1
|nbit |1, 4, 8, 16, 32| 8
|urutan byte| I = Intel;M = Motorola |sama dengan mesin host|
|tata letak| bil, bip, bsq| bil|
|skipbyte| bilangan bulat apa pun ≥ 0| 0
|ulxmap |bilangan real apa pun| 0|
|ulymap |bilangan real apa pun |nrows - 1|
|xdim |bilangan real apa pun| 1
|ydim |bilangan real apa pun| 1
|bandrowbytes |bilangan bulat apa pun > 0| bilangan bulat terkecil ≥ (ncols x nbits) / 8|
|totalrowbytes |bilangan bulat apa pun > 0| untuk bil: nbands x bandrowbytes;untuk bip: bilangan bulat terkecil ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |bilangan bulat apa pun ≥ 0| 0|

## Referensi

* [Format File HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

