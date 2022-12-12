{
  "date" : "2019-12-13",
  "keywords" :[ "ppt fájl", "ppt fájl formátum", "mi az a ppt fájl", "fájl", "ppt példa", "ppt fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a PPT fájlformátumról és az API-król, amelyek PPT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PPT - PowerPoint fájlformátum",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PPT fájl?

A PPT kiterjesztésű fájl olyan PowerPoint fájl, amely diagyűjteményből áll, és diavetítésként jeleníthető meg. Meghatározza a Microsoft PowerPoint 97-2003 által használt bináris fájlformátumot. A PPT-fájlok többféle információt tartalmazhatnak, például szöveget, felsorolásjeles pontokat, képeket, multimédiát és egyéb beágyazott OLE-objektumokat. A Microsoft 2007-től újabb, [PPTX](/hu/presentation/pptx/) néven ismert PowerPoint fájlformátumot dolgozott ki, amely az Office OpenXML-en alapul, és eltér ettől a bináris fájlformátumtól. Számos más alkalmazás, például az OpenOffice Impress és az Apple Keynote is létrehozhat PPT-fájlokat.

## Rövid története ##

A Microsoft a PowerPoint 1987-es kiadásával vezette be a PPT fájlformátumot. A stabil bináris formátumot alapértelmezésként osztották meg a PowerPoint 97-2003 for Windows rendszerben. A bináris fájlformátumot a PowerPoint legújabb verziói, beleértve a PowerPoint 2016-ot is, az olvasáshoz és az íráshoz támogatják.

## Fájlformátum specifikációi ##

Bevezetése óta a PPT fájlformátum számos felülvizsgálaton ment keresztül, új funkciókkal és fejlesztésekkel bővítve. A legfrissebb verzió specifikációi a 2018 augusztusában közzétett 6.0-s verzióhoz tartoznak, amelyet nem szabad összekeverni a PPT fájlformátum valós termékszámával, mivel a Microsoft már nem módosítja ezt a formátumot.

### Fájlformátum áttekintése ###

A PPT fájlformátum néhány kulcsfontosságú összetevője a következő:

#### Diák ####

A felhasználói adatok, például alakzatok, szövegek, animációk és médiák hozzáadódnak a dián belüli prezentációhoz. Egy prezentáció egy vagy több diát tartalmazhat, amelyek diavetítésként jelennek meg a prezentáció futtatásakor. A prezentáció mesterdiákat és címmesterdiákat tartalmaz, amelyek sablonként szolgálnak a bemutatódiák általános vizuális tulajdonságaihoz. Létezik egy jegyzet-fődia és a kiosztott fődia is, amely hasonló célt szolgál, és közös vizuális tulajdonságokat biztosít az összes jegyzetdiához és minden nyomtatott szóróanyaghoz.

#### Formák ####

Az alakzatok olyan objektumok, amelyek lehetővé teszik a felhasználók számára, hogy helyőrző alakzatok, képek és grafikonok formájában változatos tartalmat adjanak egy diához. A fődián lévő alakzatok közös adatokat határoznak meg alakzatcsoportokhoz.

#### Helyőrző alakzatok ####

Ezek speciális helyőrzők, amelyek különféle objektumok konténereiként szolgálnak. Különböző helyőrző alakzatok használhatók bizonyos típusú alakzatok, például táblázatok vagy diagramok beszúrásához. A dián belül egy helyőrző alakzat alkalmazkodik a fő fődia, a cím fődia vagy a jegyzetfődiák vizuális tulajdonságaihoz.

#### Külső objektumok ####

Külső objektumok, például beágyazott és csatolt hang, linkelt videó, beágyazott és hivatkozott OLE-objektumok és hiperhivatkozások beágyazhatók egy diába. Ezek az objektumok használhatók csatolt objektumok aktiválására külső erőforrásokhoz való hozzáféréshez diavetítés közben.

### Fájlformátum-struktúrák ###

A PowerPoint bináris fájlformátumai a következő adatfolyamokból állnak, amelyek a dokumentum általános szerkezetét és adatait képviselik.

* Jelenlegi felhasználói adatfolyam
* PowerPoint Document Stream
* Képek Stream
* Összefoglaló információ és dokumentum-összefoglaló információ (opcionális)

A DOC fájlformátum teljes specifikációja megtalálható a [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) szerint, és meg kell nézni a következő részletekben említett szakaszokra hivatkozva.

#### Jelenlegi felhasználói adatfolyam ####

Nyilvántartást vezet a dokumentumot utoljára megnyitó felhasználóról, és a nevének „Jelenlegi felhasználó”-nak kell lennie.

#### PowerPoint dokumentumfolyam ####

Rögzíti a PowerPoint prezentációval kapcsolatos összes információt, és elmagyarázza annak elrendezését és tartalmát. Ez egy kötelező adatfolyam, amelynek a nevének „PowerPoint-dokumentum”-nak KELL lennie. Ennek az adatfolyamnak a tartalmát a legfelső szintű rekordok sorozata határozza meg. A rekordszekvencia részleges rendezési korlátozásait a PersistDirectoryAtom és a UserEditAtom rekordok határozzák meg.

Konténerrekordként a DocumentContainer, MainMasterContainer (2.5.3. szakasz), HandoutContainer (2.5.8. szakasz), SlideContainer (2.5.1. szakasz) és NotesContainer (2.5.6. szakasz) rekordok a tárolórekordok fájának gyökerei. és atom rekordok. Bármely tárolórekordon belül más rekordok is létezhetnek, amelyek nincsenek kifejezetten gyermekrekordként felsorolva. Az ismeretlen rekordok akkor kerülnek azonosításra, ha a RecordHeader szerkezet recType mezője (2.3.1. szakasz) olyan értéket tartalmaz, amelyet a RecordType felsorolás (2.13.24. szakasz) nem adott meg. Ezeket az ismeretlen rekordokat figyelmen kívül kell hagyni, és meg kell őrizni<1>. Az ismeretlen rekordok figyelmen kívül hagyhatók, ha a RecLen bájtokat előre keresi a RecordHeader struktúra végéről.

Minden alkalommal, amikor ezt az adatfolyamot írják, új legfelső szintű rekordok, felhasználói szerkesztések fűzhetők a meglévő adatfolyamhoz, vagy a teljes adatfolyam tartalma lecserélhető a legfelső szintű rekordok frissített sorozatára. Ha a teljes adatfolyamot nem cserélik le, a korábbi felhasználói szerkesztéseket tartalmazó, korábban létező legfelső szintű rekordok elavulttá tehetők a később hozzáfűzött legfelső szintű rekordokkal, amelyek az aktuális felhasználói szerkesztést tartalmazzák.

#### Képfolyam ####

Ez egy opcionális adatfolyam, amely adatokat tartalmaz a PowerPoint-prezentációban található képekről. A nevének „Képek” KELL lennie. Ennek az adatfolyamnak a tartalmát az OfficeArtBStoreDelay rekord határozza meg az [MS-ODRAW] 2.2.21 szakaszában meghatározottak szerint.

#### Összefoglaló információs adatfolyam ####

Statisztikát vezet a dokumentumról a Microsoft Office szabvány szerint. Az Összefoglaló információs adatfolyam nevének "\005SummaryInformation"-nak kell lennie, ahol a \005 a 0x0005 értékű karakter, nem pedig a "\005" karakterlánc. Ezt az adatfolyamot ki KELL hagyni a titkosított dokumentumoknál. Ennek az adatfolyamnak a tartalmát az [MS-OSHARED] 2.3.3.2.1. szakasza határozza meg.

#### Dokumentum-összefoglaló információs adatfolyam ####

Egy opcionális adatfolyam, amelynek neve "\005DocumentSummaryInformation" kell legyen, ahol a \005 a 0x0005 értékű karakter, nem pedig a "\005" karakterlánc. Ez az adatfolyam<2> elhagyható a titkosított dokumentumoknál. Ennek az adatfolyamnak a tartalmát az [MS-OSHARED] 2.3.3.2.2. szakasza határozza meg.

#### Titkosított összefoglaló információs adatfolyam ####

Egy opcionális adatfolyam, amelynek a nevének "EncryptedSummary" KELL lennie. Ez az adatfolyam csak titkosított dokumentumban létezik. Ennek az adatfolyamnak a tartalmát az [MS-OFFCRYPTO] 2.3.5.4. szakasza határozza meg.

#### Digitális aláírás tárolása ####

Egy opcionális tároló, amelynek neve "_xmlsignatures" legyen. LEHET, hogy kihagyja és figyelmen kívül hagyja. Ennek a tárhelynek a tartalmát az [MS-OFFCRYPTO] 2.5.2. szakasza határozza meg.

#### Egyéni XML adattárolás ####

Egy opcionális tároló, amelynek neve "MsoDataStore" legyen. A tároló tartalmát az [MS-OSHARED] 2.3.6. szakasza határozza meg.

#### Aláírások adatfolyama ####

Egy opcionális adatfolyam, amelynek neve "_signatures" legyen. El KELL hagyni, és figyelmen kívül kell hagyni. Ennek az adatfolyamnak a tartalmát az [MS-OFFCRYPTO] 2.5.1. szakasza határozza meg.

## Referenciák ##

* [PPT fájlformátum specifikációi](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] – Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint fájlformátumok](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

