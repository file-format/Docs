{
  "date" : "2019-10-11",
  "keywords" :[ "apng-bestand", "apng-bestandsindeling", "wat is een apng-bestand", "bestand", "apng-voorbeeld", "apng-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG-bestandsindeling - geanimeerd grafisch draagbaar netwerkbestand",
  "description":"Meer informatie over de APNG-bestandsindeling en API's die APNG-bestanden kunnen maken en openen.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een APNG-bestand?

Een bestand met de extensie .apng (Animated Portable Network Graphics) is een grafische rasterindeling en is een niet-officiële extensie van de Portable Network Graphic ([PNG](/nl/image/png/) ). Het bestaat uit meerdere frames (elk PNG-afbeelding) die een animatiereeks vertegenwoordigt. Dit geeft een vergelijkbare visualisatie als een [GIF](/nl/image/gif/)-bestand. APNG-bestanden ondersteunen 24-bits afbeeldingen en 8-bits transparantie. APNG is achterwaarts compatibel met niet-geanimeerde GIF-bestanden. APNG-bestanden gebruiken dezelfde .png-extensie en kunnen worden geopend door toepassingen zoals Mozilla Firefox, Chrome met APNG-ondersteuning, iMessage-apps voor iOS 10.

## Korte geschiedenis

* APNG-specificaties zijn in 2004 gemaakt om ondersteuning te bieden voor geanimeerde PNG-afbeeldingen
* APNG-decoders zijn ontwikkeld met een veel kleiner formaat en met behulp van de achterkant van de PNG-decoder
* Na voortdurend wikken en wegen werd een nieuw MIME-type image/apng geformuleerd terwijl de extensie hetzelfde bleef als .png in plaats van .apng
* APNG werd op 20 april 2007 officieel afgewezen door de PNG-groep vanwege de uniformiteit met PNG-afbeeldingen en tegelijkertijd met verschillende specificaties

## APNG-bestandsindeling

APNG-bestanden worden opgeslagen als binaire bestanden op schijf en gebruiken de uitgebreide specificaties van PNG voor geanimeerde afbeeldingen. Het eerste frame van een APNG-bestand is een normale PNG-stream die kan worden gelezen door PNG-decoders voor weergave. Het APNG-bestandsformaat volgt de PNG-specificaties en de gegevens worden opgeslagen in segmenten die chunks worden genoemd. APNG heeft echter de volgende nieuwe chunks geïntroduceerd:

`Animation Control Chunk (acTL)` - Geeft aan dat dit bestand een geanimeerd PNG-bestand is in plaats van een normaal PNG-bestand. Het fungeert als een markering en komt voor de IDAT-chunk. Het bevat ook het aantal frames en informatie over tijden om de animaties te herhalen

`Frame Control Chunk` - Vindt plaats aan het begin van elk en metadata-informatie zoals afmetingen, positie, transparantietoepassing en vervangingsinformatie door het vorige of volgende frame zodra het voorbij is.

`Frame Data Chunk` - Slaat de inhoud van het frame op en begint met een volgnummer. Dit volgnummer heeft dezelfde structuur als de IDAT-chunk van de standaardafbeelding.

{{< figure src="../APNG.png" alt="Geanimeerde PNG - APNG-bestandsindeling" >}}

APNG is achterwaarts compatibel met PNG, aangezien de specificaties van de lateral zo zijn ontworpen dat een toepassing die een PNG-bestand leest, gewoon de stukjes negeert die het niet begrijpt. Specificaties met betrekking tot bitdiepte, kleurtype, compressie, filters, interlace-methoden en paletinformatie worden hetzelfde gebruikt als die van het standaard PNG-formaat.

## APNG versus GIF

Nu GIF al aanwezig is en gedurende een lange periode wordt gebruikt, vraagt u zich misschien af hoe APNG anders is dan GIF. Hieronder volgt een reeks vergelijkingen tussen APNG en GIF die een kort idee geeft van beide bestandsindelingen.

||APNG|GIF|
---|---|---|
|Gepubliceerd|2004|1987|
|Kleurdiepte|24 bit|8 bit|
|Frame Rate|Onbeperkt|10 frames per seconde|
|Transparantie|Volledig en gedeeltelijk|Volledig|
|Compressie|Zeer goed|Goed|

## Referenties

* [APNG-bestandsindeling](https://en.wikipedia.org/wiki/APNG)
* [Officiële PNG-formaatspecificaties](https://www.w3.org/TR/PNG/)

