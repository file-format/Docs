{
  "date": "2019-10-11",
  "keywords": [
"mng failu",
"mng faila formātā",
"kas ir mng fails",
"failu",
"mng piemērs",
"mng faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MNG faila formāts — vairāku attēlu tīkla grafikas faila formāts",
  "description": "Uzziniet par MNG failu formātu un API, kas var izveidot un atvērt MNG failus.",
  "linktitle": "MNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-mn-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir MNG fails?

Fails ar paplašinājumu .mng ir vairāku attēlu tīkla grafikas faila formāts, kas ir līdzīgs attēla formātam [PNG](/image/png/), bet atbalsta animētus attēlus. Tas tika izstrādāts, lai izvairītos no PNG formāta pārslodzes ar papildu animācijas funkciju. MNG ir arī līdzīgs [GIF](/image/gif/) failiem, taču izmanto vairāk saspiešanas un atbalsta pilnu alfa funkciju. MNG failu neoficiālais MIME multivides veids ir video/x-mng. MNG failus var atvērt tādās lietojumprogrammās kā ImageMagik un IrfanView.

## MNG faila formāts

MNG faila formāts ir līdzīgs PNG faila formātam un izmanto to pašu gabala struktūru, kas noteikta PNG specifikācijās. MNG dekodētājam jāspēj atšifrēt PNG datu straumes, nenorādot nekādus īpašus karodziņus dekodēšanas instrukcijām. MNG grupē vairākus attēlus kopā rāmī, un daži attēli tiek izmantoti kā sprite, lai pārvietotos no vienas vietas uz citu. Mehānisms ļauj atkārtoti izmantot attēla datus, tos nepārsūtot. Izstrādātāju uzziņai var izmantot [MNG specifications](http://www.libpng.org/pub/mng/spec/).

### MNG paraksts

MNG datu straume sākas ar 8 baitu parakstu, kas satur:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Tas ir līdzīgs PNG parakstam, bet satur MNG, nevis PNG.

### MNG rāmis

MNG rāmis sastāv no mazāku attēlu divdimensiju attēla. Katram mazajam attēlam var piekļūt, izmantojot rindu un kolonnu indeksa kombināciju. Formāts spēj saglabāt trīsdimensiju vokseļu datus, kas ir sakārtoti divdimensiju plakņu sērijā. Katru plakni attēlo PNG vai Delta-PNG datu plūsma. Katra Delta-PNG datu straume definē attēlu kā atšķirības no sākotnējā PNG attēla. Tas nodrošina daudz kompaktāku veidu, kā attēlot nākamos attēlus, nekā katram izmantot pilnu PNG datu straumi.

## Atsauces Nr.

* [MNG](http://www.libpng.org/pub/mng/)

* [MNG formāts v1.0](http://www.libpng.org/pub/mng/spec/)


