{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "tillägg", "fil", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om Amazon APNX-filformat och API:er som kan skapa och öppna APNX-filer.",
  "title" :"APNX - Amazon Sidnummer Index",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Vad är APNX fil? ##

Amazon Page Number Index-filen som använder tillägget .apnx är en eBook-filtyp; används av Amazon Kindle. Dessa filer är faktiskt kända som pagineringsfiler som används av Kindle-enheter. Så APNX-filerna skapas vanligtvis för att markera sidorna i Kindle eBooks. Pagineringsfunktionen har startats på Amazon Kindle-enheter sedan dess 3.1 firmware. Den tittar i APNX-filen för sidindex och mappar den sedan med sidnumren i den ursprungliga tryckta boken. Dessa filer sparas i Kindle-enheter tillsammans med Amazon eBooks-filer. Du kan inte öppna eller redigera APNX-filerna.

## APNX filformatspecifikationer ##

### Layout

|byte| innehåll| kommentarer|
---|---|---|
|4 |00010001 | Formatidentifierare. Värde av 65537 little-endian.|
|4 |början av nästa | Förskjutningen efter slutplatsen för den första rubriken. Startar en ny sekvens av rubrikinfo|
|4 |längd| Längd på första rubrik|
|N |första rubriken | Sträng som innehåller innehållshuvud. Det börjar nästa sekvens|
|2 |okänt | Alltid 1|
|2 |längd | Längd på andra rubrik|
|2 |antal sidor | Totalt antal byte efter andra rubrik som representerar sidor. Denna summa inkluderar byte som ignoreras av pageMap.|
|2 |okänt | Alltid 32|
|N |andra rubrik | Sträng som innehåller sidmappningshuvudet|
|4*N |stoppning | Den första siffran som anges i sidmappningshuvudet indikerar antalet 0 byte.|
|4*N |sidlista ||

### Innehållshuvud

Innehållsrubriken består av en sträng omsluten av {} som innehåller nyckel, värdepar:

|innehåll| kommentarer|
---|---|
|contentGuid| Guid.|
|asin | Amazon-identifierare för Kindle-versionen av boken.|
|cdeType | MOBI cdeType. Bör alltid vara EBOK för e-böcker.|
|fileRevisionId | Revision av denna fil.|

#### Exempel
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Sidmappningshuvud
Sidmappningshuvudet består av en sträng omsluten av {} som innehåller nyckel, värdepar.

|innehåll | kommentarer|
---|---|
|asin | ISBN 10 för pappersboken som sidorna motsvarar|
|pageMap| Tre värde tupel. Ser ut som: "(N,N,N)\
1) Antal byte efter rubrik som startar sidnumreringssekvensen\
2) okänd\
3) okänd\|
#### Exempel
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Sidlista

Sidlistan är en sekvens av förskjutningar i rå HTML. Varje
värde är början på en ny sida. Varje post är en 4 byte stor endian
int.



## Referenser

* [Amazon APNX-filformat](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - av MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

