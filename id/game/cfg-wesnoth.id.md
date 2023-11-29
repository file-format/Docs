{
"tanggal": "27-09-2023",
  "keywords": [
"cfg",
"file cfg",
"file bahasa markup cfg wesnoth",
"apa itu file cfg",
"cara membuka file cfg",
"mengajukan",
"ekstensi file cfg",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File CFG - File Bahasa Markup Wesnoth",
  "description":"Pelajari tentang format File CFG Wesnoth Markup Language dan API yang dapat membuat dan membuka file CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent" : "game"
}
},
"mod terakhir": "27-09-2023"
}

## Apa itu file CFG?

File CFG juga dikenal sebagai **"Wesnoth Markup Language" (WML)**. Ini adalah bahasa markup khusus yang digunakan terutama dalam game "Battle for Wesnoth", yang merupakan game strategi berbasis giliran. WML digunakan untuk mendefinisikan dan menyesuaikan berbagai aspek permainan, termasuk skenario, kampanye, unit, dan banyak lagi. Ini adalah cara bagi modder dan pengembang untuk membuat konten untuk game.

Itu ditulis dalam format yang menyerupai kombinasi XML dan skrip sederhana. Berikut ini ikhtisar beberapa elemen dan struktur umum yang mungkin Anda temukan dalam file WML:

1. **Tag:** WML menggunakan tag untuk mendefinisikan berbagai elemen dalam game. Tag diapit dalam tanda kurung siku. Misalnya:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atribut:** Di dalam tag, Anda dapat menentukan atribut untuk menentukan properti atau nilai yang terkait dengan elemen. Pada contoh di atas, "type" dan "hitpoints" adalah atribut.
    










3. **Array dan Array dari Array:** Anda dapat membuat array data dan bahkan array dari array untuk menentukan daftar unit, jenis medan, atau elemen permainan lainnya.
    










4. **Pernyataan Bersyarat:** WML mendukung pernyataan bersyarat untuk mengontrol alur permainan. Misalnya:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Perulangan:** Anda dapat menggunakan perulangan untuk mengulangi daftar item atau melakukan tindakan berulang kali.
    










6. **Termasuk:** Anda dapat menyertakan file WML lain dalam file WML utama untuk mengatur dan memodulasi konten Anda.
    










7. **Penanganan Peristiwa:** Anda dapat menentukan penangan peristiwa untuk memicu tindakan ketika peristiwa tertentu terjadi dalam game.
    











Berikut adalah contoh sederhana dari file WML yang mendefinisikan unit khusus:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Pertempuran untuk Wesnoth

"The Battle for Wesnoth" adalah game strategi berbasis giliran yang populer dan bersumber terbuka. Ini tersedia untuk berbagai platform, termasuk Mac, Windows, Linux, dan banyak lagi. Dikembangkan oleh komunitas sukarelawan yang berdedikasi, game ini terkenal dengan gameplaynya yang mendalam dan menarik, serta dunia fantasinya yang kaya.

Fitur utama "Pertempuran untuk Wesnoth" meliputi:

1. **Pengaturan Fantasi:** Game ini berlatar dunia fantasi dengan berbagai ras, termasuk manusia, elf, kurcaci, orc, dan banyak lagi. Pengetahuan dan penceritaan game ini merupakan bagian integral dari daya tariknya.
    










2. **Strategi Berbasis Giliran:** Gameplaynya berbasis giliran, di mana pemain meluangkan waktu untuk merencanakan dan mengeksekusi gerakan mereka pada kotak heksagonal. Ini menggabungkan pertempuran taktis dengan pengambilan keputusan strategis.
    










3. **Kampanye:** Game ini menawarkan beragam kampanye pemain tunggal, masing-masing dengan alur cerita, karakter, dan tantangannya sendiri. Pemain dapat menjelajahi narasi dan skenario yang berbeda.
    










4. **Multipemain:** "Wesnoth" mendukung multipemain daring, memungkinkan pemain bersaing satu sama lain dalam pertempuran strategis. Mode multipemain mencakup permainan kooperatif dan pertandingan kompetitif.

## Bagaimana cara membuka file CFG?

File CFG, yang umumnya dikaitkan dengan Wesnoth Markup Language (WML) yang digunakan dalam game "The Battle for Wesnoth", dapat dengan mudah diedit menggunakan editor teks standar apa pun. File-file ini berisi kode yang dapat dibaca manusia yang ditulis dalam WML, yang mendefinisikan berbagai aspek permainan, termasuk skenario, unit, dan kampanye.

Meskipun Anda dapat menggunakan editor teks apa pun untuk memodifikasi file CFG, beberapa editor teks tingkat lanjut seperti Emacs dan Vi menyediakan plugin penyorotan sintaksis WML. Plugin ini menyediakan pengkodean warna dan pemformatan yang berguna untuk memudahkan pengguna membedakan berbagai elemen dan struktur dalam kode WML.

Program yang membuka atau mereferensikan file CFG termasuk

- Pertempuran Wesnoth (Gratis) untuk (Windows, MAC, Linux)
- Microsoft Buku Catatan

## File CFG lainnya

Berikut jenis file lain yang menggunakan ekstensi file **.cfg**.

**Pengaturan**
- [CFG - File Konfigurasi Celestia](/id/settings/cfg-celestia/)
- [CFG - File Koneksi Server Citrix](/id/settings/cfg-citrix/)
- [CFG - File Konfigurasi MAME](/id/settings/cfg-mame/)
- [CFG - File Konfigurasi LightWave](/id/settings/cfg-lightwave/)

**Permainan**
- [CFG - File Bahasa Markup Wesnoth](/id/game/cfg-wesnoth/)
- [CFG - File Konfigurasi MUGEN](/id/game/cfg-mugen/)
- [CFG - File Konfigurasi Mesin Sumber](/id/game/cfg-sourceengine/)

**Sistem & Lainnya**
- [CFG - Berkas CFG](/id/system/cfg/)
- [CFG - File Konfigurasi Model Cal3D](/id/misc/cfg-cal3d/)

## Referensi
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
