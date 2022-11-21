{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Laporan Tata Letak Halaman",
  "keywords" :[ "rpl", "Laporkan Tata Letak Halaman", "XSD", "SQL Server", "pelaporan"],
  "description":"Pelajari tentang format aliran RPL yang merupakan format biner internal yang digunakan oleh Layanan Pelaporan Microsoft SQL Server saat menghubungi dengan kontrol penampil.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Apa itu file RPL? ##

Format aliran RPL (Report Page Layout) adalah format biner internal yang digunakan oleh Layanan Pelaporan MS SQL Server saat menghubungi kontrol penampil untuk mengurangi beberapa pekerjaan rendering dari server ke kontrol penampil klien. Pengembang dapat membuat perancang laporan khusus dengan menggunakan RPL, yang akan menghasilkan RPL serta penyaji laporan khusus yang memproses dan menampilkan file RPL untuk menampilkan laporan.

## Struktur RPL

Aliran RPL mencakup struktur aliran, struktur laporan, properti laporan, dan pencacahan. Setiap struktur termasuk yang berikut:

- Definisi struktur.

- Tata bahasa Augmented Backus-Naur Form (ABNF) untuk struktur.

- Sedikit diagram struktur.

- Definisi semua bidang yang terkandung dalam struktur.

Berikut adalah catatan singkat tentang beberapa Struktur RPL:

### Struktur Aliran
Struktur aliran terdiri dari serangkaian record. Rekaman berisi nol atau beberapa bidang terstruktur yang berisi tata letak laporan.

#### Aliran RPL
Aliran RPL harus memiliki hanya satu catatan Laporan dan aliran harus berupa rangkaian catatan biner yang mempertahankan hierarki laporan.

#### Catatan
Catatan adalah blok bangunan dasar yang digunakan untuk menyimpan informasi tentang laporan. Sebuah record terdiri dari urutan byte dengan panjang bervariasi. Sebuah record terdiri dari dua komponen:
- Jenis catatan
- Data rekaman yang khusus untuk jenis rekaman tersebut.
Jenis rekaman adalah satu byte yang menentukan jenis informasi apa yang ditentukan oleh rekaman dan bagaimana struktur data rekaman yang berkaitan dengan rekaman dipesan dan disusun. Nilai record bergantung pada jenis data yang khusus untuk record tersebut.

#### Struktur Tipe Data Sederhana

Tabel berikut menentukan tipe data dalam aliran RPL.

|Deskripsi| format|
---|---|
|Char|Mewakili nilai numerik (ordinal) 16-bit (2-byte).|
|Byte|Mewakili 8-bit (1-byte) unsigned integer.|
|Int16|Mewakili bilangan bulat bertanda tangan 16-bit (2-byte).|
|Single|Mewakili nilai floating point presisi tunggal 32-bit (4-byte).|
|Desimal|Mewakili tipe data 128-bit (16-byte).|
|DateTime|Mewakili pengkodean 64-bit (8-byte) dari nilai tanggal dan waktu.|
|Int64|Mewakili bilangan bulat bertanda 64-bit (8-byte).|
|Int32|Mewakili bilangan bulat bertanda tangan 32-bit (4-byte).|
|Float|Mewakili nilai floating point presisi tunggal 32-bit (4-byte).|
|Boolean|Mewakili nilai tipe Boolean logis 8-bit (1-byte). Nilai yang valid adalah benar (1) dan salah (0).|
|Panjang|Mewakili bilangan bulat bertanda 64-bit (8-byte).|
|String|Semua nilai String dalam protokol HARUS UNICODE UTF-16. Secara default, semua nilai String dimulai dengan bilangan bulat yang menentukan panjang String. Nilai string direpresentasikan dalam protokol sebagai larik byte; jumlah byte HARUS sama dengan jumlah karakter dalam String dikalikan dua.|

### Struktur Laporan
Struktur laporan mencakup definisi dan ukuran struktur dan elemen yang relevan.

Daftar berikut menentukan struktur laporan:

- Laporan
- Versi: kapan
- Laporkan Properti
- Elemen Array Offset
- Konten Halaman
- Halaman
- Properti halaman
- Tata letak halaman
- Bagian
- Bagian Sederhana
- Bagian Campuran
- Properti Bagian
- Elemen Area Tubuh
- Elemen Tajuk Halaman
- Elemen Footer Halaman
- Elemen Tubuh
- Properti Elemen
- Properti Elemen Bersama
- Gunakan Properti Elemen Bersama
- Properti InlineSharedElement
- Properti NonSharedElement
- Gaya
- Properti Gaya Bersama
- Properti NonSharedStyle
- Info Aksi
- Konten InfoAksi
- Tindakan
- Area ActionImageMap
- Info Aksi Dengan Peta
- DynamicImageData
- Offset Konsolidasi Gambar
- LaporanItem
- Garis
- Gambar
- Properti GambarData
- Gunakan SharedImageDataProperties
- Properti Data Gambar Bersama Sebaris
- Properti Data Gambar NonShared
- Data Gambar
- Area Peta Gambar
- Area Peta Gambar
- Bagan
-Panel Pengukur
- Peta
- Persegi panjang
- SubLaporan
- RichTextBox
- Isi Paragraf
- TextRun
- Gugus kalimat
- Struktur RichTextBox
- Tablix
- Konten Tablix
- Struktur Tablix
- Pengukuran Tablix
- Lebar Kolom
- Info Kolom
- RowHeights
- Info Baris
- TablixRow
- TablixRowCell
- Tablix Corner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Pengukuran
- Pengukuran
- ReportElementEnd

### Properti
Berikut adalah daftar properti yang dapat digunakan dalam RPL Stream:

- PENGENAL
- Jumlah Kolom
- Spasi Kolom
- Nama yang unik
- Nama
- Label
- Penanda buku
- Tip Alat
- ToggleItem
- Keterangan
- Lokasi
- KonsumsiContainerWhiteSpace (RPL 10.6)
- Bahasa
- Waktu eksekusi
- Pengarang
- Penyegaran Otomatis
- Nama Laporan
- Tinggi Halaman
- Lebar Halaman
- MarginTop
- Margin Kiri
- Margin Kanan
- Margin Bawah
- Kolom
- Nama Halaman (RPL 10.6)
- Miring
- Bisa Tumbuh
- Bisa Menyusut
- Nilai
- ToggleState
- CanSort
- SortState
- Rumus
- IsToggleParent
- TypeCode
- Nilai asli
- Sederhana
- ContentOffset
- StreamName
- Ukuran
- LinkToChild
- CetakPadaHalamanPertama
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- DiprosesDenganKesalahan
- Tipe GambarMIME
- Nama Gambar
- Lebar
- Tinggi
- Resolusi horisontal
- Resolusi Vertikal
- RawFormat
- Hyperlink
- BookmarkLink
- DrillthroughId
- MenelusuriUrl
- Warna Perbatasan
- BorderColorLeft
- BorderColorRight
- Warna Perbatasan Atas
- Batas Warna Bawah
- Gaya Perbatasan
- Gaya Perbatasan Kiri
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Lebar Perbatasan
- Lebar Batas Kiri
- Lebar Batas Kanan
- Batas Lebar Atas
- Lebar Batas Bawah
- Bantalan Kiri
- Bantalan Kanan
- PaddingTop
- Bantalan Bawah
- Gaya tulisan
- FontFamily
- Ukuran huruf
- FontWeight
- Format
- Dekorasi Teks
- Perataan Teks
- Perataan Vertikal
- Warna
- Tinggi garis
- Arah
- Mode Menulis
- UnicodeBiDi
- Gambar latar belakang
- Warna latar belakang
- Ulangi Latar Belakang
- Bahasa Angka
- Varian Angka
- Kalender
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- Tata Letak Arah
- Jalur Definisi
- Tingkat
-MemberCellIndex
- CellItemOffset
- ColSpan
-RowSpan
- DefIndex
- Indeks Kolom
- Indeks Baris
- Label Grup
- Tingkat Toggle Rekursif
- Gaya Daftar
- Tingkat Daftar
- Nomor Paragraf
- Indent Kanan
- Lekukan Kiri
- Indentasi Gantung
- SpaceBefore
- Ruang Setelah
- Garis pertama
- Markup
- KontenTop
- Konten Kiri
- Lebar Konten
- KontenTinggi
- Negara
- CellItemState
- MemberDefState

### Pencacahan
Daftar berikut menunjukkan pencacahan yang dapat digunakan dalam aliran RPL:

- Urutkan Opsi
- Ukuran
- Tipe Bentuk
- ImageRawFormat
- Gaya Font
- FontWeights
- Dekorasi Teks
- Perataan Teks
- Penjajaran Vertikal
- Arah
- Mode Menulis
- Jenis UnicodeBiDi
- Kalender
- Gaya Perbatasan
- BackgroundRepeatTypes
- Daftar Gaya
- Gaya Markup
- TypeCode
- Nilai Negara
- TablixMemberStateValues
- TablixMemberDefStateValues
- Ukuran RPL





## Referensi ##

- [Laporan Tata Letak Halaman (RPL) Format Aliran Biner](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

