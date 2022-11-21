{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - File Referensi Makro Microsoft Office",
  "description":"Pelajari tentang file MSO dan API yang dapat membuat dan membuka file MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Apa itu file MSO?

File MSO adalah format file wadah data yang dibuat saat pesan HTML dikirim menggunakan Microsoft Outlook. Ini kebanyakan terjadi dengan aplikasi Microsoft Office 2000. Dalam sebagian besar kasus, pesan email dilampirkan dengan nama file **Oledata.mso**. Penerima email, ketika membuka email semacam itu, dapat melihat file dengan benar meskipun mereka tidak menginstal perangkat lunak yang sama. File MSO mengacu pada [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Format File MSO Microsoft

File MSO disimpan dalam Microsoft Compound Document File Format (MCDF) yang juga dikenal sebagai Object Linking and Embedding (OLE) atau Component Object Model (COM) structured storage compound file implementasi format file biner.

### Struktur Format File MSO

Struktur format file internal format file MSO didefinisikan dengan baik di [Struktur](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) bagian dari dokumentasi MCDF. Tabel Alokasi File (FAT) mengelola alokasi sektor dan rantai sektor. Ini berisi array nomor sektor 32-bit. Setiap indeks dalam larik mewakili nomor sektor sedangkan nilainya mewakili sektor berikutnya dalam rantai atau nilai khusus.

## Referensi

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

