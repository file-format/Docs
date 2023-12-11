{
"dátum": "2023-06-12",
  "keywords": [
"bak",
"bak fájl",
"BAK Chromium könyvjelzők",
"mi az a bak fájl",
"hogyan kell megnyitni a bak fájlt",
"fájl",
"bak fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK fájlformátum - Chromium Bookmarks Backup",
  "description":"További információ a BAK Chromium Bookmarks formátumról és az API-król, amelyek BAK-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## Mi az a BAK fájl?

A .bak fájlok a Chromium-alapú webböngészők, például a Google Chrome és a Microsoft Edge kontextusában lényegében a könyvjelzők biztonsági másolata. Ezeket a könyvjelzőket a rendszer egyszerű szöveges listaként menti, és a használt fájlformátum JSON. Ezeknek a .bak-fájloknak az a célja, hogy megóvják könyvjelzőit azáltal, hogy biztonsági másolatot készítenek, amely véletlen törlés vagy elvesztés esetén visszaállítható.

A Chromium-alapú böngészők, köztük a Google Chrome, rutinszerűen létrehozzák ezeket a biztonsági mentési fájlokat, és általában a „Bookmarks.bak” nevet adják nekik. Ezek lényegében a könyvjelzők pillanatképei egy adott időpontban.

## Hogyan lehet .bak fájlt használni a könyvjelzők visszaállításához

1. **Keresse meg a biztonsági másolat fájlt:** Általában a Chromium-profiljához társított meghatározott mappában található. A pontos hely az operációs rendszertől függően változhat.

Windowson: Nézze meg a `C:\Users\ mappát<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

MacOS rendszeren: Keressen a `~/Library/Application Support/Chromium/Default/Bookmarks.bak` helyen.

Linuxon: Ellenőrizze a `~/.config/chromium/Default/Bookmarks.bak` elemet.

3. Győződjön meg arról, hogy a Chromium böngésző be van zárva.
4. Nevezze át a „Bookmarks.bak” fájlt a „.bak” kiterjesztés eltávolításával, így egyszerűen „Könyvjelzőknek” nevezik.
5. Indítsa el a Chromiumot.

Ha a .bak fájlt „Könyvjelzők”-re nevezi át, a Chromium azt fogja használni a jelenlegi könyvjelzőfájlként, és vissza kell állítani a korábbi könyvjelzőket.

## Chromium könyvjelzők biztonsági mentése

A Chromium-könyvjelzők biztonsági mentése bölcs óvintézkedés annak biztosítására, hogy ne veszítse el fontos mentett weboldalait és URL-címeit. A Chromium egy nyílt forráskódú böngésző, amely más böngészők, például a Google Chrome és a Microsoft Edge alapjául szolgál. A Chromium-könyvjelzők biztonsági mentéséhez kövesse az alábbi lépéseket:

## 1. módszer: Manuális biztonsági mentés

1. **Chromium megnyitása**: Indítsa el a Chromium böngészőt számítógépén.

2. **A könyvjelzők elérése**: Kattintson a három függőleges pontra (menüikon) a böngészőablak jobb felső sarkában. A legördülő menüből vigye az egérmutatót a „Könyvjelzők” fölé a könyvjelzők almenü megjelenítéséhez.

3. **Könyvjelzők exportálása**: A könyvjelzők almenüben kattintson a "Könyvjelzőkezelő" elemre. Ezzel megnyílik egy új lap, amely megjeleníti a könyvjelzőit.

4. **Könyvjelzők exportálása**: A Könyvjelzőkezelő lapon kattintson ismét a három függőleges pontra (általában a jobb felső sarokban) a könyvjelzőkezelő menü megnyitásához. Ebből a menüből válassza a "Könyvjelzők exportálása" lehetőséget.

5. **Válassza ki a helyet**: Válassza ki, hová szeretné menteni az exportált könyvjelzőfájlt a számítógépén. Az alapértelmezett fájlnév a "bookmarks.html", de tetszés szerint megváltoztathatja. Mentse el egy olyan helyre, amelyre emlékezni fog.

6. **Mentés**: Kattintson a "Mentés" vagy az "Exportálás" gombra a könyvjelzők HTML-fájlként történő mentéséhez.

A könyvjelzőiről most biztonsági másolat készült HTML-fájlként. Ezt a fájlt biztonsági okokból átmásolhatja egy külső meghajtóra vagy felhőtárhelyre.

## 2. módszer: Szinkronizálás Google-fiókkal (ha van)

Ha bejelentkezett egy Google-fiókba a Chromiumban, használhatja a beépített szinkronizálási funkciót is, hogy biztonságban tartsa könyvjelzőit, és szinkronizálva legyen az eszközök között. Így a könyvjelzőiről automatikusan biztonsági másolat készül Google-fiókjában.

1. **Nyissa meg a Chromiumot**: Indítsa el a Chromium böngészőt, és győződjön meg arról, hogy be van jelentkezve Google-fiókjába.

2. **Szinkronizálás engedélyezése**: Kattintson a három függőleges pontra (menüikon) a böngészőablak jobb felső sarkában, és lépjen a "Beállítások" elemre.

3. **Szinkronizálás és Google-szolgáltatások**: A Beállítások lapon kattintson a "Szinkronizálás és Google szolgáltatások" elemre a bal oldalsávon.

4. **Adatok szinkronizálása**: A „Szinkronizálás” alatt győződjön meg arról, hogy a „Könyvjelzők” be van kapcsolva. Ezzel szinkronizálja könyvjelzőit Google-fiókjával.

Könyvjelzőiről most automatikusan biztonsági másolat készül, és szinkronizálódik Google-fiókjával. Ezeket úgy érheti el, hogy bejelentkezik Google-fiókjába bármely olyan eszközön, amelyen Chromium vagy más böngésző támogatja a Google szinkronizálását.

Ne felejtsen el időnként manuálisan is biztonsági másolatot készíteni könyvjelzőiről, különösen akkor, ha olyan helyi másolatot szeretne, amely nem kizárólag a Google-fiókja szinkronizálásától függ.

## BAK fájl megnyitása

Ha szeretné felfedezni a könyvjelzők biztonsági mentésének nyers adatait, megnyithatja a "Bookmarks.bak" fájlt különféle szövegszerkesztőkkel, például Microsoft Visual Studio Code (több platformon elérhető), Microsoft Notepad (Windows felhasználóknak), Apple TextEdit segítségével. (Mac-felhasználóknak), vagy bármely más, az Ön által választott szövegszerkesztővel. Ezzel megtekintheti a fájlban található könyvjelzőket és metaadatokat.

Megnyithatja a "Bookmarks.bak" fájlt, és megtekintheti annak tartalmát különféle szövegszerkesztő szoftverek és kódszerkesztők segítségével. Íme néhány gyakran használt lehetőség:

1. Visual Studio Code (VS Code)
2. Jegyzettömb (Windows)
3. TextEdit (Mac)
4. Magasztos szöveg
5. Jegyzettömb++
6. Atom
7. nano és Vim (Linux)
8. WordPad (Windows)

## Egyéb BAK fájlok

Íme más fájltípusok, amelyek a **.bak** fájlkiterjesztést használják.

**Adatbázis**
- [BAK - Adatbázis biztonsági mentési fájl](/hu/database/bak/)
- [BAK - Swiftpage Act! Adatbázis biztonsági mentése](/hu/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/hu/database/bak-sqlserver/)

**Játszma, meccs**
- [BAK - Terraria World vagy Player Backup](/hu/game/bak-terraria/)

**Egyéb**
- [BAK - Backup File](/hu/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/hu/misc/bak-finale/)
- [BAK - MobileTrans Backup](/hu/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/hu/misc/bak-vegas/)

**Beállítások**
- [BAK - Holo Launcher Backup](/hu/settings/bak-holo/)

## Hivatkozások
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
