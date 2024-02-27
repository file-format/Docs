{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Filformat",
"Åben",
"Læs",
"skab",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Learn about DWF file format and APIs that can create and open DWF files.",
  "title": "DWF File Format",
  "linktitle": "DWF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dwf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DWF fil?

Design Web Format (DWF) repræsenterer 2D/3D-tegning i komprimeret format til visning, gennemgang eller udskrivning af designfiler. Den indeholder grafik og tekst som en del af designdata og reducerer størrelsen af filen på grund af dets komprimerede format. Den reducerede filstørrelse gør distribution og kommunikation af omfattende designdata effektiv. DWF kræver ikke, at modtageren kender til brugen af CAD-software, der skabte den originale tegning. Indholdet af DWF-filformatet kan være enkelt og kun omfatte et enkelt ark eller komplekst nok til at have skrifttyper, farver og billeder.

## Kort historie ##

Autodesk introducerede DWF-filformatet i 1995 som en del af Netscape Navigation plug-in, WHIP. Formatet udviklede sig fra kun 2D-format til at inkludere 3D-indhold med tiden. Mange af tredjepartsapplikationer gør også brug af dette format.

## DWF-filformat ##

DWF er et åbent, sikkert format designet specifikt til deling af omfattende tekniske designdata. Det er uafhængigt af den originale applikationssoftware, hardware og operativsystem, der bruges til at skabe disse designdata. Dette gør det muligt for teammedlemmer, der ikke bruger CAD-applikationer, at deltage i de digitale processer ved at se bygnings-, GIS- eller produktdesign. Et DWF-filarkiv består af flere XML- og binære filer, der er pakket sammen i et komprimeret arkiv, der er oprettet med [ZIP](/compression/zip/)-komprimering. Du kan omdøbe en DWF-filtypenavn til ZIP og se indholdet af filen. DWF-pakken kan indeholde mange slags designdata, såsom 2D-grafik, 3D-grafik, pakke- og sektionsmetadata og andre ressourcefiler.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Ressourcefiler** – medie- eller andre indholdsfiler, der refereres fra pakkens/sektionens metadata og normalt er præsentationer af designdata i forskellige formater (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/) osv.)

### Filformatdetaljer ###

DWF-filer er organiseret i tre hovedsektioner som vist nedenfor.

* Filidentifikationsoverskrift

* Fildatablok

* Trailer til filopsigelse


#### Filidentifikatoroverskrift ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Tegn|(|D|W|F|(mellemrum)|V|0|0|.|3|0|)

Her er en oversigt over denne tabel:

* De første seks bytes i overskriften repræsenterer altid ASCII-tegn "(DWF V"

* De følgende 5 bytes indeholder information om versionsnummeret, f.eks. "00.30" med formatets større og mindre versionsværdi


Programmer, der opretter en DWF-fil, bør angive det lavest mulige versionsnummer, som en læseapplikation skal understøtte for at kunne bruge dataene korrekt.

#### Fildatablok ####

Fildatablokken starter ved den 13. byte af en DWF-fil og er en række opkode- og operandpar, som i følgende tabel.

|Felt 1|Felt 2|Felt 3|Felt 4|Felt 5|Felt 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

En DWF-fil kan indeholde opcode-operand-par som læsbar ASCII såvel som binær kode eller en blanding af begge disse. Alle DWF-operationer har en læsbar ASCII-opkode/operandform, og de fleste operationer har også en kodet binær opkode/operandform. Opkoder er i enkeltbyte, hvilket giver mulighed for over 200 operationer. Udvidet ASCII og udvidet binær er undtagelsestilfælde. Værdierne for Opcodes kan variere fra 0-255 med nogle undtagelser. Bortset fra de to specielle typer opkoder udvidet ASCII og udvidet binær, skal en fillæser vide, hvordan man beregner operandlængden.

##### Forbudte opkoder #####

ASCII-repræsentationerne for følgende kan ikke bruges som opkoder:

Følgende ASCII-repræsentationer kan ikke bruges som opkoder:

* Mellemrum (0x20)

* Fane (0x09)

* Bindestreg (0x2D)

* ASCII-cifre 0-9 (0x30 - 0x39)

* Transportretur (0x0D)

* Line feed (0x0A)

* Enkelt anførselstegn (0x27)

* Dobbelt anførselstegn (0x22)

* Periode (0x2E)

* Parentese (0x28 og 0x29)

* Krøllede parenteser (0x7B og 0x7D)

* Firkantede parenteser (0x5B og 0x5D)

* Baglæns skråstreg (0x5C)


#### File Termination Trailer ####

Filtermineringstraileren til DWF er simpelthen en speciel opkode, der angiver slutningen af filen. Nogle applikationer kan gemme ikke-DWF-data efter opsigelseskoden. Traileren er som vist nedenfor:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Karakter|(|E|n|d|0|f|D|W|F|)

## Referencer ##

* [DWF - af Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)

* [WHIP-dataformat](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs /opc/adventures-in-packaging-episode-1)


