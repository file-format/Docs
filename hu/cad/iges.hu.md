{
  "date" : "2020-03-16",
  "keywords" :[ "IGES-fájl", "Fájlformátum", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az IGES fájlformátumról és az API-król, amelyek IGES fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"IGES fájlformátum",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Mi az IGES fájl?

Egy .iges kiterjesztésű fájl a tervezési információk cseréjére szolgál a számítógéppel támogatott tervezési (CAD) alkalmazások között. Az IGES az Initial Graphics Exchange Specifications rövidítése. Az IGES használatával kicserélt információ magában foglalja az áramköri rajzot, a drótvázat, a szabad formájú felületet vagy a szilárdtestmodellezési ábrázolásokat. Az IGES a hagyományos mérnöki rajzokban, modellelemzésekben és gyártási funkciókban találja meg alkalmazásait. A formátum 2D és 3D tervezési információkat egyaránt képes cserélni a CAD programok között. Az IGES-fájlok számos CAD-alkalmazással megnyithatók, például az Autodesk és a CADSoftTools ABViewer segítségével. Számos API is elérhető az IGES-fájlok programozott megnyitásához és konvertálásához.

## IGES fájlformátum

Az IGES fájlok ASCII szövegformátumúak, és bármely szövegszerkesztőben megnyithatók a fájl tartalmának megtekintéséhez. Az IGES-fájl szöveges információi „Hollerith” formátumban vannak ábrázolva. Egy általános IGES-fájl több ezer sort tartalmazhat, amelyek az ebben a formátumban cserélhető 2D vagy 3D információkat jeleníthetik meg. Az IGES-fájl öt részre van osztva, amelyeket a 73. oszlopban a nagybetűvel jelölnek. Ezek a szakaszok a "Kezdés" (S), "Globális" (G), "Adatbevitel" (D), "Paraméteradatok" (P) és "Megszakítás" (T) szakaszok. Az Adatbevitel és a Paraméteradatok szakaszok rövidítése általában DE, illetve PD.

### IGES fájlfejléc

A Start és a Globális szakasz alapvető információkat tartalmaz a következőkről:
* A fájl neve és forrása
* Határolók a Paraméteradatok részhez
* A fájl szerzője és egyéb általános információk.

A Wikipédián található példadokumentum Start és Global szakaszai a következők.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Amint látható, a kezdőmező a fájl ember által olvasható leírását tartalmazza, és az 1-72. oszlopokban vannak karakterek, a sor a szakasz fejlécével és a szakasz sorszámával végződik. A Start szakaszból legalább 1 sornak kell lennie. A globális szakasz előfeldolgozó adatokat tartalmaz. Ezenkívül jelen kell lennie a fájlban, és G000000# formátumban kell végződnie.

### Adatbevitel (DE) és Paraméteradatok (PD) szakasz

#### Adatbeviteli szakasz
Egy IGES fájl több entitásból áll, amelyek az IGES fájlformátum alapadataira vonatkozó információkat tartalmazzák. Egy entitás egy IGES adatformátum különböző elemeiről tartalmaz információkat, és rajzolásra szolgál. A gyakrabban használt entitások a következők:
* Körív
* Összetett görbe
* Kúpív
* Repülőgép
* Vonal

Ez csak néhány, és körülbelül 150 különböző entitás található az IGES-ben. Minden entitást egy típusszám azonosít, például:
* KÖRÍV (100-as típus)
* LINE (110-es típus)

##### Entitás tulajdonságai

Minden deklarált entitás a következő tulajdonságokkal rendelkezik.

|Mező neve|Leírás|
---|---|
|Entitástípus |Ez a leírt entitás típusa. Például a 116 egy Point entitást ír le.|
|PD pointer |Ez adja meg az entitásadatok helyét a Paraméteradatok részben. Ez a hely egyszerűen a sorszám a PD szakaszon belül, amely az entitásadatok első sorát tartalmazza.|
|Struktúra |Nulla vagy mutató a definíciós entitásra. A legtöbb entitásra nem vonatkozik|
|Line Font Pattern| Szám vagy mutató vonal betűtípusminta entitás. A szám jelentése: * 0 Nincs megadva minta (alapértelmezett) * 1 Folyamatos * 2 Szaggatott * 3 Fantom * 4 Középvonal * 5 Pontozott|
|Szint| Meghatározza az entitáshoz társítandó szinteket. Lehetővé teszi az entitás egynél több szinten való megjelenését|
|Megtekintés| Meghatározza a megtekintési beállításokat. Ezek a következők: 0 Egyenlő láthatóságot és jellemzőket jelöl minden nézetben. Alapértelmezett mutató a Nézet entitásra (410-es típus), amely megtekinthető a Hivatkozás egy nézet látható asszociációs entitásra (402-es típus, 3-as űrlap)
|Transformation Matrix pointer| Hivatkozik egy transzformációs mátrix entitásra (124-es típus), vagy alapértelmezés szerint nulla (nincs transzformáció)|
|Címke megjelenítési asszociativitás| Hivatkozik egy címkemegjelenítési asszociativitásra (402-es típus, 5-ös űrlap), amely meghatározza az entitáscímke megjelenését.|
|Állapotszám| Két szám négy szakaszát tartalmazza. 1-2: Üres állapot. Vagy 00 a normál vagy 01 az üres. 3-4: Az alárendelt entitás kapcsolója: 00 a független, 01 a fizikailag függő, 02 a logikai függő és 03 mindkettő esetében. 5-6: Entitáshasználati jelző: vagy 00 a geometriához, 01 az annotációhoz, 02 a definícióhoz, 03 az egyébhez, 04 a logikaihoz, 05 a 2D parametrikushoz és 06 az építési geometriához. Végül a 7-8 a hierarchia, ahol a 00 a globális felülről lefelé (az entitás jellemzőit használja), a 01 a globális halasztás (ne használja ennek az entitásnak a jellemzőit), a 02 pedig a hierarchia tulajdonság használata (hierarchia entitás használata (406-os típus, űrlap) 10)a hierarchikus csoportosítás jellemzőinek meghatározása).|
|Sorozatszám| D# határozza meg, ahol a # a szakasz sorszáma (nem a fájl tetejétől). Ezt az adatbeviteli entitásra is használják.|
|Entitás típusa| entitáslistánként kétszer van megadva|
|Vonalsúly száma| Meghatározza a vastagságot az entitás megjelenítésekor. A legkisebb értéke 1, a 0 az alapértelmezett|
|Színszám| Megadja az entitás színét. A megengedett egész értékek a következők: 0 Nincs szín (alapértelmezett) 1 Fekete 2 Piros 3 Zöld 4 Kék 5 Sárga 6 Bíbor 7 Cián 8 Fehér|
|Paraméter sorszáma| Megadja, hogy ez az entitás hány sort foglal el a Paraméteradatok szekcióban|
|Űrlapszám| Az entitás formáját vagy reprezentációját jelzi. Módosítja a paraméteradatok értelmezését. Az alapértelmezett érték 0|
|Fenntartott mező| Nem használt|
|Fenntartott mező| Nem használt|
|Entity Label| Alkalmazás meghatározott azonosító- jogosított|
|Alsó indexszám| Az entitáscímke numerikus minősítője. Mindkettő együtt egyedi azonosítót alkot az entitásnak|
|Sorozatszám Lásd fent. |Ez D#+1 lesz, mivel minden entitás két sorban van megadva.|

#### Paraméter adatrész
Az Adatbevitelek szakaszt a Paraméteradatok szakasz követi. Felsorolja az egyes bejegyzések adatait, és felsorolja az entitás paramétereit a Globális részben megadott elválasztójelek alapján (általában vessző a paraméterek elválasztásához, pontosvessző pedig a lista befejezéséhez).


## Hivatkozások
* [IGES a WikiPediától](https://en.wikipedia.org/wiki/IGES)

