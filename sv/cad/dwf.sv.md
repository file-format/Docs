{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Filformat", "Öppna", "Läs", "Skapa", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DWF-filformat och API:er som kan skapa och öppna DWF-filer.",
  "title" :"DWF-filformat",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DWF fil?

Design Web Format (DWF) representerar 2D/3D-ritning i komprimerat format för att visa, granska eller skriva ut designfiler. Den innehåller grafik och text som en del av designdata och minskar storleken på filen på grund av dess komprimerade format. Den minskade filstorleken gör distributionen och kommunikationen av rik designdata effektiv. DWF kräver inte att mottagaren känner till användningen av CAD-programvaran som skapade den ursprungliga ritningen. Innehållet i DWF-filformat kan vara enkelt och innehålla bara ett enda ark eller tillräckligt komplext för att ha typsnitt, färg och bilder.

## Kortfattad bakgrund ##

Autodesk introducerade DWF-filformatet 1995 som en del av Netscape Navigation plug-in, WHIP. Formatet utvecklades från endast 2D-format till att omfatta 3D-innehåll med tiden. Många av tredjepartsapplikationer använder också detta format.

## DWF-filformat ##

DWF är ett öppet, säkert format designat speciellt för att dela rik teknisk designdata. Det är oberoende av den ursprungliga programvaran, hårdvaran och operativsystemet som används för att skapa designdata. Detta gör det möjligt för teammedlemmar som inte använder CAD-applikationer att delta i de digitala processerna genom att se byggnads-, GIS- eller produktdesigner. Ett DWF-filarkiv består av flera XML- och binära filer som är paketerade tillsammans i ett komprimerat arkiv skapat med [ZIP](/sv/compression/zip/)-komprimering. Du kan byta namn på ett DWF-filtillägg till ZIP och visa innehållet i filen. DWF-paketet kan innehålla många typer av designdata som 2D-grafik, 3D-grafik, paket- och sektionsmetadata och andra resursfiler.

**DWF-metadatafiler** – XML-filer som innehåller information som hänför sig till metadata och struktur (författare, titel, skapelsetid, sektionsberoenden, sektionsordning, resursfilbeskrivningar, roller, mimetyper, etc.) och som hänför sig till sektionen (sida information, designmetadata, etc.). Den strukturella metadatan används för att skapa logiska objekt (samlingar av filer för att representera en del eller sida, etc.).

**Resursfiler** – media eller andra innehållsfiler som refereras från paketets/sektionens metadata och är vanligtvis presentationer av designdata i olika format (ZGL, W2D, [JPG](/sv/image/jpeg/), [PNG](/sv/image/png/), AVI, XML, [TXT](/sv/ordbehandling/txt/), [DOC](/sv/ordbehandling/doc/), etc.)

### Filformatdetaljer ###

DWF-filer är organiserade i tre huvudsektioner som visas nedan.

* Filidentifieringshuvud
* Fildatablock
* Filavslutningstrailer

#### Filidentifieringshuvud ####

Filidentifierarens rubrik tillåter identifiering av DWF-filer av applikationer. Den identifierar också vilken version av DWF-specifikationerna som användes för att koda filen. Det är en 12 byte header som är arrangerad enligt följande:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Tecken|(|D|W|F|(mellanslag)|V|0|0|.|3|0|)

Här är en sammanfattning av tabellen:

* De första sex byten i rubriken representerar alltid ASCII-tecken "(DWF V"
* Följande 5 byte innehåller information om versionsnumret, t.ex. "00.30" med formatets större och mindre versionsvärde

Applikationer som skapar en DWF-fil bör ange lägsta möjliga versionsnummer som en läsarapplikation behöver stödja för att kunna använda data på rätt sätt.

#### Fildatablock ####

Fildatablocket börjar vid den 13:e byten i en DWF-fil och är en serie av opcode- och operandpar, som i följande tabell.

|Fält 1|Fält 2|Fält 3|Fält 4|Fält 5|Fält 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

En DWF-fil kan innehålla opcode-operand-par som läsbar ASCII såväl som binär kod eller en blandning av båda dessa. Alla DWF-operationer har en läsbar ASCII-opkod/operandform, och de flesta operationer har även en kodad binär opkod/operandform. Opcodes är i en byte som tillåter över 200 operationer. Utökad ASCII och utökad binär är undantagsfall. Värdena för Opcodes kan variera från 0-255 med vissa undantag. Förutom de två speciella typerna av op-koder utökad ASCII och utökad binär, måste en filläsare veta hur man beräknar operandens längd.

##### Förbjudna opkoder #####

ASCII-representationerna för följande kan inte användas som opkoder:

Följande ASCII-representationer kan inte användas som opkoder:

* Mellanslag (0x20)
* Tab (0x09)
* Bindestreck (0x2D)
* ASCII-siffror 0-9 (0x30 - 0x39)
* Transportretur (0x0D)
* Radmatning (0x0A)
* Enstaka citattecken (0x27)
* Dubbla citattecken (0x22)
* Period (0x2E)
* Parentes (0x28 och 0x29)
* Lockiga parenteser (0x7B och 0x7D)
* Hakparenteser (0x5B och 0x5D)
* snedstreck bakåt (0x5C)

#### Filavslutningstrailer ####

Filavslutningstrailern för DWF är helt enkelt en speciell op-kod som indikerar slutet på filen. Vissa applikationer kan lagra icke-DWF-data efter avslutningskoden. Trailern är som visas nedan:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Tecken|(|E|n|d|0|f|D|W|F|)

## Referenser ##

* [DWF - av Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP-dataformat](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

