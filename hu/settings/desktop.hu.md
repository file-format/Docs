{
"dátum": "2023-05-31",
  "keywords": [
"asztali fájl",
"mi az asztali fájl",
"mit tartalmaz az asztali fájl",
"példa asztali fájl",
"hogyan lehet megnyitni az asztali fájlt",
"mi az asztali fájl formátuma",
"fájl",
"asztali fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "ASZTAL Fájlformátum - Asztali bejegyzési fájl",
  "description":"További információ az DESKTOP formátumról és az API-król, amelyek DESKTOP fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Mi az a DESKTOP fájl?

A .desktop fájl egy konfigurációs fájl, amelyet Linux asztali környezetek használnak az alkalmazások parancsikonjainak és indítóinak meghatározására. Metaadatokat biztosít egy alkalmazásról, például annak nevét, ikonját, végrehajtandó parancsát és egyéb tulajdonságait. Ezeket a fájlokat általában parancsikonok létrehozására használják az alkalmazásmenükben, az asztali indítókban vagy a Linux-alapú rendszerek paneleiben.

## Mit tartalmaz a DESKTOP fájl?

A .desktop fájl meghatározott formátumot követ, és több kulcsmezőt tartalmaz:

- **[Asztali bejegyzés]:** Ez a .desktop fájl fő szakaszának fejléce.
- **Név:** Az alkalmazás nevét adja meg.
- **Megjegyzés:** Rövid leírást vagy megjegyzést ad az alkalmazásról.
- **Exec:** Az alkalmazás indításakor végrehajtandó parancsot határozza meg.
- **Ikon:** Megadja az alkalmazáshoz társított ikonfájl elérési útját.
- **Terminal:** Meghatározza, hogy az alkalmazás terminálablakban fut-e.
- **Típus:** Meghatározza a bejegyzés típusát, például „Alkalmazás” vagy „Link”.
- **Kategóriák:** Meghatározza azokat a kategóriákat vagy csoportokat, amelyek alatt az alkalmazás megjelenjen a menüben.
- **StartupNotify:** Megadja, hogy az asztali környezet mutasson-e indítási értesítést az alkalmazáshoz.
- **NoDisplay:** Meghatározza, hogy az alkalmazás el legyen-e rejtve a menükből.
- **Műveletek:** Meghatározza az alkalmazáson végrehajtható további műveleteket, például egy adott fájl megnyitását.

## Példa DESKTOP fájl

Íme egy példa egy .desktop fájlra egy "MyTextEditor" nevű fiktív szövegszerkesztőhöz:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Ebben a példában a .desktop fájl határozza meg a "MyTextEditor" alkalmazást a hozzá tartozó tulajdonságokkal. Két további műveletet is tartalmaz, az "Új ablak megnyitása" és a "Meglévő fájl megnyitása", amelyek az alkalmazásindító helyi menüjéből érhetők el.

Ha egy .desktop fájlt meghatározott könyvtárakba, például `/usr/share/applications` vagy `~/.local/share/applications` elhelyez, az asztali környezet felismeri azt, és ennek megfelelően megjeleníti az alkalmazást a menükben, vagy lehetővé teszi, hogy innen indítsuk el. asztali.

## DESKTOP fájl - Mivel nyitható meg?

Számos szoftver képes megnyitni és kezelni a .desktop fájlokat. Ezek a programok általában fájlkezelők vagy asztali környezetek Linux alapú rendszereken. Íme néhány példa:

- **Nautilus (Fájlok):** Az alapértelmezett fájlkezelő a GNOME asztali környezethez.
- **Nemo:** A fájlkezelő a Cinnamon asztali környezethez.
- **Dolphin:** Az alapértelmezett fájlkezelő a KDE Plasma asztali környezethez.
- **Thunar:** Az alapértelmezett fájlkezelő az Xfce asztali környezethez.
- **KDE menüszerkesztő:** A KDE Plasma asztali környezetre jellemző eszköz, amely lehetővé teszi a .desktop fájlok megtekintését és szerkesztését.

Ezek a fájlkezelők és asztali környezetek grafikus felületet biztosítanak a .desktop fájlok kezeléséhez. Lehetővé teszik a .desktop fájlok tulajdonságainak megtekintését és szerkesztését, alkalmazásindítók létrehozását és parancsikonok rendszerezését az alkalmazásmenükben vagy az asztalon.

A .desktop fájlok egyszerű szöveges fájlok, így tetszőleges szövegszerkesztővel is megnyithatja és szerkesztheti őket. Egyszerűen kattintson a jobb gombbal a .desktop fájlra, és válassza a „Megnyitás” vagy a „Megnyitás másik alkalmazással” lehetőséget, hogy szövegszerkesztőt válasszon a telepített programok listájából.

## Mi a DESKTOP fájl formátuma?

A .desktop fájlformátum meghatározott szerkezetet és formátumot követ. Ez egy egyszerű szöveges fájl, amely kulcs-érték párokat tartalmaz szakaszokba rendezve. Íme a formátum áttekintése:

- **Szakaszfejlécek:** Minden szakasz szögletes zárójelben ([]) lévő fejléccel kezdődik. Az elsődleges szakasz neve általában [Desktop Entry], amely az alkalmazás vagy az indító fő metaadatait tartalmazza.
- **Kulcs-érték párok:** Az egyes szakaszokon belül kulcs-érték párok segítségével határozhatja meg a tulajdonságokat. A formátum "Kulcs=Érték". A kulcs azonosítja a tulajdonságot, az érték pedig a megfelelő adatokat szolgáltatja.
- **Tulajdonság szintaxisa:** A tulajdonságértékek különböző típusúak lehetnek, beleértve a karakterláncokat, logikai értékeket, fájl útvonalakat vagy listákat. Az egyes tulajdonságértékek formátuma a típusától függ.
- **Megjegyzések:** Megjegyzéseket írhat a .desktop fájlba a „#” szimbólum használatával. Bármi, ami a "#" karakter után következik, megjegyzésnek minősül, és figyelmen kívül hagyja.

## Hivatkozások
* [Asztali bejegyzés fájlok](https://www.baeldung.com/linux/desktop-entry-files)

