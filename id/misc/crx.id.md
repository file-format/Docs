{
"tanggal": "08-06-2023",
  "keywords": [
"file crx",
"apa itu file crx",
"cara memasang file crx di google chrome",
"cara membuka file crx",
"apa isi file crx",
"apa format file crx",
"mengajukan",
"ekstensi file crx",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File CRX - Ekstensi Google Chrome",
  "description":"Pelajari tentang format CRX dan API yang dapat membuat dan membuka file CRX.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent" : "misc"
}
},
"mod terakhir": "08-06-2023"
}

## Apa itu file CRX?

Format file CRX dikaitkan dengan ekstensi browser Google Chrome. File CRX pada dasarnya adalah paket terkompresi yang berisi file dan metadata yang diperlukan agar ekstensi dapat dipasang dan dijalankan di Google Chrome. Ini meningkatkan fungsionalitas atau tampilan browser web dengan menyediakan fitur atau tema tambahan.

Saat file CRX diunduh dan dipasang di Google Chrome, browser memverifikasi integritas ekstensi menggunakan kunci publik dan tanda tangan. Jika verifikasi berhasil, Chrome mengekstrak konten file CRX dan memasang ekstensi, sehingga tersedia untuk digunakan. Pengguna dapat mengelola ekstensi mereka melalui halaman Ekstensi Chrome, yang memungkinkan pengaktifan, penonaktifan, atau penghapusan ekstensi yang dipasang.

## Bagaimana cara menginstal file CRX di Google Chrome?

Untuk memasang file CRX di Google Chrome, Anda dapat mengikuti langkah-langkah berikut:

1. Buka peramban Chrome.
2. Ketik `chrome://extensions` di bilah alamat dan tekan Enter.
3. Aktifkan sakelar sakelar "Mode pengembang" yang terletak di sudut kanan atas halaman Ekstensi.
4. Klik tombol "Muat belum dibongkar".
5. Cari dan pilih folder yang berisi konten ekstrak file CRX (atau cukup pilih file CRX itu sendiri).
6. Klik "Buka" untuk menginstal ekstensi.

## Apa isi file CRX?

File CRX berisi file dan metadata yang diperlukan untuk ekstensi Google Chrome. Berikut ini rincian konten umum yang ditemukan dalam file CRX:

- **File manifes (manifest.json):** File ini adalah file berformat JSON yang berisi informasi tentang ekstensi seperti nama, versi, deskripsi, izin, dan skrip latar belakangnya. Ini mendefinisikan struktur dan perilaku ekstensi.
- **File JavaScript:** File ini berisi kode yang mendefinisikan fungsionalitas ekstensi. Mereka mungkin menyertakan skrip untuk menangani peristiwa, memodifikasi halaman web, atau berinteraksi dengan API Chrome.
- **File HTML, CSS, dan gambar:** Ekstensi sering kali menyertakan elemen antarmuka pengguna, seperti jendela popup atau halaman opsi. File HTML menentukan struktur antarmuka ini, sedangkan file CSS mengontrol tampilannya. File gambar digunakan untuk ikon atau aset grafis lainnya.
- **File sumber daya opsional:** Ekstensi dapat mencakup sumber daya tambahan, seperti file pelokalan untuk mendukung berbagai bahasa. File-file ini berisi terjemahan teks yang digunakan dalam antarmuka pengguna ekstensi.
- **Skrip latar belakang:** Jika ekstensi memiliki proses latar belakang atau skrip yang berjalan secara independen dari halaman web aktif, skrip ini akan disertakan dalam file CRX.
- **Skrip konten:** Skrip konten adalah skrip yang dapat dimasukkan ke halaman web untuk mengubah perilaku atau berinteraksi dengan kontennya. Jika ekstensi menggunakan skrip konten, file yang diperlukan untuk skrip tersebut akan ada dalam file CRX.
- **Aset lainnya:** Tergantung pada persyaratan ekstensi tertentu, file tambahan seperti file audio atau video, font, atau file data mungkin disertakan.

Format file CRX pada dasarnya adalah paket terkompresi yang berisi semua file dan folder ini secara terstruktur. Saat file CRX dipasang di Google Chrome, browser mengekstrak konten dan menempatkannya di lokasi yang sesuai, memungkinkan ekstensi dimuat dan dijalankan di dalam browser.

## Apa format file CRX?

Format file CRX adalah format khusus untuk mengemas dan mendistribusikan ekstensi Google Chrome. Ini pada dasarnya adalah arsip ZIP terkompresi dengan ekstensi file berbeda. Struktur dasar file CRX adalah sebagai berikut:

- **Tanda tangan file:** 4 byte pertama file berisi angka ajaib "Cr24" (heksadesimal: 43 72 32 34) yang berfungsi sebagai tanda tangan untuk mengidentifikasi file sebagai file CRX.
- **Nomor versi:** 4 byte berikutnya mewakili nomor versi format CRX.
- **Panjang kunci publik:** 4 byte berikut menunjukkan panjang kunci publik yang dikodekan yang digunakan untuk verifikasi tanda tangan ekstensi.
- **Panjang tanda tangan:** 4 byte berikutnya menentukan panjang tanda tangan ekstensi.
- **Kunci publik:** Bagian ini berisi kunci publik terkode yang digunakan untuk memverifikasi integritas ekstensi.
- **Tanda Tangan:** Bagian ini berisi tanda tangan ekstensi, yang dihasilkan dengan menandatangani konten ekstensi menggunakan kunci pribadi yang sesuai dengan kunci publik yang disebutkan di atas.
- **Arsip ZIP:** Sisa byte file CRX terdiri dari arsip ZIP terkompresi. Arsip ini berisi semua file dan folder ekstensi yang diperlukan, termasuk file manifes, file JavaScript, file HTML, file CSS, gambar, dan sumber daya lainnya.

## Referensi
* [Spesifikasi format CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

