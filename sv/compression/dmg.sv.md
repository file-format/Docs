{
  "date" : "2021-04-30",
  "keywords" :[ "DMG", "Komprimerad", "Fil", "Extension", "Filformat", "Apple Disk Image", "Macintosh" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMG - Apple Disk Image",
  "description":"Läs mer om DMG-filformat och API:er som kan skapa och öppna DMG-filer.",
  "linktitle" : "DMG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Vad är en DMG fil?

En fil med filtillägget .dmg är en Apple Disk Image-fil och känd som en Mac OS X Disk Image-fil. DMG-filformatet är den mest använda skivavbildsfilen som är avsedd att fördela applikationer och filer mellan Apple-datorer. Det är väldigt bekvämt att montera DMG-filer på en virtuell enhet eller kan använda Apple Disk Utility-programvara för att öppna och visa innehållet i DMG-filformatet. Den gamla versionen av IMG-filer som används i Mac OS Classic ersätts av DMG-filformatet. DMG-filer genereras för Mac-användare och stöds inte av Windows OS men användare kan komma åt DMG-innehållet i Windows operativsystem genom att använda komprimerings- och dekomprimeringsverktyg som 7-Zip, Pea Zip, etc. DMG-filtillägget används också av Oracle Export and Ingress-verktyget för scrapheap-filer som lagras i Oracle-databasens binära format.

## Kortfattad bakgrund

DMG-filtillägget utvecklades av Apple och används mest på Macintosh-datorer. Oftast används DMG-filen för att ge Mac-enheterna möjlighet att installera olika typer av filer och programvara som initieras från internet. DMG-filen är i grunden en monteringsbar skivbild som visas på ditt skrivbord när den öppnas. Filen innehåller rådata som i allmänhet är både krypterad och komprimerad. Mac-system behandlar DMG på samma sätt som de skulle behandla en skiva som var interfolierad, och de försöker omedelbart att öppna eller "spåra" filen.

## Tekniska specifikationer för DMG-filformat

* Speciellt skapad för Macintosh-datorer
* Utvecklad av Apple
* Filformatet är binärt
* Filkategori är Disk Image File
* Programmet som stöds är MacOS
* Kan innehålla en partitionstabell
* Kan innehålla alla typer av filsystem som HFS+
* Funktionalitet för att komprimera bilderna

