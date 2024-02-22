{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"File GCODE - Apa itu file .gcode dan bagaimana cara membukanya?",
   "description":"Pelajari tentang format file GCODE dan API yang dapat membuat dan membuka file GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-id",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Apa itu file GCODE?

**File GCODE** adalah file teks biasa yang berisi instruksi untuk mengendalikan peralatan mesin terkomputerisasi dan printer 3D; G-code, atau Kode Geometris, adalah bahasa yang digunakan untuk mengontrol pergerakan dan tindakan mesin **CNC (Computer Numerical Control)**; Mesin CNC meliputi mesin penggilingan, mesin bubut, router, dan printer 3D.

Perintah kode-G ditulis dalam sintaksis tertentu yang biasanya terdiri dari huruf dan angka; setiap perintah memerintahkan mesin untuk melakukan tindakan tertentu seperti memindahkan alat ke posisi tertentu, mengganti alat atau menyesuaikan kecepatan.

Kode-G sering kali dihasilkan oleh perangkat lunak **CAM (Computer-Aided Manufacturing)**; Perangkat lunak CAM mengambil model 3D atau desain 2D dan menghasilkan jalur alat dan instruksi kode-G yang sesuai; file kode-G kemudian dimuat ke mesin CNC atau printer 3D untuk dieksekusi.

File G-code biasanya memiliki ekstensi file .nc atau .gcode, misalnya, program.nc atau print.gcode.

## Struktur File GCODE:

File GCODE adalah file teks biasa dengan setiap baris berisi perintah tertentu; perintah-perintah ini berkisar dari mengendalikan pergerakan mesin hingga menyesuaikan suhu, kecepatan, dan parameter lain yang penting untuk pembuatan suatu objek.

Sintaks GCODE melibatkan kombinasi huruf dan angka; masing-masing mewakili tindakan atau parameter yang berbeda; perintah umum termasuk G0 dan G1 untuk pergerakan, M3 dan M5 untuk kontrol spindel, dan S dan F untuk penyesuaian kecepatan dan laju umpan.

## Generasi GCODE:

Perangkat lunak pengiris seperti **Simplify3D** dan **Slic3r**, menerjemahkan gambar Computer-Aided Design (CAD) ke dalam GCODE; Perangkat lunak CAD digunakan untuk membuat model 3D, yang kemudian diekspor dalam format seperti STL; perangkat lunak pengiris mengambil model ini dan menghasilkan file GCODE yang menentukan detail seperti tinggi lapisan, kecepatan pencetakan, dan pengaturan suhu.

## Contoh GCODE

Berikut contoh sederhana G-code untuk menggerakkan mesin CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Bagaimana cara membuka file GCODE?

Untuk membuka file G-code Anda dapat menggunakan berbagai jenis perangkat lunak tergantung kebutuhan Anda.

Jika Anda membuat kode G untuk printer 3D; Anda dapat membukanya menggunakan perangkat lunak yang disertakan dengan printer 3D Anda atau perangkat lunak pengiris khusus; contohnya termasuk **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** atau **Repetier-Host**; program ini sering kali memiliki antarmuka ramah pengguna yang memungkinkan Anda memuat dan memvisualisasikan kode-G.

File GCODE adalah teks biasa sehingga Anda dapat membukanya dengan editor teks apa pun; editor teks yang umum mencakup **Notepad (di Windows)**, **TextEdit (di macOS)**, atau **Gedit (di Linux)**; cukup **klik kanan** pada file G-code, pilih **Buka dengan,** dan pilih editor teks.

