{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format File Cadangan Data CSD Steam Game dan API.",
  "title" :"Format File CSD - File Cadangan Data Game Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Apa itu file CSD?

File CSD adalah file cadangan game yang dihasilkan oleh layanan game **Steam** yang memungkinkan pengguna mengunduh dan mengelola game **Valve**. Ini berisi data cadangan terkait game yang dapat digunakan untuk memulihkan game yang dihapus. Steam hanya dapat mengembalikan game dari file CSD jika game tersebut selesai diunduh, diinstal, dan ditambal melalui Steam. Untuk mengembalikan game dari file CSD, gunakan opsi Steam → Backup and Restore Gamesteam dan pilih file tersebut.

## Format File CSD - Informasi Lebih Lanjut

Struktur internal format file CSD tidak tersedia untuk umum dan spesifikasi format filenya tidak tersedia untuk referensi pengembang. File CSD disertai dengan file CSM dan ISS yang juga merupakan format file game Steam.

### Di mana Menemukan File Cadangan Steam?

Seluruh file cadangan Steam dapat ditemukan di lokasi berikut:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Konfigurasi khusus dan skrip konfigurasi
* \downloads\ - Konten khusus untuk game multipemain
* \maps\ - Peta khusus yang telah dipasang atau diunduh selama permainan multipemain
* \materials\ - Tekstur dan kulit khusus
* \SIMPAN\ - Game tersimpan pemain tunggal

Namun, lokasi game buatan pihak ketiga bisa berbeda dan ditentukan oleh pengembang game tersebut.

### Memulihkan dari File Cadangan CSD

Instal Steam dan masuk ke akun Steam yang benar (lihat Memasang Steam untuk instruksi lebih lanjut)
* Luncurkan Steam
* Klik "Steam" di pojok kiri atas aplikasi Steam
* Pilih "Cadangkan dan pulihkan game..."
* Pilih "Pulihkan cadangan sebelumnya"
* Telusuri ke lokasi file cadangan game
* Lanjutkan melalui jendela Steam untuk menginstal game yang diperlukan.

## Referensi

* [Menggunakan Fitur Steam Backup](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

