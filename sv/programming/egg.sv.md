{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG-filformat - Python-distributionsfil",
  "description":"Läs mer om EGG-filformat och API:er som kan skapa och öppna EGG-filer.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Vad är en EGG fil?

En EGG-fil, även känd som Python-ägg, är ett äldre distributionsformat Python-distributioner. Det är ett [ZIP](/sv/compression/zip/) komprimerat arkiv med .egg-tillägget och innehåller Python-applikationens källfiler tillsammans med metainformation om distributionen. EGG-filer är alternativ till en Windows Executable [EXE](/sv/executable/exe/)-fil men är plattformsoberoende. Detta äldre format för Python-distributioner har ersatts med det nyare Wheel (WHL) filformatet i början av 2010.

## EGG filformat

EGG-filer sparas som komprimerade ZIP-arkiv. Det betyder att om du ersätter tillägget .egg med .zip kommer du att kunna öppna det med vanliga dekompressionsverktyg som Corel WinZIP, Microsoft Explorer eller RARLAB WinRAR.

EGG-filer kan skapas med paketet **distutils** som finns tillgängligt av Python. Ett annat verktyg som kan skapa och öppna EGG-filer är **SetupTools**. EGG-filer kan installeras som ett paket med **easy_install**.

`OBS - EGG-filformatet har blivit föråldrat till förmån för det nya hjulet WHL-filformatet.`

## Referens ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)

