{
  "date" : "2019-10-11",
  "keywords" :[ "emf fájl", "emf fájl formátum", "mi az emf fájl", "fájl", "emf példa", "emf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Továbbfejlesztett metafájl formátum",
  "description":"További információ az EMF fájlformátumról és az API-król, amelyek EMF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az EMF fájl?

**A továbbfejlesztett metafájl formátum (EMF)** a grafikus képeket eszközfüggetlenül tárolja. Az EMF metafájljai változó hosszúságú rekordokat tartalmaznak időrendi sorrendben, amelyek a tárolt képet bármilyen kimeneti eszközön történő elemzés után renderelhetik. Ezek a változó hosszúságú rekordok lehetnek zárt objektumok definíciói, rajzolási parancsok és grafikus tulajdonságok, amelyek kritikusak a kép pontos megjelenítéséhez. Amikor egy eszköz megnyit egy EMF metafájlt a saját grafikus környezetével, az eredeti kép arányai, méretei, színei és egyéb grafikai tulajdonságai ugyanazok maradnak, függetlenül a megnyitó eszköz platformjától.

## Rövid története ##

1990-ben a Microsoft egy Windows Metafile ([WMF](/hu/image/wmf/)) képfájlformátumot tervezett a Microsoft Windows számára. A Windows metafájlok 16 bites formátumúak, amelyek tartalmazhatnak néhány bittérkép-összetevőt. A WMF vektorgrafikát tartalmazhat, és célja, hogy hordozható legyen a különböző alkalmazások között. 1993-ban a Win32/GDI bejelentette az Enhanced Metafile-t (EMF), egy újabb verziót, fokozott rugalmassággal és méretezhetőséggel. Az EMF grafikus nyelvi parancsokként is használható a nyomtató-illesztőprogramok futtatásához. A Microsoft mostantól a továbbfejlesztett metafájlformátumot (EMF) ajánlja a Windows-formátum (WMF) helyett. A Windows XP bemutatásakor megjelent az Enhanced Metafile Format Plus (EMF+) verzió. Ez az újabb verzió a GDI+ API-hívások sorba rendezésével találja meg az utat, és a WMF/EMF rögzíti a GDI-hívásokat. Létezik az EMF gzip tömörített változata, EMZ néven.

## EMF metafájl formátum ##

A továbbfejlesztett metafájl formátum alapvető elemei a következők:

* Egy EMR_HEADER (verzió, méret, a kép felbontása a létrehozáskor)
* Egy táblázat a GDI objektumokhoz
* Lefoglalt paletta (opcionális)
* Metafájl rekordok tömbstruktúrába rendezve (tulajdonságbeállítások, meghatározott objektumok, rajzparancsok)
* EMR_EOF rekord (utolsó rekord az EMF metafájlban)

## EMF verziók ##
* **Eredeti**: Az eredeti verzió meghatározza az eredeti kép megtartásához és eszközfüggetlenségének fenntartásához szükséges rekordot. Ezenkívül támogatja a grafikus objektumokat és a rajzoláshoz szükséges parancsokat tartalmazó rekordot.
* **1. verzió**: Az EMF második verziója javította a rugalmasságot és az eszközfüggetlenséget azáltal, hogy hozzáadta a pixelformátum rekordját és az OpenGL parancs használatára vonatkozó lehetőséget.
* **2. verzió**: A harmadik verzió javította a pontosságot azáltal, hogy hozzáadta a Metric rendszert az eszköz felületi távolságának mérésére, így a rekord skálázhatóbbá vált.

## Továbbfejlesztett metafile rekordok ##

A metafájl rekordok tömb formájában vannak elrendezve. Ezek a rekordok ENHMETARECORD szerkezetűek és változó hosszúságúak. Az ENHMETARECORD olyan adatokat határoz meg, amelyek GDI-függvényeket határoznak meg a kép létrehozásához továbbfejlesztett metafájl formátum használatával. Az **ENHMETAHEADER** szerkezet mindig az első rekord ebben a formátumban. Ez az EMF fejléc a következő információkat tartalmazza.

A továbbfejlesztett metafájl minden rekordja kezdetben két EMR-tagot tartalmaz (ez az alapstruktúrát biztosítja). Az első tag felismeri a GDI függvényt (a paraméterek a rekordban használatosak), amely meghatározza a rekord típusát, és iType néven ismert. A másik nSize tag határozza meg az egyes rekordok méretét. A fennmaradó paraméterek (ha vannak) és további adatok közvetlenül az nSize alatt rendezve. Közvetlenül a fejléc után opcionális szöveges leírás jelenhet meg. A kép és a szerző neve szerepel a szöveges leírásban. A paletta, amelynek jelenléte opció, meghatározza a továbbfejlesztett metafájlok létrehozásához használt színeket. A többi rekord a GDI funkció meghatározására szolgál, ami elengedhetetlen a képalkotáshoz.

Minden metafájlban legalább egy EMF rekordnak jelen kell lennie. Az egyik rekordból a másikba való áthaladási információ az EMF rekordoktól függ, ezért ezeket a rekordokat egymás mellett kell elhelyezni. A metafájl bármely adott rekordjánál, kivéve az EOF_record értéket, az adott rekord hossza határozza meg, hogy a következő rekordra lépjen.

## Továbbfejlesztett metafájlok létrehozása ##

A **CreateEnhMetaFile** funkció egy továbbfejlesztett metafájl létrehozására szolgál. Ennek a függvénynek az argumentumait használják a kép méretére és tárolására a lemezen/memóriában. Ezen túlmenően ez a funkció megköveteli annak az eszköznek a méretét, amelyben a kép először megjelent (referenciaeszköz), és a referenciaeszköz kontextusát (DC). Tehát a DC kezeléséhez szükséges argumentumokat meg kell adni a **CreateEnhMetaFile** függvény meghívásakor. A függvény szintaxisa a következő:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** fogantyú referenciaeszközhöz.

**lptoFilename:** A fájlnévre mutató mutató.

**lprc:** A pointer to ovális szerkezet megadja a kép méreteit mm-ben.

**lpDesc:** mutató a képet létrehozó kép címének és alkalmazásnevének karakterláncára.

## Továbbfejlesztett metafájl műveletek ##

Az alábbiakban felsoroljuk azokat a feladatokat, amelyeket egy továbbfejlesztett metafájl fogantyújával lehet végrehajtani.

* A tárolt kép megjelenítése és szerkesztése.
* Továbbfejlesztett metafájl-másolatok készítése.
* Lekérheti egy EMF-fejléc másolatát, az opcionális leírást és egy továbbfejlesztett metafájl bináris verzióját
* Ismételje meg a színeket a palettán.

## Grafikus objektumok ##

A rajzi és festési műveletekben a grafikai objektumok objektum létrehozási rekordokkal hozhatók létre, és menthetők el további felhasználásra. Egy `EMR_SELECTOBJECT` rekord le tudja kérni ezeket a grafikus objektumokat a lejátszóeszköz környezetének használatával. A tollak, paletták, ecsetek, színterek, betűtípusok és készletobjektumok néhány újrafelhasználható objektumtípus.

## Byte rendezés ##

A Little-endian formátumot az adatok metafájl rekordokban való tárolására használják.

## Verziószám ##

Az EMF fájlformátumot kétszer módosították. A módosított verziók az eredetiek, az 1-es és a 2-es kiterjesztésűek. A kiterjesztett verziók tartalmazzák az OpenGL-rekordokat és egy opcionális leírót a belső pixelformátumhoz. A kijelzett méretekhez hozzáadunk egy milliliteres mérési lehetőséget.

## Hivatkozások ##

* [Továbbfejlesztett formátumú metafájlok | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Továbbfejlesztett metafájl formátum és specifikáció](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

