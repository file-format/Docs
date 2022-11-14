{
  "date" : "2021-08-17",
  "keywords" :[ "udf-bestand", "udf-bestandsindeling", "wat is een udf-bestand", "bestand", "udf-voorbeeld", "udf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over de UDF-bestandsindeling en API's die UDF-bestanden kunnen maken en openen.",
  "title" :"UDF - Universal Disk Format File",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Wat is een UDF-bestand?
Het bestand met de extensie .udf is een schijfbeeldformaat dat doorgaans wordt gebruikt voor het opslaan van bestanden op optische media; kan worden gebruikt voor het branden van dvd's, cd's en andere optische media; slaat een verzameling bestanden op met behulp van de directorystructuur die is gespecificeerd in de UDF-standaard; staat toe dat bestanden op de doelschijf worden verwijderd en gewijzigd, zelfs nadat ze zijn geschreven. De Optical Storage Technology Association heeft het UDF-bestandssysteem als standaard ingesteld om een gemeenschappelijk bestandssysteem te vormen voor alle optische media, zoals voor herschrijfbare optische media en alleen-lezen media.

## UDF-bestandsindeling
Het UDF-bestandsformaat is een open leveranciersonafhankelijk bestandssysteem voor computergegevensopslag voor een breed scala aan media. Het is vaak gebruikt voor dvd's en nieuwere optische schijfformaten. Gewoonlijk beheerst de software een UDF-bestandssysteem in een batchproces en schrijft het in één keer naar optische media. Wanneer het echter pakketten naar herschrijfbare media schrijft, staat de UDF toe dat bestanden op schijf worden gemaakt, verwijderd en gewijzigd, vergelijkbaar met een algemeen bestandssysteem op verwisselbare media zoals flashdrives of diskettes.
### UDF-specificaties
De UDF-standaard definieert de volgende drie bestandssysteemvarianten:

- **Plain Build**: dit is het originele formaat dat in alle UDF-revisies wordt ondersteund. Het werd geïntroduceerd in de eerste versie van de standaard. Dit formaat kan worden gebruikt op elk type schijf dat willekeurige lees- of schrijftoegang mogelijk maakt, zoals dvd+rw, harde schijven en dvd-ram-media.
- **BTW-opbouw**: wordt specifiek gebruikt voor het schrijven naar eenmaal beschrijfbare media. De VAT is een extra structuur op de schijf die het schrijven van pakketten mogelijk maakt; dat wil zeggen, het opnieuw toewijzen van fysieke blokken wanneer bestanden of andere gegevens op de schijf worden gewijzigd of verwijderd. Voor eenmaal beschrijfbare media is de hele schijf gevirtualiseerd, waardoor het eenmaal beschrijfbare karakter transparant is voor de gebruiker; de schijf kan op dezelfde manier worden behandeld als een herschrijfbare schijf.
- **Spared (RW) build**: wordt specifiek gebruikt voor het schrijven naar herschrijfbare media. Het voegt een extra Sparing Table toe om de fouten te beheren die uiteindelijk zullen optreden op delen van de schijf die meerdere keren zijn herschreven. Deze tabel slaat versleten sectoren op en wijst ze opnieuw toe aan werkende. Het defectbeheer van UDF is niet van toepassing op systemen die al een andere vorm van defectbeheer implementeren, zoals Mount Rainier (MRW) voor optische schijven of een schijfcontroller voor een harde schijf.
 




## Referenties


* [Windows Imaging Format - door Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


