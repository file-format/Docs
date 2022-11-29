{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Gör fil - Xcode Makefile skriptfil",
  "description":"Läs mer om XCode MakeFile-format och API:er som kan skapa och öppna MakeFile-filer.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Vad är en MAKE-fil?

En MAKE-fil är en XCode-skriptfil som organiserar kompilering av kod. Den används för att kompilera och länka program från flera källkodsfiler. Detta hjälper till att avgöra vilka delar av en stor applikation som måste kompileras om när applikationen behöver uppdateras. Få filer att använda en serie instruktioner för att köra beroende på vilka filer som har ändrats.

## MAKE Filformat Exempel

Följande innehåll körs med hjälp av verktyget Make och utgångarna är som följer.

```
hello:
	echo "hello world"
```
**Gör utdata**

```
$ make
echo "hello world"
hello world
```

## Referenser
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

