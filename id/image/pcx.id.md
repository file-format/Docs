{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PCX - File Gambar Bitmap Kuas",
  "description":"Pelajari tentang format file PCX dan API yang dapat membuat dan membuka file PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Apa itu file PCX?

File PCX, file Picture Exchange, adalah format file gambar raster yang digunakan sebagai format file asli untuk aplikasi Kuas PC. Ini dikembangkan oleh ZSoft Corporation, AS untuk platform DOS dan Windows dan diadopsi sebagai format file pencitraan utama sebelum kedatangan [BMP](/id/image/bmp/), [JPEG](/id/image/jpeg/), dan [ PNG](/id/image/png/) format file. File PCX berukuran lebih kecil karena dikompres menggunakan pengkodean RLE. Ini digunakan dalam file [DCX](/id/image/dcx/) multi-halaman yang terutama digunakan untuk membuat file faks digital.

## Format File PCX

File PCX disimpan ke disk dalam format file biner. Struktur format file internal mengikuti urutan byte endian kecil dan memiliki tiga bagian berikut:

**`PCX Header`** - Panjang PCX Header adalah 128 byte. Ini berisi pengenal, nomor versi, dimensi gambar, 16 warna palet, bidang warna angka dan kedalaman bit setiap bidang, dan nilai untuk metode kompresi.

Header PCX seperti yang ditunjukkan di bawah ini dengan referensi dari Ensiklopedia format file grafik (2nd ed.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Data Gambar`** - Data gambar PCX mengikuti tepat setelah header. Data gambar dapat dikompresi tergantung pada pengaturan bidang di header. Penyimpanan data dalam file PCX bergantung pada jumlah bidang warna yang ditentukan. Data gambar diatur dalam baris. Dalam kasus beberapa bidang, ini disimpan oleh bidang dalam baris dalam susunan berurutan dari data merah, hijau dan biru. Pola ini diulangi untuk setiap garis pada bidang.

## Referensi

* [PCX - Oleh Wikipedia](https://en.wikipedia.org/wiki/PCX)

