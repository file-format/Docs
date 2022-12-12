{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az AHK fájlformátumról és az API-król, amelyek AHK-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"AHK fájlformátum - AutoHotkey Script File",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Mi az AHK fájl?

Az AHK-fájl az AutoHotkey szoftveralkalmazással létrehozott szkriptfájl, amelyet a Microsoft Windows feladatok automatizálására használnak. Utasításokat tartalmaz a feladatok gyorsbillentyűk segítségével történő automatizálásához, amelyek azonnali műveletek végrehajtására használhatók. A fájlt az AutoHotkey hajtja végre, és az összes műveletet egymás után hajtja végre. Az AHK fájlok elég erősek ahhoz, hogy összetett feladatokat hajtsanak végre a gyorsbillentyűkkel meghatározott gyorsbillentyűkkel. Az AHK fájlok olyan szövegszerkesztőkkel nyithatók meg, mint a Microsoft Notepad és a Notepad++.

## AHK fájlformátum

Az AHK-fájlok egyszerű szöveges fájlokként kerülnek a lemezre, és olyan kódsorokat tartalmaznak, amelyeket az AutoHotkey futtathat. Az AutoHotkey egy ingyenes, nyílt forráskódú szkriptnyelv, amely lehetővé teszi a felhasználók számára, hogy egyszerű és összetett szkripteket hozzanak létre olyan műveletek végrehajtásához, mint például űrlapkitöltések, automatikus kattintás, makrók végrehajtása stb. Egy AHK-fájl legalább egyetlen műveletet hajthat végre, majd kiléphet. .

Vannak olyan eszközök, amelyekkel az AHK [Exe](/hu/executable/exe/) fájlokká konvertálható.

### AHK példa

A következő példa a Win+Z billentyűket használja a Microsoft Jegyzettömb futtatásához, vagy előtérbe helyezéséhez, ha már fut.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Hogyan hozhatok létre AHK fájlt?

A következő lépésekkel hozhat létre AHK fájlt. Ezek feltételezik, hogy az AutoHotkey már telepítve van a gépen.

* Kattintson jobb gombbal az asztalon.
* Keresse meg az "Új" elemet a menüben.
* Kattintson az "AutoHotkey Script" gombra az "Új" menüben.
* Adjon új nevet a szkriptnek.
* Keresse meg az újonnan létrehozott fájlt az asztalon, és kattintson rá jobb gombbal.
* Kattintson a "Szkript szerkesztése" gombra.
* Egy ablaknak fel kellett volna bukkannia, valószínűleg a Jegyzettömbnek.
* Mentse el a fájlt.

## Hivatkozások

* [AutoHotkey](https://www.autohotkey.com/)
* [Batch fájl – a Wikipewdia által](https://en.wikipedia.org/wiki/Batch_file)

