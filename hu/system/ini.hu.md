{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "kiterjesztés", "fájl", "formátum", "rendszer", "kezdeményezés", "könyvtárkiterjesztés", "programok", "számítógép", "alkalmazás" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Initiation File Format",
  "description":"További információ az INI fájlformátumról és az INI-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Mi az INI fájl? ##

Az INI-fájl olyan számítógépes programok üzenetkonfigurációs dokumentuma, amelyek nyilvános kulcsokat tartalmaznak az attribútumokat keretrendszerben és nyelvtanban rendező jellemzőkhöz és szakaszokhoz. Ezek a rendszerfájlformátumú konfigurációs dokumentumok az MS-DOS operációs rendszer INI könyvtárkiterjesztéséről kapták a nevüket, amely az iniciációt jelenti. Népszerűsítette a szoftverbeállítás ezen formáját. Más szoftveralkalmazásokon sok program különféle fájlnév-kiegészítést használ, mint például a CONF és a [CFG](/hu/system/cfg/), bár a formátum számos konfigurációs helyzetben nem hivatalos szabványt hozott létre.

## Az INI-fájlok rövid története##

Kezdetben a Windows fő programkonfigurációs technikája egy szöveges fájlformátum volt, amely szövegsorokból állt, soronként egy döntő párral, szakaszokra osztva. Az eszközillesztőket, a betűtípusokat és az indító indítókat ebben a formátumban tároltuk. Az egyes beállításokat az alkalmazások általában INI-fájlokban is tárolták.
A Windows 3.1x-ig a formátumot a 16 bites Microsoft Windows platformok támogatták. A Windows 95-től kezdődően a Microsoft arra ösztönözte a fejlesztőket, hogy az INI-fájlok helyett a Windows Registry-t használják a konfigurációhoz.

## INI fájl – Fájlformátum specifikációi

### Kulcsok/Tulajdonságok ###

A kulcs/tulajdonság az INI-fájl legalapvetőbb eleme. Egy egyenlőség szimbólum (=) választja el az egyes kulcsok nevét és értékét. Az egyenlőségjeltől balra a név jelenik meg. Az egyenlőség szimbólum és a pontosvessző diszkrét betűk a Windows rendszerben, ezért nem használhatók a kulcsban. Az értékben bármilyen karakter használható.

```
name=value
```

### Szakaszok ###

A szakasz megjegyzése szögletes zárójelben ([]) jelenik meg a saját sorában. A szakasz meghatározása után az összes kulcs ehhez a szakaszhoz kapcsolódik. A szakaszok a következő szakaszmegjelöléssel vagy a dokumentum végén érnek véget; nincs külön "szakasz vége" elválasztó. A szakaszokat nem lehet egymásra rakni; csak egyszer nevezhetők meg, és nem kötelező összekapcsolni őket.

```
[section]
a=a
b=b
```

### Változó funkciók ###

Az INI fájlformátumnak nincs globálisan elfogadott definíciója. Számos számítógépes alkalmazás tartalmaz a már említetteken kívül további funkciókat is. Az alábbi lista néhány olyan általános jellemzőt tartalmaz, amelyek bármely egyedi programban szerepelhetnek, vagy nem.

* Hozzászólások
* Escape karakterek
* Ismétlődő nevek


## INI példa ##

A minta INI fájl a következőképpen néz ki:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Hivatkozási szám

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

