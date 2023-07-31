{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file BCP dan API yang dapat membuat dan membuka file BCP.",
  "title" :"BCP - Format File Salinan Massal SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file BCP?

BCP (Bulk Copy Format) adalah format data teknis Microsoft SQL Server yang menentukan struktur data untuk menyimpan nilai tipe data database yang berbeda untuk impor/ekspor. Format sepenuhnya mendefinisikan interpretasi dari setiap kolom data sehingga kumpulan nilai yang ditentukan dalam file data dapat dibaca. Utilitas [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) menggunakan format file BCP untuk membaca data dari file tersebut dan mengidentifikasinya.


## Format File BCP

File format BCP adalah dokumen XML yang menentukan urutan kolom, nama, dan tipe data. Ini memungkinkan pengguna mengimpor/mengekspor data dalam jumlah besar dari file data yang menentukan bidang ini. Ini berguna dalam impor massal nilai data dari file data. Jumlah dan urutan bidang data dalam file data mungkin berbeda dengan yang ada di kolom tabel tujuan. Ini adalah saat file format data BCP membantu dengan menentukan urutan dan jenis kolom untuk mengimpor data.

Struktur file format direpresentasikan dalam format berikut.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Tipe Data BCP

|Tipe Data|Rentang|Representasi|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) hingga 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Biner|1 hingga 8000 byte|format string Unicode berkode heksadesimal `Biner = 32000OCTET`|
|Bit|0 atau 1|string Unicode sederhana Bit = "0" / "1"|
|Char|1 hingga 8000|Format String Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET dengan n = 4 x (2.147.483.647)|
|Tanggal|01-01-01 sampai 31-12-9999|format string YYYY-MM-DD|
|TanggalWaktu|01-01-1753 00:00:00.000 sampai 31-12-9999 23:59:59.997| Unicode YYYY-MM-DD format string hh:mm:ss[.nnn]|
|DateTime2|0001-01-01 00:00:00.0000000 sampai 9999-12-31 23:59:59.9999999.| Unicode YYYY-MM-DD format string hh:mm:ss[.nnnnnnn]|
|DateTimeOffset|0001-01-01 00:00:00.0000000 hingga 9999-12-31 23:59:59.9999999 dalam zona waktu Waktu Universal Terkoordinasi (UTC)| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnn] [{+|-}hh:mm] format string|
|Desimal|-1038 + 1 hingga 1038 – 1|Format string Unicode `Desimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1.79E+308 hingga -2.23E-308; 0; dari 2.23E-308 hingga 1.79E+308|format string Unicode|
|Gambar|urutan byte yang berkisar dari 0 hingga 231 – 1 (2.147.483.647)|format string Unicode yang dikodekan heksadesimal|
|Int|-231 (-2.147.483.648) hingga 231 – 1 (2.147.483.647)|Format string Unicode|

## Referensi

* [Format BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

