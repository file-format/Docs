{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "file", "format", "jenis file", "ekstensi", "apa itu file DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Pelajari tentang format file DOCX dan API yang dapat membuat dan membuka file DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Apa itu file DOCX? ##

DOCX adalah format terkenal untuk dokumen Microsoft Word. Diperkenalkan dari tahun 2007 dengan dirilisnya Microsoft Office 2007, struktur format Dokumen baru ini diubah dari biner biasa menjadi kombinasi file XML dan biner. File Docx dapat dibuka dengan Word 2007 dan versi lateral tetapi tidak dengan versi MS Word sebelumnya yang mendukung ekstensi file DOC.

## Sejarah Singkat ##

Setelah Microsoft membuka spesifikasi untuk format file DOC, mudah bagi para pesaingnya untuk merekayasa balik format tersebut dan memberikan dukungan yang sama pada aplikasi mereka sendiri. Selain itu, persaingan dari Open Office dalam bentuk Open Document Format-nya, memaksa Microsoft mengadopsi standar yang lebih terbuka dan luas. Pada awal tahun 2000, Microsoft memutuskan untuk melakukan perubahan untuk mengakomodasi standar **Office Open XML**. Dokumen di bawah Standar baru ini diberikan [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), "X" menjadi untuk XML. Pada tahun 2007, format file baru ini menjadi bagian dari Office 2007 dan dijalankan di versi baru Microsoft Office juga. Jenis file baru telah menambahkan keunggulan ukuran file kecil, lebih sedikit perubahan korupsi dan representasi gambar yang diformat dengan baik.

## Spesifikasi Format File DOCX - Informasi Lebih Lanjut

File Docx terdiri dari kumpulan file XML yang terdapat di dalam arsip ZIP. Isi dokumen Word baru dapat dilihat dengan membuka ritsleting isinya. Koleksi berisi daftar file XML yang dikategorikan sebagai:

* File MetaData - berisi informasi tentang file lain yang tersedia di arsip
* Dokumen - berisi isi sebenarnya dari dokumen tersebut

### Berkas Metadata ###

Microsoft Word menggunakan file-file ini untuk menemukan hubungan antar file dan untuk menemukan konten dokumen. Ketika arsip dokumen Word diekstraksi, itu berisi sejumlah file seperti yang dijelaskan di bawah ini.

#### Hubungan - \_rels/.rels ####

File ini berisi informasi yang memberi tahu MS Word tempat mencari konten dokumen dan referensi lainnya. Setiap hubungan diidentifikasi oleh id hubungan yang unik dan menentukan file XML yang direferensikan sebagai target. Contoh file hubungan ditampilkan sebagai berikut:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Jenis Konten ####

Sebuah dokumen dapat berisi beberapa jenis media di dalamnya seperti gambar, tema, seni kata, dll. [Content_Types].xml berisi informasi tentang jenis media yang ada dalam dokumen. Konten file XML seperti itu ditampilkan sebagai berikut:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referensi Ke Sumber Daya - \_rels/document.xml.rels ####

Informasi tentang sumber daya, seperti gambar yang disematkan dalam dokumen, direferensikan dalam file XML ini.

#### Isi Dokumen Utama ####

Ini mengacu pada file XML utama dari arsip yang berisi konten teks dokumen. Konten ini diwakili oleh berbagai node sesuai spesifikasi OpenOffice XML. Sebagian besar isi file ini terdiri dari Paragraf dan Tabel, meskipun bisa juga node lain.

### File Format Node ###

File document.xml utama adalah kumpulan node untuk mewakili keseluruhan konten file. Setiap node memiliki awal dan akhir yang merangkum node lebih lanjut atau isinya. Contoh sederhana dari file xml tersebut adalah sebagai berikut:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Berikut adalah informasi tentang beberapa node yang terdapat dalam file DOCX untuk representasi konten.

`<w:document> ` - Merupakan elemen root dari konten utama file.

`<w:body> ` - Mewakili isi dokumen yang dapat terdiri dari banyak simpul elemen lain seperti paragraf, tabel, dan bagian.

#### Paragraf ####

Sebuah paragraf adalah pemegang konten utama dalam sebuah dokumen. Diwakili oleh **<w:p> ** elemen dalam dokumen. Sebuah paragraf selanjutnya terdiri dari satu atau lebih run **<w:r> ** yang berisi teks paragraf yang sebenarnya. Selain run, paragraf juga dapat berisi elemen dokumen lain seperti hyperlink, komentar, dll. Contoh struktur paragraf adalah seperti yang ditunjukkan di bawah ini:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Referensi ##

* [MS - Format File DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

