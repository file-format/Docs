{
  "date" : "2019-10-11",
  "keywords" :[ "file dicom", "format file dicom", "apa itu file dicom", "file", "contoh dicom", "ekstensi file dicom", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Format File Pencitraan Digital dan Komunikasi",
  "description":"Pelajari tentang format file DICOM dan API yang dapat membuat dan membuka file DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DICOM?

DICOM adalah singkatan dari Digital Imaging and Communications in Medicine dan berkaitan dengan bidang Informatika Medis. DICOM digunakan untuk integrasi perangkat pencitraan medis seperti printer, server, pemindai dll dari berbagai vendor dan juga berisi data identifikasi setiap pasien untuk keunikannya. File DICOM dapat dibagi antara dua pihak jika mereka dapat menerima data gambar dalam format DICOM. Bagian komunikasi DICOM adalah protokol lapisan aplikasi dan menggunakan TCP/IP untuk berkomunikasi antar entitas. Versi yang didukung oleh layanan web adalah 1.0, 1.1, 2 atau yang lebih baru.

## Sejarah ##

DICOM dikembangkan bersama oleh American College of Radiology (ACR) dan National Electrical Manufacturers Association (NEMA) untuk pertukaran dan tampilan gambar medis seperti MRI, CT scan, dan gambar ultrasound. Awalnya, sulit untuk memecahkan kode gambar yang dihasilkan mesin. Oleh karena itu, ACR dan NEMA bersama-sama membentuk tim pada tahun 1983 yang merilis standar pertamanya, ACR/NEMA 300 pada tahun 1985. Versi kedua dirilis pada tahun 1988 yang lebih populer di kalangan vendor, namun segera disadari bahwa versi kedua juga perlu perbaikan. Versi ke-3 dari standar dirilis pada tahun 1993 sebagai "DICOM". 3.0 masih merupakan versi terbaru namun terus diperbarui sejak tahun 1993.

## Format File DICOM ##

DICOM adalah kombinasi dari definisi format file dan protokol komunikasi jaringan. DICOM menggunakan ekstensi .DCM. .DCM ada dalam dua format yang berbeda yaitu format 1.x dan format 2.x. DCM Format 1.x selanjutnya tersedia dalam dua versi normal dan diperpanjang. Protokol HTTP dan HTTPS digunakan untuk layanan web DICOM.

### Kepala Berkas ###

Header file berisi Pembukaan File 128 byte, dan awalan DICOM 4 byte.

**Pembukaan # 128 Byte**|**Awalan # 4 Byte “D, I, C, M**

**Pembukaan** digunakan untuk mengakses gambar dan data lain dalam file DICOM yang menyediakan kompatibilitas dengan format file gambar yang umum digunakan.

**Awalan** berisi string "DICM" sebagai karakter huruf besar.

### Himpunan data ###

Setiap file harus berisi satu kumpulan data yang mewakili contoh SOP dan Kelas SOP dengan IOD terkait. Kumpulan data adalah representasi dari informasi dunia nyata. Kumpulan data berisi elemen data dan elemen data berisi nilai atribut objek itu. Struktur atribut ditentukan dalam IOD. Objek data DICOM terdiri dari sejumlah atribut, termasuk item seperti nama, ID, dll., dan juga satu atribut khusus yang berisi data piksel gambar.

### Elemen Data ###

Elemen data terdiri dari tag elemen data, panjang nilai dan nilai untuk elemen data. Ada 5 jenis elemen Data yaitu elemen Data Wajib Tipe 1, Elemen Data Bersyarat Tipe 1C, Elemen Data Wajib Tipe 2, Elemen Data Bersyarat Tipe 2C, dan Elemen Data opsional Tipe 3. Dasar Tiga jenis struktur elemen data adalah sebagai berikut.

**Elemen Data dengan VR Eksplisit**

|Nomor Grup|Nomor Elemen|Representasi Nilai|Dicadangkan|Panjang Nilai|Bidang Nilai
---|---|---|---|---|---|
|2 Byte|2 Byte|2 Byte|2 Byte # 0x00, 0x00|4 Byte|"Nilai Panjang Byte"

**Elemen Data dengan VR Eksplisit**

|Nomor Grup|Nomor Elemen|Representasi Nilai|Panjang Nilai|Bidang Nilai
---|---|---|---|---|
|2 Byte|2 Byte|2 Byte|2 Byte|"Nilai Panjang Byte"

**Elemen Data dengan VR Implisit**


|Nomor Grup|Nomor Elemen|Panjang Nilai|Bidang Nilai
---|---|---|---|
|2 Byte|2 Byte|4 Byte|"Nilai Panjang Byte"

1. **Tag Elemen Data**: Integer terurut yang mewakili nomor grup dan nomor elemen
1. **Representasi Nilai VR**: VR adalah string karakter yang mewakili VR elemen data.
1. **Panjang Nilai**: apakah bilangan bulat tidak bertanda mewakili panjang eksplisit bidang nilai.
1. **Bidang Nilai**: Menjelaskan nilai elemen data.

## Mentransfer Sintaks ##

Sintaks transfer adalah seperangkat aturan untuk pengkodean agar secara jelas mewakili sintaksis yang lebih abstrak. Dengan bantuan sintaks transfer entitas yang berkomunikasi bernegosiasi tentang teknik pengkodean umum yang mereka dukung.

## SOP ##

Persatuan IOD dan DIMSE mendefinisikan Kelas SOP. Definisi Kelas SOP berisi aturan dan semantik yang dapat membatasi penggunaan layanan di Grup Layanan DIMSE atau Atribut IOD. Contoh Elemen Layanan adalah Simpan, Dapatkan, Temukan, Pindahkan, dll. Contoh Objek adalah gambar CT, gambar MR, tetapi juga termasuk daftar jadwal, antrean cetak, dll.

## Jasa ##

DICOM menyediakan berbagai layanan, sebagian besar terkait dengan komunikasi data. Masing-masing dijelaskan secara singkat di bawah ini:


**Store:** Layanan DICOM Store mengirim gambar atau objek lain ke sistem pengarsipan dan komunikasi gambar (PACS) atau server.


**Komitmen penyimpanan:** Layanan komitmen penyimpanan digunakan untuk konfirmasi bahwa gambar telah disimpan secara permanen ba perangkat di semua jenis media.


**Kueri/ambil:** Layanan ini memungkinkan stasiun kerja menemukan daftar gambar atau objek lain, lalu mengambilnya dari PACS.


**Daftar kerja modalitas:** Layanan daftar kerja modalitas memberikan daftar prosedur pencitraan yang telah dijadwalkan untuk dijalankan oleh perangkat akuisisi citra.


**Cetak:** Layanan ini mengirim gambar ke printer.

## Nomor port melalui IP ##

DICOM menggunakan port TCP dan UDP berikut:

1. 104
1. 2761
1. 2762
1. 11112

## Referensi ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

