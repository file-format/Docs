{
  "date" : "2019-10-11",
  "keywords" :[ "apng-fil", "apng-filformat", "vad är en apng-fil", "fil", "apng-exempel", "apng-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG-filformat - Animerad bärbar nätverksgrafisk fil",
  "description":"Läs mer om APNG-filformat och API:er som kan skapa och öppna APNG-filer.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en APNG fil?

En fil med tillägget .apng (Animated Portable Network Graphics) är ett rastergrafikformat och är ett inofficiellt tillägg till Portable Network Graphic ([PNG](/sv/image/png/) ). Den består av flera bildrutor (var och en av PNG-bilder) som representerar en animationssekvens. Detta ger liknande visualisering som en [GIF](/sv/image/gif/)-fil. APNG-filer stöder 24-bitars bilder och 8-bitars transparens. APNG är bakåtkompatibel med icke-animerade GIF-filer. APNG-filer använder samma .png-tillägg och kan öppnas av applikationer som Mozilla Firefox, Chrome med APNG-stöd, iMessage-appar för iOS 10.

## Kortfattad bakgrund

* APNG-specifikationer skapades 2004 för att ge stöd för animerade PNG-bilder
* APNG-avkodare utvecklades med mycket mindre storlek och med baksidan av PNG-avkodaren
* Efter kontinuerliga överväganden formulerades en ny MIME-typ image/apng samtidigt som tillägget hölls samma som .png istället för .apng
* APNG avvisades officiellt av PNG-gruppen den 20 april 2007 på grund av dess enhetlighet med PNG-bilder samtidigt som den hade olika specifikationer

## APNG filformat

APNG-filer lagras som binära filer på skiva och använder de utökade specifikationerna för PNG för animerade bilder. Den första bildrutan i en APNG-fil är en normal PNG-ström som kan läsas av PNG-avkodare för visning. APNG-filformat följer PNG-specifikationerna och data lagras i segment som kallas chunks. Men APNG introducerade följande nya bitar:

`Animation Control Chunk (acTL)` - Indikerar att den här filen är en animerad PNG-fil snarare än en vanlig PNG-fil. Den fungerar som en markör och kommer före IDAT-biten. Den innehåller också antalet bildrutor och information om tider för att loopa animationerna

`Frame Control Chunk` - Uppstår i början av varje och metadatainformation såsom dimensioner, position, transparensapplikation och ersättningsinformation av föregående eller nästa bildruta när den är över.

`Frame Data Chunk` - Lagrar ramens innehåll och börjar med ett sekvensnummer. Detta sekvensnummer har samma struktur som standardbildens IDAT-bit.

{{< figure src="../APNG.png" alt="Animerad PNG - APNG filformat" >}}

APNG är bakåtkompatibel med PNG eftersom lateralens specifikationer utformades på ett sådant sätt att en applikation som läser en PNG-fil ska helt enkelt ignorera de bitar som den inte förstår. Specifikationer för bitdjup, färgtyp, komprimering, filter, sammanflätningsmetoder och palettinformation används på samma sätt som för standard PNG-format.

## APNG vs GIF

Med GIF redan på plats och används under en lång tidsperiod, kanske du undrar hur APNG skiljer sig från GIF. Följande är en uppsättning jämförelser mellan APNG och GIF som ger en kort uppfattning om båda filformaten.

||APNG|GIF|
---|---|---|
|Publicerad|2004|1987|
|Färgdjup|24 bitar|8 bitar|
|Bildhastighet|Obegränsat|10 bilder per sekund|
|Transparens|Fullständig och delvis|Fullständig|
|Kompression|Mycket bra|Bra|

## Referenser

* [APNG-filformat](https://en.wikipedia.org/wiki/APNG)
* [Officiella specifikationer för PNG-format](https://www.w3.org/TR/PNG/)

