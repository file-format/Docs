{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Gecomprimeerd", "Bestand", "Extensie", "Bestandsindeling", "Lempel-Ziv-Oberhume"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO-bestandsindeling",
  "description":"Meer informatie over LZO-bestandsindeling en API's die LZO-bestanden kunnen maken en openen.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Wat is een LZO-bestand? ##

Een bestand met de extensie .lzo wordt gecombineerd met functies voor bestandsarchivering die de grootte van alle bestanden in het gecomprimeerde bestand kunnen verkleinen. Alle gecomprimeerde bestanden kunnen een of meer bestanden bevatten of zelfs groepen mappen met verschillende bestanden van verschillende soorten en afmetingen. De grootte van een gecomprimeerd bestand is kleiner in vergelijking met de gezamenlijke grootte van alle bestanden en mappen die zijn opgeslagen in een gecomprimeerd LZO-bestand. Alle LZO-gecomprimeerde bestanden worden opgeslagen in het LZO-formaat en worden expliciet uitgevoerd met compressiefuncties die worden gebruikt door de LZOP-bestandscompressie- en decompressiesoftware. Alle compressiespecificaties zijn gecombineerd in dit bestandscompressie- en decompressieprogramma dat afkomstig is uit de Lempel-Ziv-Oberhume bestandscompressiebibliotheek. Hogere decompressiesnelheid en ontwikkelde compressieverhoudingen worden ook gecombineerd in deze LZO-bestanden.

## LZO-specificatie ##

Markus Franz Xaver Johannes Oberhumer ontwikkelde het originele "lzop"-algoritme, gebaseerd op eerdere algoritmen van Abraham Lempel en Jacob Ziv, in 1996. Deze bibliotheek implementeert een verscheidenheid aan algoritmen met de volgende kenmerken:

* Snellere compressie dan DEFLATE
* Snelle decompressie
* Extra buffers die nodig zijn tijdens compressie (van 8 KB of 64 KB, afhankelijk van het compressieniveau)
* De bron- en bestemmingsbuffers zijn al het geheugen dat nodig is voor decompressie
* Biedt controle over zowel de compressieverhouding als de compressiesnelheid

Als blokcompressie-algoritme voert LZO zowel overlappende compressie als in-place decompressie uit. Om overlappende compressie te bereiken, moet de blokgrootte van zowel compressie als decompressie overeenkomen. Het LZO-compressie-algoritme splitst de invoergegevens op in overeenkomsten (een glijdend woordenboek) en literalen die niet overeenkomen, wat goede resultaten oplevert met zeer redundante gegevens en acceptabele resultaten met niet-samendrukbare gegevens, waarbij alleen de niet-samendrukbare gegevens toenemen met 1/64 van het origineel maat.

## Problemen bij het openen van een LZO-bestand ##

Hieronder volgen enkele problemen die een slechte werking van het LZO-bestandsformaat kunnen veroorzaken:
  


* Het bestand is mogelijk beschadigd. Om dit probleem op te lossen, downloadt u het bestand opnieuw of vraagt u de afzender om het bestand opnieuw te verzenden
* De tweede reden is dat het geïnfecteerde bestand in dit geval het bestand goed scant
* Onjuiste links naar het LZO-bestand
* Verwijdering van de beschrijving van de LZO
* Niet genoeg hardwarebronnen
* Verouderde stuurprogramma's van de apparatuur
  


## Referenties ##

* [LZO - Door Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

