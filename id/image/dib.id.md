{
  "date" : "2020-01-10",
  "keywords" :[ "file dib", "format file dib", "apa itu file dib", "file", "contoh dib", "ekstensi file dib", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Pelajari tentang format file DIB dan API yang dapat membuat dan membuka file DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Apa itu file DIB?

Device-Independent bitmap (DIB) adalah file gambar raster yang strukturnya mirip dengan file Bitmap standar ([BMP]()/image/bmp/)). Ini berisi tabel warna yang menjelaskan pemetaan warna RGB ke nilai piksel. Ini memungkinkan DIB untuk merepresentasikan gambar di perangkat apa pun. Itu dapat dibuka dengan hampir semua aplikasi yang dapat membuka file BMP standar di Windows dan juga macOS. DIB adalah file biner dan memiliki format file kompleks yang mirip dengan BMP. Gambar DIB tidak bergantung pada kemampuan keluaran perangkat rendering dalam hal kedalaman warna dan piksel per inci.

## Spesifikasi Format File DIB ##
DIB berisi informasi warna dan dimensi berikut:

* Format warna perangkat tempat gambar persegi panjang dibuat.
* Resolusi perangkat tempat gambar persegi panjang dibuat.
* Palet untuk perangkat tempat gambar dibuat.
* Larik bit yang memetakan triplet merah, hijau, biru ( RGB ) ke piksel dalam gambar persegi panjang.
* Pengidentifikasi kompresi data yang menunjukkan skema kompresi data (jika ada) yang digunakan untuk mengurangi ukuran larik bit.

### Format Blok Data DIB ###

DIB hadir dalam konteks blok memori dibandingkan dengan file .DIB yang disimpan di disk. Blok memori terdiri dari struktur yang sesuai dengan spesifikasi Windows API untuk DIB. DIB aktual terdiri dari:
* Sebuah tajuk
* Palet warna
* Data Piksel

Secara praktis, bekerja dengan data palet, header, dan gambar dilakukan seolah-olah mereka adalah tiga blok memori yang terpisah. Pegangan untuk blok memori umum ini ditetapkan menggunakan GlobalAlloc dan dikenal sebagai HDIB, yang digunakan untuk mengekstrak dan bekerja dengan header, tabel warna, dan data piksel.

### Struktur ###
Informasi yang terkandung dalam DIB diwakili oleh struktur yang berbeda. Ini termasuk:

BITMAPInfo - Menentukan informasi dimensi dan warna untuk DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Ini terdiri dari BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
diikuti oleh dua atau lebih struktur RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bit Data ###
|Bit|Deskripsi|
---|---|
|Format 1-bit (monokrom)|Bitmap monokrom terdiri dari dua warna (hitam dan putih). Karena jumlah warna yang terbatas ini, bitmap ini memakan lebih sedikit ruang pada disk. BitBitCount mengembalikan benar atau salah untuk mewakili kedua warna. Sebagian besar aplikasi melewati palet sepenuhnya jika bitBitCount==1.
|Format 4 bit (VGA atau 16 warna)|Setiap byte data gambar mewakili dua piksel dan bitBitCount==4. Bit-bit ini mewakili warna piksel dalam urutan menurun.
|Format 8 bit (256 warna)|Format 8-bit ini dapat mewakili maksimal 256 warna. Setiap byte dalam larik data bitmap gambar mewakili satu piksel. Nilai byte itu adalah nomor entri palet warna yang akan digunakan dari 256 entri yang diwakili oleh bmciColors.
|24 bit format (TrueColor)|Bitmap ini dapat memiliki maksimal 2^24 warna (biBitCount == 24). Setiap urutan tiga byte dalam larik data bitmap mewakili intensitas relatif dari tiga rona utama piksel. Rona digambarkan sebagai nilai mulai dari 0 hingga 255 dan disimpan dalam tiga byte dalam urutan Biru, Hijau, dan Merah. Ini adalah perbedaan penting, karena sebagian besar referensi warna di Windows menggunakan urutan yang berlawanan: Merah/Hijau/Biru, jadi pikirkan "BGR" saat bekerja dengan gambar TrueColor, bukan "RGB". Palet warna dapat ditentukan untuk mempercepat proses menggambar untuk Windows, dalam hal ini biClrUsed tidak akan menjadi 0. Tapi seperti yang Anda lihat, ini tidak diperlukan, karena data piksel itu sendiri berisi informasi warna.
|Format 32 bit|Gambar 32 bit memiliki maksimum 2^24 warna (biBitCount == 24).

## Referensi ##
* [Bitmap Perangkat-Independen - Oleh Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

