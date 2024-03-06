{
  "date": "2022-03-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGZ fails — Gzipped Tar fails",
  "description": "Uzziniet par TGZ faila formātu un API, kas var izveidot un atvērt TGZ failus.",
  "linktitle": "TGZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-lvz"
}
},
  "lastmod": "2022-03-02"
}

## Kas ir TGZ fails?

Fails ar paplašinājumu .tgz ir TAR arhīva fails, kas sastāv no vairākiem failiem un mapēm, kas ir saspiests, izmantojot Gnu Zip (gzip) saspiešanas programmatūru. Fails [TAR](/compression/tar/) parasti apvieno vairākus failus vienā failā dublēšanai vai izplatīšanai internetā. Tas tiek atspiests fails, līdz tas tiek saspiests, izmantojot gzip programmatūru, un pēc tam tas kļūst par TGZ failu. TGZ faili, kas ir saspiesti faili, aizņem mazāk vietas diskā un ir viegli pārsūtāmi, izmantojot internetu, izmantojot e-pastu. Dažas lietojumprogrammas, kas var atvērt TGZ failus, ir WinZip, Apple Archive Utility, 7-Zip un WinRAR. TGZ faili galvenokārt tiek izmantoti UNIX un Linux sistēmās.

## TGZ faila formāts

TGZ faili tiek saglabāti kā saspiesti binārie faili, izmantojot saspiešanas algoritmu [GZ](/compression/gz/).

## Kā izpakot .tgz failu operētājsistēmā Linux

Operētājsistēmā Linux/Unix OS var izmantot šādu komandu, lai izpakotu TGZ failus no komandrindas.

```
tar zxvf tgzCompressedFile.tgz
```

Iepriekš minētā komanda atspiež saspiesto TGZ failu un izvelk tā failus no TAR arhīva diskā.
## Atsauces Nr.

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip — Wikipedia](https://en.wikipedia.org/wiki/Gzip)


