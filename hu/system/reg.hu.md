{
"dátum": "2023-03-07",
  "keywords": [
"reg fájl",
"mi az a reg fájl",
"fájl",
"reg fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "REG fájlformátum - Windows rendszerleíró fájl",
  "description":"További információ a REG formátumról és az API-król, amelyek REG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Mi az a REG fájl?

A REG fájl a Windows rendszerleíró adatbázis adatainak importálására vagy exportálására használt fájlformátum. A Windows Registry egy hierarchikus adatbázis, amely a Windows operációs rendszer és a telepített alkalmazások konfigurációs beállításait és beállításait tárolja. A rendszerleíró adatbázis olyan információkat tartalmaz, mint a felhasználói beállítások, alkalmazásbeállítások, hardver- és szoftverkonfigurációs adatok stb.

A REG fájl általában ".reg" kiterjesztésű, és egy egyszerű szöveges fájl, amely rendszerleíró bejegyzések és értékek sorozatát tartalmazza meghatározott formátumban. A formátum egy fejlécrészből áll, amely a fájlt rendszerleíró fájlként azonosítja, majd egy sor kulcs- és értékpárból áll, amelyek a rendszerleíró bejegyzéseket képviselik.

## REG fájlformátum - További információ

Íme egy példa a reg fájlformátumra:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

A fájl első sora a rendszerleíró adatbázis-szerkesztő verzióját adja meg. A következő sorok a rendszerleíró adatbázis bejegyzéseit kulcsútvonal formátumban tartalmazzák, amelyet értéknév és értékadatok követnek. Ebben a példában a reg fájl két bejegyzést tartalmaz: az egyiket, amely hozzáad egy "Example.exe" nevű programot a Windows indítási listájához, és egy másikat, amely a Windows Intéző speciális beállításaiban a "Hidden" értékét "true"-ra állítja.

Reg fájlok létrehozhatók és szerkeszthetők szövegszerkesztővel, például Jegyzettömbbel. Gyakran használják biztonsági mentési és visszaállítási célokra, valamint több számítógép konfigurálására ugyanazokkal a beállításjegyzék-beállításokkal.

## A Windows rendszerleíró adatbázis importálása vagy exportálása

A REG-fájl egy olyan fájltípus, amelyet adatok importálására vagy exportálására használnak a Windows rendszerleíró adatbázisából. A Windows Registry egy hierarchikus adatbázis, amely a Windows operációs rendszer és a telepített alkalmazások konfigurációs beállításait és beállításait tárolja. A rendszerleíró adatbázis olyan információkat tartalmaz, mint a felhasználói beállítások, alkalmazásbeállítások, hardver- és szoftverkonfigurációs adatok stb.

A Reg fájlok használhatók beállításjegyzék-bejegyzések létrehozására vagy módosítására, és gyakran használják biztonsági mentési és visszaállítási célokra, valamint több számítógép konfigurálására ugyanazokkal a beállításjegyzék-beállításokkal. A következőképpen adhat hozzá reg fájlt egy új beállításjegyzék-bejegyzés hozzáadásához a Windows rendszerleíró adatbázisához:

1. Hozzon létre egy új szövegfájlt egy szövegszerkesztővel, például a Jegyzettömbbel.
2. Írja be a rendszerleíró adatbázis bejegyzést a megfelelő formátumban. A formátum egy fejléc részből áll, amely a fájlt rendszerleíró fájlként azonosítja, majd egy sor kulcs- és értékpárból áll, amelyek a rendszerleíró bejegyzéseket képviselik. Íme egy példa:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Ez létrehoz egy új „Példa” nevű kulcsot a „Szoftver” kulcs alatt az aktuális felhasználó rendszerleíró adatbázisában, és a „Setting1” értékét „Érték1”-re állítja.

3. Mentse el a fájlt .reg kiterjesztéssel.
4. Kattintson duplán a .reg fájlra, hogy hozzáadja az új rendszerleíró bejegyzést a Windows rendszerleíró adatbázisához.

A rendszer kéri, hogy erősítse meg, hogy hozzá kívánja-e adni a bejegyzést a rendszerleíró adatbázishoz. A megerősítést követően az új bejegyzés hozzáadódik a rendszerleíró adatbázishoz, és ellenőrizheti azt a Rendszerleíróadatbázis-szerkesztő eszközzel.

## Hivatkozások
* [Windows Registry](https://en.wikipedia.org/wiki/Windows_Registry)

