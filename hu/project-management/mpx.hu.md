{
  "date" : "2019-10-11",
  "keywords" :[ "mpx fájl", "mpx fájl formátum", "mi az mpx fájl", "fájl", "mpx példa", "mpx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange fájlformátum",
  "description":"További információ az MPX fájlformátumról és az MPX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Mi az MPX fájl? ##

Az .mpx kiterjesztésű fájl Microsoft Exchange fájlformátum. Az MPX fájlformátumot a Microsoft Project (MSP) fejlesztette ki, hogy megkönnyítse a projektinformációk cseréjét az MSP és az MPX fájlformátumot támogató egyéb alkalmazások között, beleértve a Primavera Project Planner, a Sciforma és a Timerline Precision Estimating alkalmazásokat. Az MPX-fájlok használatával mindenféle információt átvihet egy projektből egy másik rendszerbe, például részletes erőforrás-hozzárendelési információkat, naptárinformációkat vagy a Projektinformáció párbeszédpanelen található információkat.

A Microsoft Project 4.0 bevezette a Microsoft Project 98-on keresztül továbbra is használt MPX fájlformátumok létrehozásának és olvasásának támogatását. Az MPX fájlok létrehozásának támogatása azonban megszüntette a Microsoft Project 2000 kiadását, és a Microsoft Project 2010-ig tartó verziók csak az MPX olvasást támogatják. Az MPX fájlformátum nem támogatott az MSP 2010-nél újabb verziókban.

## MPX fájlformátum ##

Ebben a részben áttekintést adunk az MPX fájl specifikációiról. A teljes specifikáció megtalálható ebben a [Knowledge Base]-ban (https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) cikket, és a részletekért hivatkozni lehet rá.

### Rekordok ###

Az MPX fájl rekordja a projekt információit tartalmazza. Különféle típusú rekordok léteznek, ahol minden rekordnak saját sorrendje van. Minden rekordtípust a rekordszámuk azonosít. MPX fájl esetén tartalmaznia kell a File Creation rekordtípust. Más típusú rekordok nem kötelezőek. A következő táblázat az összes rekordtípust, azok rekordszámát, valamint az egyes típusok által az MPX fájlban található rekordok számát mutatja. Az MPX-fájlba való felvételnek követnie kell a táblázat sorrendjét, a megjegyzéseket bárhol be kell illeszteni.

|Rekord neve|Rekordszám|Rekordok maximális száma
---|---|---|
|Fájl létrehozása (kötelező)|nincs|1
|Pénznem beállítások|10|1
|Alapértelmezett beállítások|11|1
|Dátum és idő beállításai|12|1
|Alapnaptár definíció|20|250
|Alapnaptári órák|25| 7 Base Calendar Definition rekordonként
|Alapnaptár kivétel|26| 250 alapnaptár-definíciós rekordonként
|Projekt fejléc|30|1
|Szöveges erőforrás táblázat definíciója|140|1- (Vagy használhatja a Numerikus erőforrás táblázat definíció rekordját)
|Numerikus erőforrástábla definíciója|41|1
|Forrás|50|9999
|Forrásjegyzetek|51| 1 erőforrásrekordonként
|Forrásnaptár definíció|55| 1 erőforrásrekordonként
|Forrásnaptár nyitvatartási ideje|56| 7 erőforrásnaptáronként
|Forrásnaptár kivétel| 57|250 forrásnaptáronként
|Szöveges feladattábla definíció|60|1 (Vagy használhatja a Numerikus Feladattábla Definíció rekordot)
|Numerikus feladattábla definíciója|61|1
|Feladat|70|9
|Feladatjegyzetek|71| Feladatrekordonként 1
|Ismétlődő feladat|72| Feladatrekordonként 1
|Erőforrás hozzárendelés|75| Feladatrekordonként 100
|Munkacsoport-mezők hozzárendelése|76| Hozzárendelési rekordonként 1
|Projektnevek|80|500
|DDE és OLE ügyféllinkek|81|500
|Megjegyzések|0|korlátlan

### Fájlszerkezet ###

Az MPX fájl a fent említett rekordokból áll, amelyek a fájlon belül előre beállított módon vannak elrendezve. A rekordtípusok részleteit a következőképpen tárgyaljuk:

**Fájllétrehozási rekord (FCR):** Ez egy kötelező rekord, amelynek célja a következők azonosítása:

* Fájlformátum (MPX)
* A fájlban használt elválasztó karakterek listája
* A fájl létrehozásához használt program és verziószám
* A fájlban használt MPX fájlformátum verziószáma
* A fájl létrehozásához használt kódlap

Ennek kell lennie az első rekordnak a fájlban. A Microsoft Projectből történő exportáláskor a listaelválasztó karakter a Windows Vezérlőpult Területi beállítások elemében van megadva. Az FCR rekord a következő mezőket tartalmazza:

* MPX, amelyet közvetlenül a listaelválasztó karakter követ
* Program neve/azonosítója
* A fájl verziószáma
* Kódoldal (850, 437, MAC, ANSI)

Például a rekord tartalmazhat **MPX, Microsoft Project, 3.0** információt, amely meghatározza, hogy ebben az MPX-fájlban vessző legyen a listaelválasztó karakter. A fájlban használt MPX formátum verziója a Microsoft Project 3.0-s verziójából lett exportálva.

**Pénznembeállítások** Ez a 10-es rekordszámú rekord a Beállítások párbeszédpanel pénznembeállításainak beállításait adja meg. Ha ez a rekord nem szerepel, akkor a Beállítások párbeszédpanel aktuális beállításai kerülnek felhasználásra. Az ezres és a tizedes elválasztókat a Windows Vezérlőpultjának Területi beállítások eleme határozza meg.
A rekordban szereplő mezők a következők:

* Pénznem szimbólum
* Szimbólum helyzete (0 # után, 1 # előtt, 2 # után szóközzel, 3 # előtt szóközzel)
* Pénznem számjegyei (0,1,2)
* Ezres elválasztó
* Tizedes elválasztó

**Példa:** 10,$,1,2,",".
Ez a példa megadja, hogy a valutaértékek előtt szerepeljen egy dollárjel ($), hogy a tizedesvessző után két számjegy szerepeljen, vesszőt használjon az ezrek elválasztására, és egy pontot használjon tizedesvesszőként. Mivel a listaelválasztó karakter szerepel az Ezerelválasztó mezőben, a mezőt idézőjelek veszik körül.

**Alapértelmezett beállítások:** Ez a 11-es rekordszámú rekord megadja az alapértelmezett beállítások beállításait a Beállítások párbeszédpanelen. Ha az időtartam nincs megadva, az alapértelmezett időtartam egységet be kell állítani a megfelelő időtartam-mértékegység kiszámításához. Ha ez a rekord nem szerepel, akkor a Beállítások párbeszédpanel aktuális beállításai kerülnek felhasználásra.
A rekordban szereplő mezők a következők:

* Az időtartam alapértelmezett mértékegységei (0 # perc, 1 # óra, 2 # nap, 3 # hét)
* Alapértelmezett időtartam típusa (0 # nem rögzített, 1 # rögzített)
* Alapértelmezett munkaegységek (0 # perc, 1 # óra, 2 # nap, 3 # hét)
* Alapértelmezett óra/nap
* Alapértelmezett óra/hét
* Alapértelmezett normál díj
* Alapértelmezett túlóradíj
* Feladat állapotának frissítése Erőforrás állapot frissítése (0 # nem, 1 # igen)
* Folyamatban lévő feladatok felosztása (0 # nem, 1 # igen)

**Dátum- és időbeállítások:** Ez a 12-es rekordszámú rekord megadja a dátum- és időbeállításokat a Beállítások párbeszédpanelen, valamint a Bar Text Date Format opciót az Elrendezés párbeszédpanelen. Ha ez a rekord nem szerepel, akkor a Beállítások párbeszédpanel aktuális beállításai kerülnek felhasználásra.
\\A rekordban szereplő mezők a következők:

* Rendelés dátuma (0 # hónap/nap/év, 1 # nap/hónap/év, 2 # év/hónap/nap)
* Időformátum (0 # 12 óra, 1 # 24 óra)
* Alapértelmezett idő (éjfél utáni percek száma)
* Dátumelválasztó
* Idő elválasztó
* 0:00-11:59 Szöveg
* 12:00-23:59 Szöveg
* Dátumformátum (0-14)*
* Oszlopszöveg dátumformátuma (0 -194)*

**Alapnaptár definíció:** Ezek a 20-as rekordszámú rekordok határozzák meg az alapnaptárakat, valamint a hét munka- és szabadnapjait. Az alapértelmezett beállításokat használja a rendszer, ha nincs bejegyzés egy napra. Az alapértelmezett beállítások hétfőtől péntekig munkanapokon, szombat és vasárnap pedig munkaszüneti napokon. Ebben a rekordban a Név mező kitöltése kötelező. A napok mindegyikére a 0-s bejegyzés azt jelenti, hogy a nap munkaszüneti nap, az 1-es pedig azt, hogy a nap munkanap.
A rekordban szereplő mezők a következők:

* Név
* Vasárnap
* Hétfő
* Kedd
* Szerda
* Csütörtök
* Péntek
* Szombat

**Alapnaptári órák:** Ezek a 25-ös rekordszámú rekordok a hét napjaira adják meg a munkaidőt, ha eltérnek az alapértelmezett beállításoktól. Az alapértelmezett munkaidő 8:00 és 12:00 és 13:00 és 17:00 között. Minden alapnaptári óra rekord az előző alapnaptár definíciós rekordra vonatkozik. Legfeljebb hét ilyen rekord követheti az egyes Base Calendar Definition rekordokat.

* A hét napja (1-7, ahol 1 # vasárnap és 7 # szombat)
* 1. időponttól
* 1. időpontig
* 2. időponttól
* Az idő 2
* 3. időponttól
* Időhöz 3

**Alapnaptári kivétel:** Ezek a 26-os rekordszámú rekordok az előző két rekordtípusban meghatározott napok és órák kivételeit határozzák meg. Legfeljebb 250 ilyen rekord követheti az egyes Base Calendar Definition rekordokat. Ezeket a rekordokat időrendi sorrendben kell felsorolni. Ha a kivétel egy nap, a Dátum mezőt üresen hagyhatja. Ha nincs megadva idő, akkor az alapértelmezett 8:00 és 12:00, valamint 13:00 és 17:00 óra között kerül beállításra.
A rekordban szereplő mezők a következők:

* Dátumtól
* Randizni
* Nem dolgozik/dolgozik (0 # nem dolgozik, 1 # dolgozik)
* 1. időponttól
* 1. időpontig
* 2. időponttól
* Az idő 2
* 3. időponttól
* Időhöz 3

**Projektfejléc:** Ez a 30-as rekordértékkel rendelkező rekord globális projektmezőket állít be, például a projekt kezdő dátumát és befejezési dátumát. A rekord mezői megfelelnek a Projektadatok és Statisztika párbeszédpanelek információinak.
A rekordban szereplő mezők és fülek a következők:

* Projekt fül
* Vállalat
* Menedzser
* Naptár (Szabványos használat, ha nincs bejegyzés)
* Kezdő dátum (vagy ez a mező, vagy a következő mező számít egy importált fájlhoz, az Ütemezés kezdetétől függően)
* Befejezés dátuma
* Menetrend tól (0 # kezdés, 1 # cél)
* Mostani dátum*
* Hozzászólások
* Költség
* Alapköltség
* Tényleges költség
* Munka
* Alapmunka
* Tényleges munka
* Munka
* Időtartam*
* Alapidőtartam*
* Tényleges időtartam
* Teljesítés százaléka
* Kiindulási indítás
* Alapvonal befejezése
* Tényleges kezdés
* Tényleges befejezés
* Indítsa el az eltérést
* Finish Variancia
* Tantárgy
* Szerző
* Kulcsszavak

**Szöveges erőforrás táblázat meghatározása**: Ez a rekord felsorolja az importált vagy exportált erőforrásmezőket, sorrendben. Az importált fájlok nevének meg kell egyeznie a Microsoft Projectben használt mezőnevekkel. Az exportált fájlok esetében ez a rekord az erőforrás-exportálási táblából származik. Vagy ezt a rekordot, vagy a Numerikus erőforrástábla definíciós rekordját kell használni. A Microsoft Projectből történő exportáláskor mindkét rekord szerepel.

**Numerikus erőforrástábla definíciója:** Ez a rekord nevek helyett számokat használ, sorrendben felsorolja az importált vagy exportált erőforrásmezőket. Ez egy alternatív módszer az egyes erőforrásrekordokban található erőforrásmezők azonosítására, és hasznos egy idegen nyelvű termék által létrehozott MPX-fájl definiálásakor.

**Erőforrás:** Ezek a rekordok az egyes importált vagy exportált erőforrásokra vonatkozó információkat tartalmazzák. Minden erőforrásrekord egy erőforrást ír le. Amikor adatokat importál, a benne szereplő mezőket a szöveges erőforrástábla definíciója vagy a numerikus erőforrástábla definíciója rekord határozza meg. Az adatok exportálásakor az erőforrás-exportálási táblázatban szereplő mezők szerepelnek.

**Megjegyzések az erőforrásokról:** Ezek a rekordok megjegyzéseket tartalmaznak a közvetlenül megelőző erőforrásrekordról. A jegyzeten belüli új sorhoz a 127-es ASCII karakter kerül felhasználásra. Ha a jegyzet tartalmazza a listaelválasztó karaktert, tegye idézőjelek közé a megjegyzést.

**Erőforrás naptár meghatározása:** Ezek a rekordok határozzák meg a közvetlenül megelőző Erőforrás rekordban megadott erőforrás munkanapjait. Az importált fájlok esetében, ha nincs bejegyzés az Alapnaptárnév mezőben, akkor a rendszer a Szabványt használja. Az adott napra vonatkozó bejegyzés hiánya azt jelzi, hogy a nap alapértelmezettre van állítva (2). Ha nincsenek Erőforrás-naptár-definíciós rekordok, a szabványos rendszer az erőforrás alapnaptáraként szolgál, alapértelmezés szerint a napokra. A napok mindegyikére a 0-s bejegyzés azt jelzi, hogy az adott nap munkaszüneti nap, az 1-es azt, hogy a nap munkanap, a 2-es pedig az alapértelmezett beállítást.

**Erőforrás naptári órák:** Ezek a rekordok határozzák meg az erőforrás munkaidejét, amely eltér az erőforrás által használt alapnaptártól. Ezek a rekordok a közvetlenül ezt a rekordot megelőző Erőforrás-naptár-definíciós rekordra vonatkoznak. E rekordok közül legfeljebb hét követheti az egyes erőforrás-naptár-definíciós rekordokat.

**Erőforrás naptári kivétel:** Ezek a rekordok az előző két rekordtípusban meghatározott napok és órák alóli kivételeket határozzák meg. Legfeljebb 250 ilyen rekord követheti az egyes erőforrás-naptár-definíciós rekordokat. Ezeket a rekordokat időrendi sorrendben kell felsorolni. Ha a kivétel csak egy nap, akkor a Dátum mezőt üresen hagyhatja. Ha nincs megadva idő, akkor az alapértelmezett 8:00 és 12:00, valamint 13:00 és 17:00 óra között kerül beállításra.

**Szöveges feladattábla meghatározása:** Ez a rekord felsorolja az importálás vagy exportálás alatt álló feladatmezőket, sorrendben. Az importált fájlok nevének meg kell egyeznie a Microsoft Projectben használt mezőnevekkel. Ha a fájl exportálásra kerül, ez a rekord a feladat Exportálási táblájából származik. A Microsoft Projectből történő exportáláskor mindkét rekord szerepel. A Microsoft Project által kiszámított mezőket, például az ütemezett indítást és az ütemezett befejezést, a rendszer figyelmen kívül hagyja importáláskor. Ha a feladat kezdési vagy befejezési dátuma rögzített, használja a Kényszer típusa és a Kényszer dátuma mezőket.

**Numerikus feladattábla definíciója:** Ez a rekord nevek helyett számokat használ, sorrendben felsorolja az importált vagy exportált feladatmezőket. Ez egy alternatív módszer az egyes Task rekordokban található feladatmezők azonosítására, és akkor hasznos, ha idegen nyelvű termékkel létrehozott MPX-fájlt definiál.

**Feladat:** Ezek a rekordok az egyes importált vagy exportált feladatok adatait tartalmazzák. Minden Task rekord egy feladatot ír le. Amikor adatokat importál, a benne szereplő mezőket a szöveges feladattábla-definíciós rekord vagy a numerikus feladattábla-definíció rekord határozza meg. Az adatok exportálásakor a mezők szerepelnek az Exportálási feladat táblázatában.

**Feladat megjegyzések:** Ezek a rekordok megjegyzéseket tartalmaznak a közvetlenül megelőző feladatrekordról. Használja a 127-es ASCII karaktert a jegyzeten belüli új sor jelzésére. Ha a jegyzet tartalmazza a listaelválasztó karaktert, tegye idézőjelek közé a megjegyzést.

**Erőforrás-hozzárendelés**: Ezek a rekordok az előző Feladatrekordban definiált feladathoz rendelt erőforrásokról tartalmaznak információkat. Ha fájlokat egyesít, és meg szeretné őrizni az erőforrás-hozzárendelési információkat, akkor ezeket az információkat bele kell foglalnia az MPX-fájlba. Ha egyesíti, az egyesített feladatokhoz tartozó összes meglévő hozzárendelés törlődik. Ha egyedi azonosítók alapján egyesíti a fájlokat, az erőforrások az azonosítók helyett az egyedi erőforrás-azonosítók használatával kerülnek hozzárendelésre.

**Erőforrás-hozzárendelési munkacsoportmezők:** Ezek a rekordok a Microsoft Project 4.0 és 4.1 munkacsoport-szolgáltatásaihoz tartozó egyes hozzárendelésekkel együtt tárolt információkat tartalmazzák. Ha a Munkacsoport szolgáltatásait használja, akkor ezt a rekordot is fel kell vennie annak biztosítására, hogy az információk ne vesszenek el.

**Projektnevek:** Ezek a rekordok felsorolják a projektben tárolt összes DDE-hivatkozásnevet.

**DDE- és OLE-klienshivatkozások:** Ezek a rekordok felsorolják a projekthez vezető DDE-hivatkozásokat.

**Megjegyzések:** Ezek a rekordok megjegyzések hozzáadására használhatók a fájlhoz, és a fájl bármely pozíciójában megjelenhetnek. Minden megjegyzésrekordnak „0”-val kell kezdődnie.

## Problémák az MPX fájl megnyitásakor ##

Íme néhány gyakori probléma, amely előfordulhat, és az MPX formátum hibás működését okozhatja:

* A támogató szoftver hiánya
* Sérült fájl
* Vírus által fertőzött fájl
* Nincs hozzáférési jog a rendszerben a fájlok megnyitásához
* Elavult meghajtó a rendszerben
* A fájl kiterjesztése átnevezve

## Referenciák ##

* [MPX – Microsoft Tudásbázis](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

