{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "file", "ekstensi", "format", "apa itu file amr", "musik", "format file amr", "file amr", "konversi file amr ke mp3", "putar file amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file AMR dan API yang dapat membuat, mengonversi, dan membuka file AMR.",
  "title" :"AMR - File Codec Multi-Tingkat Adaptif",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Apa itu file AMR?
File dengan ekstensi .amr adalah format data audio yang relevan dengan codec audio **Adaptive Multi-Rate**; terdiri dari codec ucapan pita sempit multi-tingkat yang mengkodekan sinyal pita sempit pada laju bit 4,75-12,2 kbit/dtk dengan kecepatan bit tol mulai dari 7,4 kbit/dtk; menggunakan adaptasi tautan untuk memilih salah satu dari delapan bit rate yang berbeda berdasarkan.

## Format File AMR
Format file AMR menggunakan banyak teknik pengkodean, algoritma ACELP (Algebraic Code Excited Linear Prediction) salah satu teknik terbaik; dirancang untuk mengompresi audio ucapan manusia dengan cara yang lebih efisien. AMR ditetapkan sebagai codec suara atau ucapan standar oleh 3GPP pada tahun 1999. Format file AMR juga digunakan untuk menyimpan audio yang diucapkan dengan menggunakan codec audio **Adaptive Multi-Rate** yang digunakan oleh banyak ponsel pintar untuk menyimpan rekaman pidato.

### Struktur format file
AMR (Adaptive Multi-Rate) adalah format audio; banyak digunakan di berbagai aplikasi dan perangkat seluler, biasanya di pemutar/perekam audio atau di jenis aplikasi VoIP. AMR dapat diklasifikasikan lebih lanjut sebagai:

1.AMR-NB(NarrowBand)
2.AMR-WB(WideBand)

Biasanya, AMR mengacu pada AMR-NB. Format file AMR memiliki struktur sebagai berikut:

Setiap file AMR berisi header 6 byte yang mengenali file tersebut sebagai audio AMR. Tajuk ini selalu disetel ke:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Ini biasanya serupa di semua file AMR-NB. Jika header mengikuti standar, kemungkinan besar file tersebut rusak dan tidak boleh digunakan. file AMR terdiri dari sejumlah frame audio yang dikemas. Frame ini masing-masing menyusun audio 20ms. Setiap frame dapat dikodekan menggunakan salah satu mode AMR-NB yang valid (0-7, 8 SID dalam mode DTX). Karena frame dapat dikodekan pada kecepatan bit yang berbeda, metode tipikal ini disebut Adaptive Multi-Rate (AMR).
#### mode AMR
Berikut ini adalah mode AMR yang berbeda dan bitrate yang sesuai:

|MODE| TARIF BIT|
---|---|
|0| AMR 4.75 - Mengkodekan pada 4,75 kbit/dtk|
|1 | AMR 5.15 - Mengkodekan pada 5,15 kbit/dtk|
|2 | AMR 5.9 - Mengkodekan pada 5,9 kbit/dtk|
|3 | AMR 6.7 - Mengkodekan pada 6.7kbit/dtk|
|4 | AMR 7.4 - Mengkodekan pada 7,4 kbit/dtk|
|5 | AMR 7.95 - Mengkodekan pada 7,95 kbit/dtk|
|6 | AMR 10.2 - Mengkodekan pada 10,2 kbit/dtk|
|7 | AMR 12.2 - Mengkodekan pada 12.2kbit/dtk|

Ukuran bingkai mode AMR dalam byte (termasuk byte header) diberikan di bawah ini:

|CMR |MODE |FRAME SIZE( dalam byte )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## Referensi ##

* [Codec audio Multi-Rate Adaptif - Oleh Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Format Muatan RTP dan Format Penyimpanan File untuk codec Audio AMR dan AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

