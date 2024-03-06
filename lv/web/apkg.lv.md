{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"apkg failu",
"apkg faila formātā",
"apkg faila tips",
"failu",
"veids",
"Kas ir APKG fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG — Anki Flashcard Deck faila formāts",
  "description": "Uzziniet, kas ir APKG fails un API, kas var tos izveidot un atvērt.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-lvg"
}
},
  "lastmod": "2021-06-16"
}

## Kas ir APKG fails?

Fails ar paplašinājumu .apkg ir zibatmiņu komplekts, kas ģenerēts izmantošanai [Anki](https://ankiweb.net/about) lietojumprogrammā, kas ir uz zibatmiņas kartēm balstīta mācību programma. Tajā ir [HTML](/web/html/) teksts, kas jāielādē un jāparāda lietojumprogrammā Anki, un tajā var būt arī attēli un skaņas vizuālai un dzirdamai apmācībai. Anki ļauj lietotājiem izveidot savus Anki zibatmiņas karšu komplektus, kā arī importēt citu lietotāju zibatmiņas karšu komplektus.

## APKG faila formāts

Anki karšu komplekti tiek veidoti no veidnēm, kas ir rakstītas HTML valodā, kas ir slavena un izplatīta tīmekļa lapu izveides valoda. Klāja karšu veidošana tiek veikta, izmantojot CSS, kas ir valoda, ko izmanto tīmekļa lapu veidošanai. Stils ietver šādas izmaiņas:

 * font-family — kartē izmantojamā fonta nosaukums.
 * font-size — fonta lielums pikseļos.
 * text-align — nosaka, vai tekstam jābūt līdzinātam centrā, pa kreisi vai pa labi.
 * krāsa — definē teksta krāsu, kas var būt vienkārši krāsu nosaukumi, piemēram, zils, sarkans utt., vai HTML krāsu kodi.
 * background-color — definē kartes fona krāsu

Stila informācija tiek kopīgota starp visām kartēm, kas ietekmē visas kartītes, kad tiek veiktas izmaiņas. Šajā piemērā uz visām kartītēm, izņemot pirmo, tiks izmantots dzeltens fons.

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Attēlu izmēru maiņu Anki kartē var kontrolēt šādi.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript iegulšana Anki kartēs

Izmantojot karšu veidnes, Anki kartē ir iespējams iegult [Javascript](/web/js/). Tomēr Javascript uzlabotā līmeņa dēļ tā atbalsts netiek nodrošināts. Turklāt renderēšanas ierīces var atšķirīgi parādīt Javascript ieviešanas ietekmi kartē, kā rezultātā ir jāpārbauda ieviešana visās ierīcēs. Daži Javascript līdzekļi, piemēram, window.alert, kas apgrūtina jūsu rakstītā Javascript koda atkļūdošanu.

## Atsauces Nr.

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

