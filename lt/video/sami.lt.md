{
  "date": "2023-05-16",
  "keywords": [
"sami failas",
"kas yra sami failas",
"sami failo pavyzdys",
"failą",
"sami failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI failo formatas – subtitrų ir metaduomenų mainų failas",
  "description": "Sužinokite apie SAMI formatą ir API, kurios gali kurti ir atidaryti SAMI failus.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-lt",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## Kas yra SAMI failas?

Failas su plėtiniu .sami paprastai reiškia subtitrų ir metaduomenų mainų (SAMI) failą. SAMI yra subtitrų formatas, naudojamas vaizdo įrašuose rodyti subtitrus. Iš pradžių ją sukūrė Microsoft savo Windows Media Player.

SAMI failuose yra laiko informacija ir subtitrų tekstinis turinys, todėl juos galima sinchronizuoti su vaizdo įrašo atkūrimu. Formatas palaiko pagrindines formatavimo parinktis, tokias kaip šrifto stilius, spalva ir subtitrų padėtis ekrane.

SAMI failai paprastai yra paprasto teksto failai, kuriuos galima atidaryti ir redaguoti naudojant teksto rengyklę. SAMI failo turinys paprastai apima antraštės skyrių, kuriame pateikiama informacija apie failą, po kurio pateikiami atskiri subtitrų įrašai su atitinkamu laiku ir tekstu.

Štai pavyzdys, kaip gali atrodyti SAMI failas:

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

SAMI failai dažniausiai naudojami kartu su vaizdo grotuvais arba medijos leistuvais, kurie palaiko subtitrų rodymą, pvz., Windows Media Player arba VLC Media Player. Grotuvas nuskaito SAMI failą ir sinchronizuoja subtitrus su vaizdo įrašo turiniu, todėl žiūrovai gali skaityti antraštes žiūrėdami vaizdo įrašą.

## Palaikomos HTML žymos

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` Šakninis elementas, apimantis visą SAMI failą.
- ``<HEAD> :`` Yra SAMI failo antraštės informacija.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` Apibrėžia uždarojo teksto šrifto ypatybes. Šrifto išvaizdai keisti galima naudoti tokius atributus kaip spalva, veidas, dydis ir stilius.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` Pateikiamas tekstas atvaizduojamas pusjuodžiu šriftu.</b>
- `` <I>:`` Pateikiamas tekstas pateikiamas kursyvu.</i>
- `` <U>:`` Pateikiamas tekstas pabrauktas.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

Tai yra keletas pagrindinių žymų, kurias palaiko SAMI failai. Svarbu pažymėti, kad SAMI nepalaiko visų HTML žymų ir atributų. Palaikomos žymos pirmiausia yra skirtos subtitrų stiliui ir išdėstymui, o ne plačiam dokumentų struktūrizavimui ar interaktyvumui.

## Nuorodos
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


