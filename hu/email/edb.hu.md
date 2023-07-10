{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB fájlformátum - Exchange Mail adatbázis-fájl",
  "description":"További információ az EDB fájlformátumról és az API-król, amelyek EDB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Mi az EDB fájl?

Az .edb kiterjesztésű fájl a Microsoft Exchange Server által létrehozott postafiók-adatbázis a levelezéssel kapcsolatos adatok tárolására. Az EDB, az Exchange Database a folyamatban lévő és nem SMTP-alapú üzeneteket tárolja. Az EDB-t Extensible Storage Engine (ESE) adatbázis-fájlokként is ismerik, és a fájlokat b-tree struktúrával tárolják. Tárolófájlokként az EDB-fájlok más levéltároló fájlformátumokká konvertálhatók, például [PST](/hu/email/pst/) és [OST](/hu/email/ost/).

## EDB fájl formátum

Nem áll rendelkezésre hivatalos/nyílt EDB fájlformátum specifikáció, amelyre hivatkozni lehetne. Némi előrelépés történt a fájlformátum visszafejtése terén, ami részleges specifikációk dekódolását eredményezte. Ezek szerint az EDB fájl a következőkből áll:
* Fájlfejléc – Adatbázisfájl fejléc-információkat tartalmaz
* Fix méretű oldalak - Tartalmazza a táblázatokat és indexeket tartalmazó adatbázist

### Adatbázisfájl fejléce
Az adatbázisfájl fejléce az első adatbázis-oldalon található, és legalább 668 bájt. A fájlfejléc a többi mező mellett tartalmazza a "Fájlformátum verziója" és a "Fájltípus" mezőket.

#### Fájl típusok
|Típus|Leírás
---|---|
|0| Adatbázis|
|1| Streaming|

`Megjegyzés:` Ezeknek a típusoknak az azonosítói nem ismertek.

#### Fájlformátum verziója
Az EDB eredeti formátuma 1997 áprilisában indult, és ezt követően folyamatosan változott.

|Verzió dátuma|Verzió|Feldolgozás|leírás
---|---|---|---|
|1997. ápr.| 0x00000620|0x00000000| Az operációs rendszer eredeti béta formátuma.|
|1997. május |0x00000620|0x00000001| Adjon hozzá oszlopokat a katalógushoz a feltételes indexeléshez és a OLD.|
|1997. június|0x00000620|0x00000002|Adja hozzá a fLocalizedText jelzőt az IDB-hez.|
|1997. október|0x00000620|0x00000003|SPLIT_BUFFER hozzáadása a térfa gyökéroldalaihoz.|
|1998. január|0x00000620|0x00000002|Változtassa vissza a változatot, hogy az ESE97 továbbra is kompatibilis maradjon.|
||0x00000620|0x00000003|Új címkézett oszlopok hozzáadása a katalógushoz ("CallbackData" és "CallbackDependencies").|
|1998. május|0x00000620|0x00000004|Super Long Value (SLV) támogatás: signSLV, fSLVLétezik a dbheaderben.|
|1998. május|0x00000620|0x00000005|Új SLV térfa.|
|1998. október|0x00000620|0x00000006|SLV űrtérkép.|
|1998. december|0x00000620|0x00000007|4 bájtos IDXSEG.|
|1999. január|0x00000620|0x00000008|Új sablon oszlopformátum.|
|1999. június|0x00000620|0x00000009|Rendezett sablonoszlopok. A Windows XP SP3|-ban használatos
||0x00000620|0x0000000b|Tartalmazza az oldal fejlécét az Exchange-ben használt ECC ellenőrzőösszeggel|
||0x00000620|0x0000000c|Windows Vista (SP0) rendszerben használatos|
||0x00000620|0x00000011|2 KiB, 16 KiB és 32 KiB oldalak támogatása.Kibővített oldalfejléc további ECC-ellenőrző összegekkel.Oszloptömörítés.Szóközi tippek.Windows 7 (SP0) rendszerben használatos|
|1999. május|0x00000623|0x00000000|Új Space Manager.|

### Adatbázis fájlok

Az EDB adatbázisfájl tartalmazza az adatbázisban lévő összes tábla sémáját. Ezenkívül tartalmazza az összes adatbázistáblázat rekordját és a táblákhoz tartozó indexeket. Helyét a következő azonosítók határozzák meg.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Ezek alapján az adatbázis állapota a következőképpen értékelhető.

|Érték|Azonosító|Leírás
---|---|---|
|1|JET_dbstateJustCreated|Az adatbázis most jött létre.|
|2|JET_dbstateDirtyShutdown|Az adatbázis kemény vagy puha helyreállítást igényel, hogy használható vagy mozgatható legyen. Ebben az állapotban nem szabad megkísérelni az adatbázisok mozgatását.|
|3|JET_dbstateCleanShutdown|Az adatbázis tiszta állapotban van. Az adatbázis naplófájl nélkül csatolható.|
|4|JET_dbstateBeingConverted|Az adatbázis frissítése folyamatban van.|
|5|JET_dbstateForceDetachInternal|Ez az érték a WindowsXP-ben került bevezetésre|
 

## Hivatkozások
* [Extensible Storage Engine (ESE) adatbázisfájl (EDB) specifikációi](https://github.com/libyal/libesedb/tree/main/documentation)

