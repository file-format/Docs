{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG-bestandsindeling - Python-distributiebestand",
  "description":"Meer informatie over EGG-bestandsindeling en API's die EGG-bestanden kunnen maken en openen.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Wat is een EGG-bestand?

Een EGG-bestand, ook wel Python-eieren genoemd, is een ouder distributieformaat voor Python-distributies. Het is een [ZIP](/nl/compression/zip/) gecomprimeerd archief met de extensie .egg en bevat de bronbestanden van de Python-toepassing samen met meta-informatie over de distributie. EGG-bestanden zijn een alternatief voor een Windows Executable [EXE](/nl/executable/exe/)-bestand, maar zijn platformonafhankelijk. Dit oudere formaat voor Python-distributies is begin 2010 vervangen door het nieuwere Wheel (WHL)-bestandsformaat.

## EGG-bestandsindeling

EGG-bestanden worden opgeslagen als gecomprimeerde ZIP-archieven. Dit betekent dat als u de .egg-extensie vervangt door .zip, u deze kunt openen met standaard decompressieprogramma's zoals Corel WinZIP, Microsoft Explorer of RARLAB WinRAR.

EGG-bestanden kunnen worden gemaakt met behulp van het **distutils**-pakket dat beschikbaar is door Python. Een andere tool die EGG-bestanden kan maken en openen is **SetupTools**. EGG-bestanden kunnen als pakket worden geïnstalleerd met **easy_install**.

`OPMERKING - EGG-bestandsformaat is verouderd ten gunste van het nieuwe wiel WHL-bestandsformaat.`

## Referentie ##

* [Python EGG's](https://python101.pythonlibrary.org/chapter38_eggs.html)

