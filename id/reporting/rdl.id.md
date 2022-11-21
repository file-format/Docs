{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - File Bahasa Definisi Laporan",
  "keywords" :[ "rdl", "bahasa definisi laporan", "XmlTextWriter", "XSD", "elemen RDL"],
  "description":"Pelajari tentang format file RDL yang merupakan representasi XML dari definisi laporan Layanan Pelaporan SQL Server.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Apa itu file RDL? ##

RDL (Report Definition Language) adalah tolok ukur yang ditetapkan oleh Microsoft untuk menentukan laporan. File RDL terdiri dari satu atau banyak Elemen RDL. Sedangkan elemen RDL terdiri dari tipe data dan kardinalitasnya. Sebuah elemen bisa sederhana atau kompleks. Elemen sederhana tidak memiliki elemen atau atribut anak, sedangkan elemen kompleks memiliki anak dan atribut opsional.

## Definisi Skema RDL XML
File XML Schema Definition (XSD) memvalidasi file RDL. Skema menentukan aturan di mana elemen RDL dapat muncul dalam file .rdl. Elemen RDL bisa sederhana atau kompleks. Elemen sederhana tidak memiliki elemen anak atau atribut dan elemen kompleks memiliki anak dan secara opsional, atribut.

## Membuat RDL
Karena RDL bersifat terbuka dan dapat diperluas, banyak aplikasi dan alat dapat dibangun yang menghasilkan file RDL berdasarkan skema XML-nya. Salah satu cara termudah untuk membuat RDL dari aplikasi adalah dengan menggunakan kelas Microsoft .NET Framework dari namespace **System.Xml** dan System.Linq namespace. Khususnya, kelas **XmlTextWriter**, dapat digunakan untuk menulis RDL. Anda dapat membuat definisi laporan lengkap dari awal hingga akhir dalam aplikasi .NET Framework dengan menggunakan **XmlTextWriter**. Pengembang juga dapat menambahkan item laporan khusus dengan properti khusus untuk memperluas RDL.

## Jenis RDL
Tabel berikut mencantumkan jenis dan atribut yang digunakan dalam elemen RDL.

|Jenis|Deskripsi|
---|---|
|Biner |Sebuah properti dengan nilai biner yang disandikan basis-64.|
|Boolean| Properti dengan benar atau salah sebagai nilai objek. Kecuali ditentukan lain, nilai objek Boolean opsional yang dihilangkan adalah False.|
|Tanggal |Sebuah properti dengan nilai tanggal atau waktu yang ditentukan sepenuhnya ditentukan dalam format tanggal ISO8601: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Sebuah properti dengan nilai teks string yang harus menjadi salah satu dari daftar nilai yang ditunjuk.|
|Float |Properti dengan nilai float. Tanda titik (.) digunakan sebagai pemisah desimal opsional.|
|Integer |Properti dengan nilai integer (int32).|
|Bahasa |Properti dengan nilai teks yang berisi kode bahasa dan budaya, seperti "en-us" untuk bahasa Inggris AS. Nilai harus berupa bahasa tertentu atau bahasa netral yang bahasa defaultnya ditentukan di Microsoft .NET Framework.|
|Nama |Properti dengan nilai teks string. Nama harus unik di dalam ruang nama item. Jika tidak ditentukan, ruang nama untuk suatu item adalah objek yang mengandung paling dalam yang memiliki nama.|
|NormalizedString |Sebuah properti dengan nilai teks string yang telah dinormalisasi.|
|Ukuran |Elemen ukuran harus berisi angka (dengan karakter titik digunakan sebagai pemisah desimal opsional). Angka tersebut harus diikuti oleh penanda untuk satuan panjang CSS seperti cm, mm, in, pt, atau pc. Spasi antara nomor dan penunjuk adalah opsional. Untuk informasi selengkapnya tentang penunjuk ukuran, lihat Nilai CSS dan Referensi Unit. Di RDL, nilai maksimum untuk Ukuran adalah 160 inci. Ukuran minimumnya adalah 0 inci.|
|String |Properti dengan nilai teks string.|
|UnsignedInt |Sebuah properti dengan nilai unsigned integer (uint32).|
|Varian |Sebuah properti dengan tipe XML apa pun yang sederhana.|

## Tipe Data RDL
Di RDL, DataType Enumeration mendefinisikan tipe data dari atribut, ekspresi, atau parameter. Tabel berikut memperlihatkan bagaimana tipe data CLR terkait dengan tipe data RDL.

|CLR Type(s) |Coresponding Data Type|
---|---|
|Boolean| Boolean|
|TanggalWaktu, TanggalWaktuOffset |TanggalWaktu|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Tunggal, Ganda |Mengambang|
|String, Karakter, GUID, Rentang Waktu |String|


## Referensi ##

- [Bahasa Definisi Laporan (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

