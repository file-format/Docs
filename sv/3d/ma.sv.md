{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma fil", "ma filformat", "filformat", "3d", "ma fil nedladdning", ".ma fil", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om MA-filformat och API:er som kan öppna och skapa MA-filer.",
  "title" :"MA filformat",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Vad är en MA fil?

En fil med filtillägget .ma är en 3D-projektfil skapad med Autodesk Maya-applikationen. Den innehåller en stor lista med textkommandon för att ange information om filen. En **.ma-fil** kan öppnas och redigeras i vilken textredigerare som helst för att åtgärda eventuella problem med kommandona om en fil skulle bli korrupt. Dessa filer innehåller information för att definiera 3D-sceninformation som geometri, ljussättning, animering och rendering.

## MA filformat

MA-filer sparas på skiva i ASCII-textformat till skillnad från MB-filer som sparas i binärt filformat på skiva. En detaljerad referens för MA-filformat finns i [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) och kan hänvisas till till för utvecklarens referens.

### MA-filhuvud

MA-filhuvudet börjar med en sektion med kommentarer som ger information om hur filen skapades och datumet för ändringen. Maya-filläsare ignorerar detta block eftersom det bara används i informationssyfte. En rubrik måste dock börja med de första sex tecknen som "//Maya".

ASCII-filhuvudet ser ut som följer.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Filreferenser

Filreferensavsnittet i en .ma-fil innehåller information om alla andra Maya-filer som det refereras till i den här filen. Varje refererad fil kan läsas med ett enda filkommando som finns i samma fil. Syntaxen för filkommandot när det används för referenser är:

```
file -r -rpr prefixString fileName;
```
eller

```
file -r -ns nameSpace fileName
```
Här är ett exempel på en sträng.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Det här exemplet visar att solobjektet som finns i filen `solar` skulle vara tillgängligt i den här filen med namnet "solar_sun".

### Krav

Kravsektionen i en .ma-fil består av en serie obligatoriska kommandon och berättar May-information som version och plugin-information som krävs för att läsa filerna. Ett exempel på kravavsnittet är följande.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Nästa avsnitt specificerar kraven. Detta består av en serie kräver kommandon. Den här delen av filen berättar för Maya vilken programvara som behövs för att ladda filen ordentligt. Närmare bestämt vilken version av Maya och vilka plugins.

## MA fil nedladdning
Det är lite svårt att hitta och ladda ner MA-filen för en 3d-modell. Därför kan du ladda ner ett exempel på MA-fil här:

- [Sample.ma](../sample.ma)


## Referenser

* [Organisation of Maya ASCII Files - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

