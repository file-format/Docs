{
  "date" : "2020-08-20",
  "keywords" :[ "file fon", "format file fon", "apa itu file fon", "file", "contoh fon", "ekstensi file fon", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - File Perpustakaan Font",
  "description":"Pelajari tentang format file FON dan API yang dapat membuat dan membuka file FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Apa itu file FON?

File dengan ekstensi .fon adalah perpustakaan font Microsoft Windows 3.x yang sebenarnya adalah file yang dapat dieksekusi tetapi diganti namanya menjadi .fon. Ini adalah kumpulan file [.fnt](/id/font/fnt/) itu sendiri dan aplikasi mereferensikannya saat mengakses font sistem. Itu sebabnya ia bertindak sebagai file sumber daya. Itu dapat dibuka di OS Windows menggunakan aplikasi Microsoft Windows Font View.

## Format File FO

File FON berisi sumber daya font dan memiliki format file Resource (.res). Format file .res menentukan header file serta spesifikasi bagian data. .fnt juga merupakan file data sumber daya yang disertakan dengan file sumber daya. File FON memiliki format file biner dan memiliki tipe MIME application/octet-stream.

Sumber daya font, tidak seperti jenis sumber daya lainnya, tidak ditambahkan ke sumber daya aplikasi. Sebaliknya, mereka ditambahkan ke file EXE dan diganti namanya menjadi file .fon, menghasilkan file perpustakaan, bukan aplikasi. Beberapa font Individu merupakan komponen dari grup font di mana setiap grup mengikuti struktur grup sumber daya. Sumber daya font menggunakan struktur grup sumber daya ini. Header grup memiliki semua informasi yang diperlukan untuk mengakses font tertentu dari grup. Sumber daya komponen font memiliki format berikut.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/id/font/fnt/) file)
```
Satu file sumber daya .rc dapat memiliki deklarasi sumber daya campuran. Grup font dapat berada di mana saja di file sumber daya dan tidak perlu bersebelahan. Program yang membuat file .RES harus menambahkan entri manual FONTDIR. Berikut adalah struktur tajuk grup.

```
[Header sumber daya normal (tipe = 7)]

Jumlah KATAFont; // Jumlah total dalam file .RES
```     
The remaining data is repeated for every font in the .RES file.

```
Fon KATAOrdinal;
struct FontDirEntry {
KATA dfVersi;
DWORD dfSize;
char dfHak Cipta[60];
KATA dfType;
dfPoin KATA;
KATA dfVertRes;
KATA dfHorizRes;
KATA Berkembang;
KATA dfPemimpin Internal;
KATA dfExternalLeading;
BYTE dfItalik;
BYTE dfUnderline;
BYTE dfStrikeOut;
KATA dfBerat;
BYTE dfCharSet;
KATA dfPixWidth;
KATA dfPixTinggi;
BYTE dfPitchAndFamily;
KATA dfRata-rataLebar;
KATA dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
KATA dfLebarBytes;
DWORD dfPerangkat;
DWORD dfFace;
DWORD dfDipesan;
char szDeviceName[];
char szNamaWajah[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

