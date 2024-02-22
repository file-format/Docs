{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Skrip shell - Cara menjalankannya di Ubuntu dan Linux",
  "description":"Pelajari tentang apa itu Shell Script dan cara menjalankannya di Ubuntu dan Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-id",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Apa itu Skrip Shell?

Skrip shell melibatkan penulisan serangkaian perintah dalam file teks biasa, sering disebut sebagai **Skrip Shell**. Skrip ini dijalankan oleh shell, yang merupakan penerjemah baris perintah. Kerang yang paling umum termasuk

1. Bash (Bourne Lagi SHell)
2. Zsh (Z Cangkang)
3. Ikan.

Skrip shell dapat berkisar dari yang sederhana hingga program yang kompleks, dan skrip tersebut digunakan untuk melakukan berbagai macam tugas, seperti manipulasi file, administrasi sistem, dan otomatisasi tugas yang berulang.

## Manfaat Skrip Shell:

1.  **Otomasi:** Skrip Shell memungkinkan pengguna mengotomatiskan tugas yang berulang, menghemat waktu, dan mengurangi kemungkinan kesalahan manusia.
    
2.  **Penyesuaian:** Pengguna dapat membuat skrip yang disesuaikan dengan kebutuhan spesifik mereka, sehingga memberikan penyesuaian tingkat tinggi.
    
3.  **Pemrosesan Batch:** Skrip Shell sangat baik untuk menangani tugas pemrosesan batch, yang mengharuskan beberapa perintah dijalankan secara berurutan.
    
4.  **Administrasi Sistem:** Skrip shell biasanya digunakan untuk tugas administrasi sistem, seperti pencadangan, rotasi log, dan instalasi perangkat lunak.

## Menulis Skrip Shell Sederhana:

Mari kita membuat skrip shell dasar yang mencetak pesan ucapan. Buka editor teks dan buat file bernama `greeting.sh`. Tambahkan baris berikut:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Simpan file dan buat agar dapat dieksekusi dengan menjalankan perintah berikut di terminal:

```
chmod +x greeting.sh
```

Sekarang, Anda dapat menjalankan skrip:

```
./greeting.sh
```

Outputnya harus:

```
Hello, welcome to the world of shell scripting!
```

## Menjalankan Skrip Shell di Ubuntu dan Linux:

Sekarang, kita akan membahas **cara menjalankan file .sh di Ubuntu dan Linux**.

1.  **Membuat Skrip Dapat Dieksekusi:** Sebelum menjalankan skrip shell, pastikan skrip dapat dieksekusi. Gunakan perintah `chmod` seperti yang ditunjukkan sebelumnya.
    
2.  **Navigasi ke Direktori Skrip:** Buka terminal dan gunakan perintah `cd` untuk menavigasi ke direktori yang berisi skrip shell Anda.
    
3.  **Jalankan Skrip:** Jalankan skrip dengan mengetik `./scriptname.sh` di terminal, ganti scriptname dengan nama skrip Anda yang sebenarnya.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Menggunakan Perintah Bash:** Jika skrip Anda dimulai dengan `#!/bin/bash` (dikenal sebagai **shebang**), Anda juga dapat menjalankannya menggunakan perintah `bash`.

```
bash greeting.sh
```

## Apa arti $@ dalam Skrip Shell?

Dalam skrip shell, `$@` mewakili semua argumen baris perintah yang diteruskan ke skrip. Ini sering digunakan untuk mereferensikan daftar argumen sebagai entitas terpisah. Ketika digunakan dalam tanda kutip ganda, seperti `$@`, argumen individual akan dipertahankan, dengan memperhitungkan spasi dan karakter khusus.

Berikut penjelasan singkatnya:

- `$@`: Mewakili semua parameter posisi (argumen) yang diteruskan ke skrip atau fungsi. Setiap argumen diperlakukan sebagai kata terpisah.
    
- `$@`: Saat dikutip ganda, mempertahankan pemisahan argumen, memungkinkan adanya spasi atau karakter khusus dalam masing-masing argumen.
    

Berikut ini contoh sederhana untuk diilustrasikan:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Saat Anda menjalankan skrip ini dengan argumen, misalnya:

```
bash example.sh arg1 "argument 2" arg3
```

Ini akan menghasilkan:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Seperti yang Anda lihat, `$@` mewakili semua argumen, dan `$@` mempertahankan masing-masing argumen, meskipun argumen tersebut mengandung spasi.

