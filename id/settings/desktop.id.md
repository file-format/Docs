{
"tanggal": "31-05-2023",
  "keywords": [
"berkas desktop",
"apa itu file desktop",
"apa isi file desktop",
"contoh file desktop",
"cara membuka file desktop",
"apa format file desktop",
"mengajukan",
"ekstensi file desktop",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File DESKTOP - File Entri Desktop",
  "description":"Pelajari tentang format DESKTOP dan API yang dapat membuat dan membuka file DESKTOP.",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "pengaturan"
}
},
"mod terakhir": "31-05-2023"
}

## Apa itu file DESKTOP?

File .desktop adalah file konfigurasi yang digunakan oleh lingkungan desktop Linux untuk menentukan pintasan dan peluncur aplikasi. Ini memberikan metadata tentang aplikasi seperti nama, ikon, perintah untuk mengeksekusi dan properti lainnya. File-file ini biasanya digunakan untuk membuat pintasan di menu aplikasi, peluncur desktop, atau panel di sistem berbasis Linux.

## Apa isi file DESKTOP?

File .desktop mengikuti format tertentu dan berisi beberapa bidang utama:

- **[Entri Desktop]:** Ini adalah header bagian utama untuk file .desktop.
- **Nama:** Menentukan nama aplikasi.
- **Komentar:** Memberikan deskripsi atau komentar singkat tentang aplikasi.
- **Exec:** Mendefinisikan perintah untuk dijalankan saat meluncurkan aplikasi.
- **Ikon:** Menentukan jalur ke file ikon yang terkait dengan aplikasi.
- **Terminal:** Menentukan apakah aplikasi harus dijalankan di jendela terminal.
- **Jenis:** Menentukan jenis entri seperti "Aplikasi" atau "Tautan".
- **Kategori:** Menentukan kategori atau grup tempat aplikasi akan ditampilkan dalam menu.
- **StartupNotify:** Menentukan apakah lingkungan desktop harus menampilkan pemberitahuan startup untuk aplikasi.
- **NoDisplay:** Menentukan apakah aplikasi harus disembunyikan dari menu.
- **Tindakan:** Menentukan tindakan tambahan yang dapat dilakukan pada aplikasi seperti membuka file tertentu.

## Contoh file DESKTOP

Berikut ini contoh file .desktop untuk editor teks fiktif bernama "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Dalam contoh ini, file .desktop mendefinisikan aplikasi "MyTextEditor" dengan properti terkaitnya. Ini juga mencakup dua tindakan tambahan, "Buka Jendela Baru" dan "Buka File yang Ada", yang dapat diakses dari menu konteks peluncur aplikasi.

Dengan menempatkan file .desktop di direktori tertentu seperti `/usr/share/applications` atau `~/.local/share/applications`, lingkungan desktop akan mengenalinya dan menampilkan aplikasi yang sesuai di menu atau mengizinkannya diluncurkan dari Desktop.

## Bagaimana cara membuka file DESKTOP?

Beberapa program perangkat lunak dapat membuka dan menangani file .desktop. Program-program ini biasanya berupa pengelola file atau lingkungan desktop pada sistem berbasis Linux. Berikut beberapa contohnya:

- **Nautilus (File):** Manajer file default untuk lingkungan desktop GNOME.
- **Nemo:** Pengelola file untuk lingkungan desktop Cinnamon.
- **Dolphin:** Manajer file default untuk lingkungan desktop KDE Plasma.
- **Thunar:** Manajer file default untuk lingkungan desktop Xfce.
- **KDE Menu Editor:** Alat khusus untuk lingkungan desktop KDE Plasma yang memungkinkan Anda melihat dan mengedit file .desktop.

Manajer file dan lingkungan desktop ini menyediakan antarmuka grafis untuk mengelola file .desktop. Mereka memungkinkan Anda melihat dan mengedit properti file .desktop, membuat peluncur aplikasi dan mengatur pintasan di menu aplikasi atau di desktop.

File .desktop adalah file teks biasa, jadi Anda juga dapat membuka dan mengeditnya dengan editor teks pilihan Anda. Cukup klik kanan pada file .desktop dan pilih "Buka dengan" atau "Buka dengan aplikasi lain" untuk memilih editor teks dari daftar program yang diinstal.

## Apa format file DESKTOP?

Format file .desktop mengikuti struktur dan format tertentu. Ini adalah file teks biasa dengan sekumpulan pasangan nilai kunci yang disusun menjadi beberapa bagian. Berikut ini ikhtisar formatnya:

- **Header Bagian:** Setiap bagian diawali dengan header yang diapit tanda kurung siku ([]). Bagian utama biasanya diberi nama [Entri Desktop], yang berisi metadata utama untuk aplikasi atau peluncur.
- **Pasangan Nilai-Kunci:** Dalam setiap bagian, Anda menentukan properti menggunakan pasangan nilai-kunci. Formatnya adalah "Kunci=Nilai". Kuncinya mengidentifikasi properti dan nilai menyediakan data yang sesuai.
- **Sintaks Properti:** Nilai properti dapat berupa tipe berbeda termasuk string, nilai boolean, jalur file, atau daftar. Format untuk setiap nilai properti bergantung pada tipenya.
- **Komentar:** Anda dapat memasukkan komentar dalam file .desktop menggunakan simbol '#'. Apa pun yang mengikuti '#' pada baris dianggap sebagai komentar dan diabaikan.

## Referensi
* [File Entri Desktop](https://www.baeldung.com/linux/desktop-entry-files)

