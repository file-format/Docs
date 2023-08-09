{
  "date" : "2019-12-09",
  "keywords" :[ "3mf fil", "3mf filformat", "vad är en 3mf fil", "fil", "3mf exempel", "3mf filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Läs mer om 3MF-filformat och API:er som kan öppna och skapa 3MF-filer.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Vad är 3MF fil?

3MF, 3D Manufacturing Format, används av applikationer för att återge 3D-objektmodeller till en mängd andra applikationer, plattformar, tjänster och skrivare. Den byggdes för att undvika begränsningar och problem i andra 3D-filformat, som [STL](/sv/cad/stl/), för att arbeta med de senaste versionerna av 3D-skrivare. 3MF är ett relativt nytt filformat som har utvecklats och publicerats av 3MF-konsortiet. Den är tillräckligt rik för att fullständigt beskriva en modell, behåller intern information, färg och andra egenskaper som gör den utbyggbar för att stödja nya innovationer inom 3D-utskrift. Formatet är utbyggbart, kan användas brett och fritt från problem som drabbar andra allmänt använda filformat.

## Kort historik över 3MF-filformat

De befintliga begränsningarna i tillgängliga modellbeskrivande filformat, som STL och andra, leder till att de ledande varumärkena går samman och formulerar ett mer utbyggbart filformat för 3D-utskrift. Ett viktigt övervägande var hur applikationer skulle skicka modelldata till 3D-skrivare. 3MF-konsortiet kom därför till för att stödja ett nytt 3D-filformat som heter 3MF med målet att göra det tillräckligt utbyggbart för att tillgodose behoven av 3D-utskrift. Flera företag ingick i detta konsortium, inklusive Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP och andra. Microsoft donerade sitt 3D-filformat som pågår som utgångspunkt för 3MF-konsortiets gemensamma vidareutveckling av specifikationen.

## 3MF filformat - Mer information

3MF är ett XML-baserat dataformat – mänskligt läsbar komprimerad XML – som innehåller definitioner för data relaterade till 3D-tillverkning, inklusive tredjeparts utökbarhet för anpassad data. 3MF-filformatet utformades med tanke på de begränsningar och problem som andra 3D-filformat möter. Detta ledde till formuleringen av 3MF filformat som är:

* **Fullständig:** Innehåller all nödvändig modell-, material- och egendomsinformation i ett enda arkiv
* **Läsbar för människor:** Använder vanliga strukturer som OPC, [ZIP](/sv/compression/zip/) och XML för att underlätta utvecklingen
* **Enkelt:** En kort, tydlig specifikation som gör utvecklingen enkel och valideringen snabb
* **Utökningsbar:** Att utnyttja XML-namnrymder möjliggör både offentliga och privata tillägg samtidigt som kompatibiliteten bibehålls
* **Entydigt:** Tydliga språk- och överensstämmelsetester säkerställer att en fil alltid är konsekvent från digital till fysisk
* **Gratis:** Tillgång till och implementering av 3MF-specifikationen är och kommer alltid att vara fri från royalties, patent och licensiering

Specifikationerna för 3MF-filformat finns på [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) för offentlig åtkomst och kontinuerliga uppdateringar. Den nuvarande publicerade versionen är 1.2.3 som beskriver uppsättningen konventioner för användning av XML och andra allmänt tillgängliga tekniker för att beskriva innehållet och utseendet på en eller flera 3D-modeller. Utvecklare som vill bygga system för bearbetning av 3MF-filformat kan hänvisa till dessa specifikationer för implementeringsändamål.

## 3MF filformatspecifikationer

3MF-filformatet använder Open Packaging-specifikationerna i form av ZIP-arkiv för sin fysiska modell. Det inkluderar en väldefinierad uppsättning delar och relationer som fyller särskilda syften i dokumentet. Detta gör också att formatet följer paketfunktionen inklusive digitala signaturer och miniatyrer.

### 3MF-dokumentet - en översikt

Ett typiskt 3MF-dokument ser ut som följer:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Nyttolasten inkluderar hela uppsättningen delar som krävs för att bearbeta 3D-modelldelen. Allt innehåll som ska användas för att tillverka ett objekt som beskrivs i 3D-nyttolasten MÅSTE finnas i 3MF-dokumentet. Beskrivningen av varje dokumentdel tillsammans med dess status efter behov eller alternativ visas i följande tabell.


|**Namn**|**Beskrivning**|**Källa för relation**|**Obligatoriskt/valfritt**
--- | --- | --- | ---
|3D-modell|Innehåller beskrivningen av ett eller flera 3D-objekt för tillverkning.|Paket|KRÄVS
|Kärnegenskaper|OPC-delen som innehåller olika dokumentegenskaper.|Paket|VALFRITT
|Digital Signature Origin|OPC-delen som är roten till digitala signaturer i paketet.|Paket|VALFRITT
|Digital signatur|OPC-delar som var och en innehåller en digital signatur.|Digital signaturursprung|VALFRITT
|Digitalt signaturcertifikat|OPC-delar som innehåller ett digitalt signaturcertifikat.|Digital signatur|VALFRITT
|PrintTicket|Tillhandahåller inställningar som ska användas vid utmatning av 3D-objekt i 3D-modelldelen.|3D-modell|VALFRITT
|Thumbnail|Innehåller en liten JPEG- eller PNG-bild som representerar 3D-objekten i paketet eller paketet som helhet.|Paket|VALFRITT
|3D Texture|Innehåller en textur som används för att applicera färg på ett 3D-objekt i 3D-modelldelen (tillgänglig för tillägg)|3D-modell|VALFRITT
|Anpassade delar|OPC-delar som är associerade med metadata|Paket|VALFRITT

[Delar och relationer](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D-modeller](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) och [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) avsnitt i specifikationerna dokumentet ger detaljerad information om 3MF-dokumentet.

## Referenser ##

* [3MF filformatspecifikationer](https://github.com/3MFConsortium/spec_core)
* [3MF - av Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

