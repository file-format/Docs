{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fájl készítése - Xcode Makefile Script File",
  "description":"További információ az XCode MakeFile formátumról és az API-król, amelyek MakeFile fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Mi az a MAKE fájl?

A MAKE fájl egy XCode parancsfájl, amely megszervezi a kód összeállítását. Több forráskódfájlból való programok összeállítására és összekapcsolására szolgál. Ez segít eldönteni, hogy egy nagy alkalmazás mely részeit kell újrafordítani, amikor az alkalmazást frissíteni kell. Állítsa be a fájlok futtatását egy sor utasítás alapján, attól függően, hogy mely fájlok változtak.

## MAKE fájlformátum példa

A következő tartalom a Make segédprogrammal kerül végrehajtásra, és a kimenetek a következők.

```
hello:
	echo "hello world"
```
**Kimenet létrehozása**

```
$ make
echo "hello world"
hello world
```

## Hivatkozások
* [XCode and Make – Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Object-C útmutató](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

