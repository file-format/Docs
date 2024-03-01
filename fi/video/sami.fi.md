{
  "date": "2023-05-16",
  "keywords": [
"saamen tiedosto",
"mikä on saamelainen tiedosto",
"esimerkki sami-tiedostosta",
"tiedosto",
"sami tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI-tiedostomuoto - tekstitys ja metatietojen vaihtotiedosto",
  "description": "Opi SAMI-muodosta ja API-liittymistä, jotka voivat luoda ja avata SAMI-tiedostoja.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-fi",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## Mikä on SAMI-tiedosto?

Tiedosto, jonka tunniste on .sami, viittaa yleensä SAMI-tiedostoon (Subtitles And Metadata Interchange). SAMI on tekstitysmuoto, jota käytetään tekstityksen näyttämiseen videoissa. Sen kehitti alun perin Microsoft Windows Media Playerilleen.

SAMI-tiedostot sisältävät tekstityksen ajoitustietoja ja tekstisisältöä, mikä mahdollistaa niiden synkronoinnin videon toiston kanssa. Muoto tukee perusmuotoiluvaihtoehtoja, kuten kirjasintyyliä, väriä ja tekstityksen sijaintia näytöllä.

SAMI-tiedostot ovat yleensä pelkkiä tekstitiedostoja, ja niitä voidaan avata ja muokata tekstieditorilla. SAMI-tiedoston sisältö sisältää tyypillisesti otsikkoosion, joka sisältää tietoja tiedostosta, ja sen jälkeen yksittäiset tekstitysmerkinnät niiden ajoituksen ja tekstin kanssa.

Tässä on esimerkki siitä, miltä SAMI-tiedosto voi näyttää:

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

SAMI-tiedostoja käytetään yleisesti tekstitysnäyttöä tukevien videosoittimien tai mediasoittimien, kuten Windows Media Playerin tai VLC Media Playerin, kanssa. Soitin lukee SAMI-tiedoston ja synkronoi tekstitykset videosisällön kanssa, jolloin katsojat voivat lukea kuvatekstejä katsoessaan videota.

## Tuetut HTML-tunnisteet

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` Juurielementti, joka kapseloi koko SAMI-tiedoston.
- ``<HEAD> :`` Sisältää SAMI-tiedoston otsikkotiedot.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` Määrittää kirjasimen ominaisuudet suljetulle tekstille. Attribuutteja, kuten Color, Face, Size ja Style, voidaan käyttää fontin ulkoasun muokkaamiseen.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` Muodostaa oheisen tekstin lihavoituna.</b>
- `` <I>:`` Muodostaa oheisen tekstin kursiivilla.</i>
- `` <U>:`` Tekee oheisen tekstin alleviivatuksi.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

Nämä ovat joitain SAMI-tiedostojen tukemista perustunnisteista. On tärkeää huomata, että SAMI ei tue kaikkia HTML-tageja ja -attribuutteja. Tuetut tunnisteet keskittyvät ensisijaisesti tekstitysten muotoiluun ja sijoittamiseen sen sijaan, että ne tarjoaisivat laajan asiakirjan jäsentelyn tai interaktiivisuuden.

## Viitteet
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


