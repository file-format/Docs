{
  "date": "2023-05-16",
  "keywords": [
"sāmu fails",
"kas ir sāmu fails",
"sami faila piemērs",
"failu",
"sami faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI faila formāts — subtitru un metadatu apmaiņas fails",
  "description": "Uzziniet par SAMI formātu un API, kas var izveidot un atvērt SAMI failus.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-lv",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## Kas ir SAMI fails?

Fails ar paplašinājumu .sami parasti attiecas uz subtitru un metadatu apmaiņas (SAMI) failu. SAMI ir parakstu formāts, ko izmanto subtitru rādīšanai videoklipos. Sākotnēji to izstrādāja Microsoft savam Windows Media Player.

SAMI faili satur laika informāciju un teksta saturu subtitriem, kas ļauj tos sinhronizēt ar video atskaņošanu. Formāts atbalsta pamata formatēšanas opcijas, piemēram, fonta stilu, krāsu un subtitru novietojumu ekrānā.

SAMI faili parasti ir vienkārša teksta faili, un tos var atvērt un rediģēt, izmantojot teksta redaktoru. SAMI faila saturs parasti ietver galvenes sadaļu, kas sniedz informāciju par failu, kam seko atsevišķi subtitru ieraksti ar attiecīgo laiku un tekstu.

Šeit ir piemērs tam, kā varētu izskatīties SAMI fails:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI faili parasti tiek izmantoti kopā ar video atskaņotājiem vai multivides atskaņotājiem, kas atbalsta subtitru attēlojumu, piemēram, Windows Media Player vai VLC Media Player. Atskaņotājs nolasa SAMI failu un sinhronizē subtitrus ar video saturu, ļaujot skatītājiem videoklipa skatīšanās laikā lasīt parakstus.

## Atbalstītie HTML tagi

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` Saknes elements, kas iekapsulē visu SAMI failu.
- ``<HEAD> :`` Satur SAMI faila galvenes informāciju.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` Nosaka fonta rekvizītus pievienotajam tekstam. Lai mainītu fonta izskatu, var izmantot tādus atribūtus kā krāsa, seja, izmērs un stils.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` Atveido pievienoto tekstu treknrakstā.</b>
- `` <I>:`` Atveido pievienoto tekstu slīprakstā.</i>
- `` <U>:`` Padara pievienoto tekstu pasvītrotu.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

Šie ir daži no pamata tagiem, ko atbalsta SAMI faili. Ir svarīgi atzīmēt, ka SAMI neatbalsta visu HTML tagu un atribūtu klāstu. Atbalstītie tagi galvenokārt ir vērsti uz subtitru stilu un novietojumu, nevis nodrošina plašu dokumentu strukturēšanu vai interaktivitāti.

## Atsauces
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


