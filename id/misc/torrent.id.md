{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File Torrent - File BitTorrent",
  "description":"Pelajari tentang file TORRENT dan API yang dapat membuat dan membuka file TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Apa itu file TORRENT?

File TORRENT adalah file teks yang digunakan oleh BitTorrent dan program P2P (peer-to-peer) lainnya untuk mengunduh dan bertukar konten. Konten yang dapat diunduh dapat mencakup dokumen, video, game, film, dan media lain yang tersedia di internet. Ini mencakup informasi metadata tentang konten dan lokasi media yang akan diunduh. Perangkat lunak seperti BitTorrent menggunakan informasi dari file ini seperti nama, ukuran file, dan struktur folder untuk mengunduh data. File torrent dapat dikonversi ke format file lain seperti [PDF](/id/pdf/) online.

## Apa itu Torrent? Format File TORRENT untuk Pertukaran Data

Torrenting adalah konsep pertukaran (mengunduh dan mengunggah) file data menggunakan jaringan BitTorrent. Tidak seperti server konvensional di mana data diunggah untuk diakses dan diunduh orang lain, file torrent diambil dan dikirim menggunakan jaringan torrent. Saat pengguna membuka file .torrent di aplikasi seperti BitTorrent, perangkat lunak mulai mengunduh konten file secara bitwise. Jika banyak pengguna memiliki file yang sama, BitTorrent membagi unduhan di antara semua pengguna untuk mempercepat proses pengunduhan. Pada saat yang sama, komputer pengguna yang mengunduh file juga menjadi sumber file untuk mengirimkannya ke pengguna lain yang juga mengunduh file yang sama.

### Struktur File TORRENT

File torrent adalah kombinasi dari daftar file dan informasi metadata tentang semua bagian file yang akan diunduh. Ini berisi informasi berikut dalam bentuk kunci.

- `announce` — URL pelacak yang diumumkan ke peer lain untuk menginformasikan tentang ketersediaan file
- `info` — Ini memetakan ke kamus yang kuncinya bergantung pada apakah satu atau lebih file sedang dibagikan:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `panjang` — ukuran file dalam byte.
- `path` — daftar string yang sesuai dengan nama subdirektori, yang terakhir adalah nama file sebenarnya
- `panjang` — ukuran file dalam byte (hanya jika satu file dibagikan)
- `nama` — nama file tempat file akan disimpan
- `panjang bagian` — jumlah byte per bagian. Ini biasanya 28 KiB = 256 KiB = 262.144 B.
- `pieces` — daftar hash yang merupakan gabungan dari setiap hash SHA-1 setiap bagian.

## Apakah Torrenting Aman dan Legal?

Protokol torrent untuk pertukaran data antara pengguna P2P aman karena ini hanyalah cara untuk berbagi semua jenis file. Dengan demikian, protokol itu sendiri tidak aman atau ilegal. Namun, konten yang dibagikan melalui jaringan mungkin berisi file atau media yang dapat melanggar status hukum dokumen yang dibagikan. Dalam kasus seperti itu, pertukaran data tersebut dapat menyebabkan tindakan hukum terhadap pihak yang terlibat dalam berbagi file tersebut secara publik.

## Referensi

* [File TORRENT - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

