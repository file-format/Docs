{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extensie", "bestand", "formaat", "Stripboeken", "Bestandsindeling stripboeken", "eBook"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over CBC-bestandsindeling en API's die CBC-bestanden kunnen maken en openen.",
  "title" :"CBC - Comic Book Collection-bestandsformaat",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Wat is een CBC-bestand?

Een bestand met de extensie .cbc is een gecomprimeerde verzameling stripboekbestanden voor eBooks en bevat [CBZ](/nl/ebook/cbz/) en [CBR](/nl/ebook/cbr/) bestanden. Het wordt gebruikt door [Calibre](https://calibre-ebook.com/), een eBook-conversietoepassing, een platformonafhankelijke open-source e-bookmanager waarmee u uw e-boeken kunt beheren en deze naar verschillende formaten kunt converteren . Een CBC-bestand bevat een .txt-bestand, comics.txt, met een lijst van andere bestanden die deel uitmaken van het archief. Er zijn online verschillende applicaties beschikbaar die CBC-bestanden kunnen converteren naar [AZW3](/nl/ebook/azw3/), [EPUB](/nl/ebook/epub/), [FB2](/nl/ebook/fb2/), [MOBI](/nl/ebook/ mobi/), [TXT](/nl/tekstverwerking/txt/), [PDF](/nl/pdf/) en andere populaire bestandsindelingen.

## CBC-bestandsindeling

CBC-bestanden zijn gecomprimeerde archieven die CBZ, CBR en een tekstbestand bevatten voor het weergeven van de inhoud. Het tekstbestand, comics.txt is UTF8-gecodeerd en bevat een lijst van de CBC-bestanden die lezers moeten gebruiken voor het organiseren van hun collecties. Een CBC-bestand heeft meestal verschillende attributen die de organisatie van deze collectie mogelijk maken, zoals Comic, Category, Publisher, Series, Edition en Artist.

De inhoud van een voorbeeld-CBC-bestand wordt als volgt weergegeven:

* comics.txt - Tekstbestand dat een lijst met CBR- en CBZ-bestanden bevat
* 1.cbz
* 2.cbz
* 3.cbz
* CBZ-bestand(en)

waar het comic.txt-bestand de inhoud als volgt weergeeft:

* 1.cbz: eerste hoofdstuk
* 2.cbz: tweede hoofdstuk
* 3.cbz: derde hoofdstuk

Lezers verwerken het comic.txt-bestand en genereren de inhoudsopgave op basis van de verstrekte gegevens.

## Referenties

* [Kaliber](https://calibre-ebook.com/)

