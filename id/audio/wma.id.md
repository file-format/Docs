{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "file", "ekstensi", "format", "format file interchange audio", "musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file WMA dan API yang dapat membuat dan membuka file WMA.",
  "title" :"WMA - Berkas Audio Media Windows",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Apa itu file WMA?

File dengan ekstensi .wma mewakili file audio yang disimpan dalam format Advanced Systems Format (ASF). ASF adalah format milik Microsoft yang berisi bitstream yang disandikan oleh Windows Media Audio 9. Selain konten audio, file WMA juga berisi objek metadata seperti judul, album, artis, dan genre trek. File WMA terutama digunakan untuk streaming melalui web mirip dengan file [.mp3](/id/audio/mp3/).

## Format File WMA

File WMA adalah format file biner dan terkandung dalam format file ASF. Ini menentukan pengkodean metadata tentang file yang mirip dengan tag ID3 yang digunakan oleh file MP3. Codec WMA telah digunakan oleh Microsoft dalam Protected Interoperable File Format (PIFF) sejak 2008. Namun, ini belum dinyatakan sebagai codec audio standar oleh standar industri terkait seperti DECE UltraViolet dan MPEG-DASH.

### Data Spesifik Jenis WMA

Informasi khusus tipe untuk codec Windows Media Audio disimpan dalam format berikut sebagai bagian dari Data Tipe-Spesifik dari Objek Properti Stream.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referensi

* [Ikhtisar ASF - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

