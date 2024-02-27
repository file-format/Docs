{
  "date": "2019-10-11",
  "keywords": [
"ma",
"ma fil",
"ma filformat",
"filformat",
"3d",
"ma fil download",
".ma fil",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MA-filformat og API'er, der kan åbne og oprette MA-filer.",
  "title": "MA filformat",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-daa"
}
},
  "lastmod": "2021-06-04"
}

## Hvad er en MA fil?

En fil med filtypenavnet .ma er en 3D-projektfil oprettet med Autodesk Maya-applikationen. Den indeholder en stor liste over tekstkommandoer til at specificere information om filen. En **.ma-fil** kan åbnes og redigeres i enhver teksteditor for at løse eventuelle problemer med kommandoerne, hvis en fil bliver korrupt. Disse filer indeholder oplysninger til at definere 3D-sceneoplysninger såsom geometri, belysning, animation og gengivelse.

## MA filformat

MA-filer gemmes på disk i ASCII-tekstformat i modsætning til MB-filer, der gemmes i binært filformat på disk. En detaljeret reference til MA-filformat er tilgængelig i [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) og kan henvises til for udviklerens reference.

### MA-filoverskrift

MA-filoverskriften starter med en sektion med kommentarer, der giver oplysninger om filens oprettelse og datoen for ændringen. Maya-fillæsere ignorerer denne blok, da den kun bruges til informationsformål. En overskrift skal dog starte med de første seks tegn som //Maya.

ASCII-filoverskriften ser ud som følger.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Filreferencer

Filreferencesektionen i en .ma-fil indeholder information om alle andre Maya-filer, der refereres til i denne fil. Hver refereret fil kan læses ved hjælp af en enkelt filkommando, der er indeholdt i den samme fil. Syntaksen for filkommandoen, når den bruges til at referere, er:

```
file -r -rpr prefixString fileName;
```
eller

```
file -r -ns nameSpace fileName
```
Her er et eksempel på en streng.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Dette eksempel viser, at solobjektet indeholdt i filen `solar` ville være tilgængeligt i denne fil ved at bruge navnet solar_sun.

### Krav

Kravsektionen i en .ma-fil består af en række påkrævede kommandoer og fortæller May-oplysninger såsom version og plugin-oplysninger, der kræves for at læse filerne. Et eksempel på kravafsnittet er som følger.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Det næste afsnit specificerer kravene. Dette består af en række krævede kommandoer. Denne del af filen fortæller Maya, hvilken software der er nødvendig for at indlæse filen korrekt. Specifikt hvilken version af Maya, og hvilke plug-ins.

## MA fil download
Det er lidt svært at finde og downloade MA-filen af en 3d-model. Derfor kan du downloade en prøve MA-fil herfra:

- [Sample.ma](../sample.ma)


## Referencer

* [Organisation of Maya ASCII Files - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


