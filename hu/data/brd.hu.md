{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BRD Fájl - EAGLE Circuit Board fájl - Mi az .brd fájl és hogyan nyitható meg?",
  "description" : "Ismerje meg a BRD EAGLE áramköri fájl fájlt és annak megnyitását.",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-hu",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mi az a BRD fájl?

A BRD fájlformátumot használják az elektronikus tervezési automatizálási (EDA) szoftverben a nyomtatott áramköri lapok (PCB) tervezéséhez. PCB tervező szoftverek, mint például az Eagle, KiCad, Altium Designer és mások ezt a fájlformátumot használják a nyomtatott áramköri lapok elrendezésének, csatlakozásainak és egyéb tervezéssel kapcsolatos információk tárolására.

A BRD-fájl egyfajta CAD-fájl, amely digitális fájlok, amelyeket mérnökök és tervezők használnak tervek létrehozására, módosítására és elemzésére. A BRD fájl az Autodesk EAGLE-hez kapcsolódik, amely egy szoftveralkalmazás, amelyet az elektronikai iparban gyakran használnak nyomtatott áramköri kártyák (PCB) tervezésére. Az Autodesk EAGLE eszközöket biztosít mind a sematikus rögzítéshez (az áramkör vizuális megjelenítéséhez), mind a PCB-elrendezéshez (összetevők elrendezéséhez és összeköttetések útválasztásához).

A BRD fájl az EAGLE Layout Editor segítségével jön létre, amely az Autodesk EAGLE szoftvercsomag része. Ez a szerkesztő lehetővé teszi a felhasználók számára a PCB elrendezésének megtervezését, beleértve az alkatrészek elhelyezését, a nyomvonalak irányítását, a tervezési szabályok meghatározását és a gyártáshoz szükséges fájlok létrehozását.

A BRD fájlok sablonként vagy tervrajzként szolgálnak az elektronikus áramkörök tervezéséhez a PCB-n. A tervezők az EAGLE és .brd fájlokat használják sematikus diagramjaik lefordításához fizikai elrendezésekké, amelyeket le lehet gyártani.

A .BRD fájlok Gerber fúróadat-formátumban menthetők. A Gerber fájlok szabványos formátumok, amelyeket a PCB-gyártásban használnak a NYÁK-tervezés mintáinak, rétegeinek és jellemzőinek leírására. A .brd” fájlok ebbe a formátumba történő mentése lehetővé teszi, hogy számítógéppel segített gyártási (CAM) programok használják őket, amelyek a PCB gyártásához szükséges utasításokat generálják.

## BRD fájlnézegető

Számos szoftvereszköz áll rendelkezésre a .brd” fájlok megtekintéséhez, amelyek lehetővé teszik a felhasználók számára az Autodesk EAGLE-hez hasonló szoftverrel létrehozott PCB-elrendezések megjelenítését és ellenőrzését.

1.  **Autodesk EAGLE**: Ha rendelkezik hozzáféréssel az Autodesk EAGLE-hez, egyszerűen megnyithatja a .brd” fájlokat közvetlenül a szoftveren belül megtekintés és szerkesztés céljából.
    
2.  **KiCad**: A KiCad egy nyílt forráskódú EDA szoftvercsomag, amely PCB-elrendezés-szerkesztőt is tartalmaz. Képes importálni és megtekinteni az Autodesk EAGLE segítségével létrehozott .brd fájlokat.
    
3.  **ViewPlot**: A ViewPlot egy önálló Gerber megjelenítő, amely támogatja a különböző PCB fájlformátumokat, beleértve a .brd fájlt is. Lehetővé teszi a felhasználók számára, hogy eredeti tervezőszoftver nélkül tekintsék meg a PCB-terveket.
    
4.  **GC-Prevue**: A GC-Prevue egy másik népszerű Gerber-megjelenítő, amely .brd fájlokat is képes kezelni. Funkciókat biztosít a NYÁK-elrendezések megjelenítéséhez, a távolságok méréséhez és a tervezési részletek ellenőrzéséhez.
    
5.  **Gerbv**: A Gerbv egy nyílt forráskódú Gerber megjelenítő, amely támogatja a Gerber fájlok megtekintését, amelyek tartalmazhatnak Gerber formátumban mentett .brd fájlokat is.
    
6.  **Online Viewer Tools**: Vannak olyan online eszközök is, amelyek lehetővé teszik a .brd fájlok feltöltését és megtekintését közvetlenül a böngészőben. Ilyen például az EasyEDA Online Gerber Viewer, amely támogatja a különféle PCB-fájlok, köztük a Gerber és a .brd megtekintését.

## BRD fájl - Mivel nyitható meg egy BRD fájl?

A PCB tervezésben használt BRD fájlok különféle PCB tervező alkalmazásokban nyithatók meg.

- **Autodesk EAGLE**: Ez az Autodesk által kifejlesztett többplatformos PCB-tervező szoftver. Támogatja sematikus diagramok, NYÁK-elrendezések készítését és az elektromos csatlakozások útválasztását. A felhasználók a .brd fájlokat közvetlenül az Autodesk EAGLE-ben nyithatják meg megtekintés és további szerkesztés céljából.
    
- **Altium Designer**: Az Altium Designer átfogó PCB-tervező szoftver, elsősorban Windows operációs rendszerekhez. A funkciók széles skáláját kínálja a sematikus rögzítéshez, a PCB-elrendezéshez és a tervezési elemzéshez. Az Altium Designer támogatja a .brd fájlok megnyitását is, lehetővé téve a felhasználók számára, hogy más szoftverekkel létrehozott terveket importáljanak és dolgozzanak velük.
    
- **Open Board Viewer**: Az Open Board Viewer egy kifejezetten Linux operációs rendszerekhez tervezett PCB-megtekintési szoftver. Ez egy nyílt forráskódú eszköz, amely lehetővé teszi a felhasználók számára a PCB-elrendezések megjelenítését, az összetevők ellenőrzését és az útválasztás részleteit. Az Open Board Viewer támogatja a .brd fájlok megnyitását, lehetővé téve a Linux platformok felhasználóinak, hogy megtekintsék és elemezzék a más szoftverekben létrehozott terveket.

Itt található a BRD fájlok megnyitásához használható programok listája.

- **Autodesk EAGLE** (ingyenes próbaverzió) (Windows, Mac, Linux)
- **Altium Designer** (ingyenes próbaverzió) (Windows, Mac, Linux)
- **Open Board Viewer** (ingyenes) Linuxhoz

## Hivatkozások
* [EAGLE program](https://en.wikipedia.org/wiki/EAGLE_(program))


