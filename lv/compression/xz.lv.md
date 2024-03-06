{
  "date": "2022-01-23",
  "keywords": [
"xz failu",
"faila formātā",
"kas ir xz fails",
"failu",
"xz piemērs",
"xz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XZ fails — XZ saspiests arhīvs",
  "description": "Uzziniet par XZ faila formātu un API, kas var izveidot un atvērt XZ failus.",
  "linktitle": "XZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-x-lvz"
}
},
  "lastmod": "2022-01-23"
}

## Kas ir XZ fails?

XZ ir saspiests faila formāts, kas izmanto LZMA2 saspiešanas algoritmu. Tas tika izstrādāts, lai aizstātu populāros gzip un bzip2 formātus, un piedāvā vairākas priekšrocības salīdzinājumā ar šiem vecākajiem standartiem. XZ faili tiek labi atbalstīti daudzās platformās, un tos var ātri un viegli atspiest. Lai gan tie nav tik izplatīti kā [ZIP](/compression/zip/) vai [RAR](/compression/rar/) faili, XZ arhīvus var izmantot, lai uzglabātu lielu datu apjomu, nezaudējot saspiešanas kvalitāti. Ja nepieciešams saspiest vai atspiest lielus failus, ir vērts apsvērt XZ faila paplašinājumu.

## XZ faila formāts

XZ fails tiek ģenerēts un saglabāts diskā kā bināri faili. Tas izmanto LZMA algoritmu, lai saspiestu datus, un var sasniegt saspiešanas pakāpi līdz 50%. XZ faili parasti tiek izmantoti programmatūras izplatīšanai un rezerves arhīviem. Tos var atspiest, izmantojot XZ utilītu, kas ir iekļauta lielākajā daļā Linux izplatījumu.

## Izpakojiet XZ failus operētājsistēmā Linux/Unix

Lai izspiestu XZ failus, vispirms instalējiet pakotni `xz-utils':
```
$ sudo apt-get install xz-utils
```

Izmantojiet komandu unxz, lai izvilktu .xz failus:
```
$ unxz compressed_xz_file.xz
```

vai izmantojot XZ opciju --decompress:
```
$ xz --decompress compressed_xz_file.xz
```

## Atsauces

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


