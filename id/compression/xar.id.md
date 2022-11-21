{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Format File Arsip yang Dapat Diperluas",
  "description":"Pelajari tentang format file XAR dan API yang dapat membuat dan membuka file XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Apa itu file XAR?

File dengan ekstensi .xar (Extensible Archive Format) adalah arsip UNIX yang mungkin dalam format terkompresi atau non-terkompresi. Itu juga digunakan pada Mac OS untuk instalasi paket. XAR adalah open-source dan menjadi bagian dari Mac OS X 10.5 untuk digunakan dengan browser Safari.

## Format File XAR

File [XAR](https://github.com/mackyle/xar/wiki/xarformat) memiliki tiga wilayah utama.

* Tajuk
* Daftar isi
* Tumpukan

### Tajuk XAR

Header XAR disusun sebagai berikut.

|Bidang|Jenis Data|Ukuran dalam Byte|
---|---|---|
|Sihir|Int Tidak Bertanda tangan 32|4|
|Ukuran|Int Tidak Ditandatangani 16|2|
|Versi|Unsigned Int 16|2|
|Panjang TOC Dikompresi|Int Tidak Ditandatangani 64|8|
|Panjang TOC Tidak Dikompresi|Int Tidak Ditandatangani 64|8|
|Checksum|Int Tidak Ditandatangani 32|4|
|Nama Intisari Pesan |Null Dihentikan||

Struktur C header XAR dapat didefinisikan sebagai berikut.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Perhatikan bahwa semua bidang header (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) selalu disimpan dalam file XAR dalam urutan byte jaringan (alias big endian).

### Daftar Isi XAR (TOC)

Daftar isi adalah dokumen XML yang (dan harus) dikodekan sebagai UTF-8. Itu disimpan di awal file, membuatnya mudah untuk memindai melalui arsip untuk mengekstrak file satu per satu. Arsip XAR memungkinkan Anda mengompres/mengodekan file individual dalam arsip secara mandiri menggunakan skema kompresi yang berbeda seperti [GZIP](/id/compression/gz/), [BZIP2](/id/compression/bz2), dan lainnya yang serupa.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### Tumpukan

Tumpukan dimulai segera setelah toc terkompresi. Ini adalah tumpukan data tidak terstruktur yang direferensikan oleh TOC. Nilai Offset yang tercantum di TOC dimulai dari awal heap. Nilai panjang di toc mengacu pada jumlah byte sebenarnya yang disimpan di heap (dikompresi atau tidak) sedangkan nilai ukuran mengacu pada ukuran item yang diekstraksi (setelah didekompresi jika perlu).

## Referensi

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(arsip))

