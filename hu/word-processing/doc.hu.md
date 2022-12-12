{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "file", "extension", "file format", "Word", "Document" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word dokumentumfájl",
  "description":"További információ a DOC fájlformátumról és az API-król, amelyek DOC fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Mi az a DOC fájl?

A .doc kiterjesztésű fájlok a Microsoft Word vagy más szövegszerkesztő dokumentumok által generált dokumentumok bináris fájlformátumban. A bővítményt kezdetben egyszerű szöveges dokumentációhoz használták több különböző operációs rendszeren. Számos különböző típusú adatot tartalmazhat, például képeket, formázott, valamint egyszerű szöveget, grafikonokat, diagramokat, beágyazott objektumokat, hivatkozásokat, oldalakat, oldalformázást, nyomtatási beállításokat és még sok mást. A formátum népszerű volt mindenféle dokumentáció esetében, mivel számos lehetőséget kínál a felhasználóknak kézikönyvek, javaslatok, specifikációk, önéletrajzok, cikkek vagy hasonló dokumentumok írásához. A DOC frissített verziója a [DOCX](/hu/Word%20Processing/DOCX/), amely az Office OpenXML-en alapul, amelynek specifikációi nyíltan elérhetők.

## Rövid története ##

A WordPerfect, a [Corel] (https://www.corel.com/en/) terméke a DOC-t használta saját formátumának kiterjesztéseként. Az 1980-as években a WordPerfect maradt a legtöbb számítógépen a könnyű elérhetősége, a legtöbb számítógépes géppel és operációs rendszerrel való kompatibilitása miatt. A WordPerfect bukását azonban a Windows operációs rendszeren tapasztalta, amikor a Microsoft bemutatta a Microsoft Word-t, mint dokumentumfájlformátumú termékét, és a DOC kiterjesztést választotta saját formátumuknak. Ahogy a Microsoft Word egyre népszerűbbé vált, a DOC fájlformátumot a Microsoft Word 97 - 2003 között többször módosították. 2007-ben az alapértelmezett DOC fájlformátumot az Office Open XML formátum (DOCX néven ismert) váltotta fel, és a program új verziói A Microsoft Word mostantól ezt az új kiterjesztést használja alapértelmezett fájlformátumként.

## A DOC fájlformátum specifikációi – További információ

A Microsoft sokáig nem adta ki a DOC fájlformátum specifikációit, egészen 2008-ig. 2008 februárjában a Microsoft Open Specification Promise értelmében kiadták a .doc fájlformátumra vonatkozó formátumspecifikációkat. Bár a specifikáció nem írja le a DOC formátum által használt összes szolgáltatást, bőséges információt ad az ezzel a fájlformátummal való munkavégzéshez szükséges ismeretekkel kapcsolatban. Ennek ellenére visszafejtésre van szükség a rendelkezésre álló információk felhasználásához. A specifikációkat többször frissítették, és a legújabb [változat](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) a 8.0, amely 2018 augusztusában frissült .

### Néhány alapfogalom ###

Mielőtt belemennénk a DOC fájlformátum-specifikációinak részleteibe, néhány alapvető fogalmat meg kell értenünk ahhoz, hogy ezzel a fájlformátummal dolgozhassunk.

**Fájlinformációs bázis (Fib):** A Fib szerkezet információkat tartalmaz a dokumentumról, és meghatározza a fájlmutatókat a dokumentumot alkotó különböző részek felé.
A Fib egy változó hosszúságú szerkezet. A rögzített méretű alaprész kivételével minden szakaszt egy számlálómező előz meg, amely megadja a következő szakasz méretét.

**Karakterpozíció:** A CP vagy a Karakterpozíció egy előjel nélküli, 32 bites egész szám, amely egy karakter nulla alapú indexeként szolgál a dokumentum szövegében. A fájlban lévő egyes karakterek helye és mérete nem kérhető le közvetlenül, és előre meghatározott algoritmussal kell kiszámítani. A karakterek a következők:

* A dokumentum szövege
* Objektumok, például lábjegyzetek vagy szövegdobozok horgonyai
* Vezérlőkarakterek, például bekezdésjelek és táblázatcellajelek

**PLC:** A PLC-struktúra CP-k tömbje, amelyet adatelemek tömbje követ. Bármely PLC adatelemeinek azonos méretűnek, nulla vagy több bájtnak kell lenniük, ezért a CP-k számának eggyel többnek kell lennie, mint az adatelemek számának. A PLC-struktúrák különböző típusúak, és mindegyik típus meghatározza, hogy engedélyezettek-e a duplikált CP-k az adott típushoz vagy sem. A PLC szerkezet a következőkből áll:

* **aCP (változó hosszúság):** CP elemek tömbje. A **PLC** struktúra mindegyik típusa meghatározza a CP elemek jelentését és a megengedett tartományt.
* **aData (változó hosszúságú):** A **PLC** struktúrák mindegyik típusa meghatározza az adatelemek szerkezetét és jelentését, az adatelemek számára vonatkozó korlátozásokat, valamint a bennük lévő adatokra vonatkozó korlátozásokat. Meghatározza az adatelemek és a megfelelő CP-k közötti kapcsolatot is.

**Érvényes kijelölés:** A .DOC fájl konstrukciókat főként a CP-k tartománya írja le. A Microsoft számos [szabályt] (https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) határoz meg, amelyeket ilyen esetben be kell tartani.

**STTB:** Az STTB egy karakterlánc-tábla, amely egy fejlécből áll, amelyet elemek tömbje követ. A **cData** érték a tömbben található elemek számát adja meg.

**Tulajdonságok tárolása:** A Word fájl különböző elemeket tartalmazhat, például szöveget, bekezdéseket, táblázatokat, képeket és szakaszokat, amelyek mindegyikének saját tulajdonságai lehetnek. Ezek tulajdonságai az alapértelmezetttől eltérően a Word fájlban tárolódnak. Az ilyen különbségeket a PRl határozza meg, amely egy tulajdonságmódosítóból (Sprm) és annak operandusából áll. Egy alkalmazás a **Prl** listák alkalmazásával meghatározhatja a tulajdonságok végső halmazát.

**Jelszóvédelem:** A Word fájlok jelszóval is védhetők, amelyhez az alábbi mechanizmusok egyike használható.

* XOR zavarás
* Office bináris dokumentum RC4 titkosítás
* Office bináris dokumentum RC4 CryptoAPI titkosítás

Ha a FibBase.fEncrypted és a FibBase.fObfuscation egyaránt 1, akkor a fájl XOR obfuszkációval homályosításra kerül.

Ha a FibBase.fEncrypted értéke 1, a FibBase.fObfuscation pedig 0, akkor a fájl titkosítása Office Binary Document RC4 titkosítással vagy Office Binary Document RC4 CryptoAPI titkosítással történik, az EncryptionHeader a T FibBase.lKey adatfolyam első FibBase.lKey bájtjában tárolva. Az EncryptionHeader.EncryptionVersionInfo meghatározza, hogy melyik titkosítási mechanizmust használták a fájl titkosításához.

### Fájlszerkezet ###

A bináris Word-fájl eredetiségében egy összetett OLE-fájl, amely több tárolóból és adatfolyamból áll. Ezeknek a tárolóknak és adatfolyamoknak saját szerkezetük és méretük van, amelyek meghatározzák az írási és olvasási paramétereket. Ezek:

#### WordDocument Stream ####

Ez az adatfolyam tartalmazza a dokumentum szövegét és a fájl más részeiből hivatkozott egyéb információkat. Az adatfolyamnak nincs előre meghatározott struktúrája, kivéve az elején lévő FIB-t, amely kötelező, és 0-nak kell lennie. Ez az adatfolyam nem lehet nagyobb 2147 MB-nál.

#### 1TableStream vagy 0TableStream ####

Egy bináris Word-fájl tartalmazhat 1Table stream vagy 0Table stream néven ismert táblázatfolyamokat. Ezek közül legalább egynek szerepelnie kell a dokumentumban. Ha azonban egy dokumentum 1Table és 0Table adatfolyamot is tartalmaz, akkor csak a base.fWhichTblStm által hivatkozott adatfolyam kerül felhasználásra. A hivatkozás nélküli adatfolyamot figyelmen kívül kell hagyni.
Az asztali adatfolyam NEM lehet nagyobb 2147 MB-nál.

#### Adatfolyam ####

Az adatfolyamnak nincs előre meghatározott szerkezete. Olyan adatokat tartalmaz, amelyekre a FIB-ből vagy a fájl más részeiből hivatkoznak. Ennek az adatfolyamnak nem kell jelen lennie, ha nincs rá hivatkozás. Az adatfolyam NEM lehet nagyobb 2147 MB-nál.

#### Tárgytárhely ####

Az objektumkészlet tárolója a beágyazott OLE-objektumok tárolóit tartalmazza. Ennek a tárolónak nem kell jelen lennie, ha nincsenek beágyazott OLE objektumok a dokumentumban.

#### Egyéni XML adattárolás ####

Az Egyéni XML-adattár egy opcionális tároló, amelynek neve "MsoDataStore" legyen.

#### Összefoglaló információs adatfolyam ####

A Summary Information adatfolyam egy opcionális adatfolyam, amelynek a nevének "\005SummaryInformation" KELL lennie, ahol a \005 a 0x0005 értékű karakter, nem pedig a "\005" karakterlánc.

#### Dokumentum-összefoglaló információs adatfolyam ####

A Dokumentumösszesítő információs adatfolyam egy opcionális adatfolyam, amelynek a nevének "\005DocumentSummaryInformation" KELL lennie, ahol a \005 a 0x0005 értékű karakter, nem pedig a "\005" karakterlánc.

#### Titkosítási adatfolyam ####

A titkosítási adatfolyam egy opcionális adatfolyam, amelynek a nevének "titkosításnak" KELL lennie. Ennek az adatfolyamnak NEM SZABAD jelen lennie, hacsak nem teljesül mindkét alábbi feltétel:

* A dokumentum Office Binary Document RC4 CryptoAPI titkosítással van titkosítva.
* Az fDocProps értéke az EncryptionHeader.Flags mezőben van beállítva.

#### Makrótárhely ####

A Makrótároló egy opcionális tároló, amely a fájl makróit tartalmazza. Ha van, akkor projekt gyökértárnak KELL lennie.

#### XML aláírások tárolása ####

Az XML-aláírások tárolója egy opcionális tároló, amelynek a nevének „_xmlsignatures”-nek KELL lennie.

#### Aláírások adatfolyama ####

Az aláírások adatfolyama egy opcionális adatfolyam, amelynek neve "_signatures" legyen. Ez az adatfolyam digitális aláírásokat tartalmaz.

#### Információjog-kezelés Adatterület tárolása ####

Az információjog-kezelési adatterület tároló egy opcionális tároló, amelynek a nevének "\006DataSpaces" KELL lennie, ahol a \006 a 0x0006 értékű karakter, nem pedig a "\006" karakterlánc. Ha ez a tárhely megvan, akkor a védett tartalomfolyamnak is jelen KELL lennie.
Ha ez a tároló jelen van, akkor ezen a tárolón és a védett tartalom adatfolyamon kívül minden megadott adatfolyamot és tárhelyet be KELL olvasni a védett tartalom adatfolyamból az [MS-OFFCRYPTO] szerint, és ha ezen adatfolyamok és tárolók bármelyike a védett tartalomon kívül található. Stream, figyelmen kívül KELL hagyni őket.

#### Védett tartalomfolyam ####

A Protected Content Stream egy opcionális adatfolyam, amelynek a nevének "\009DRMContent" KELL lennie, ahol a \009 a 0x0009 értékű karakter, nem pedig a "\009" karakterlánc.
Ha ez az adatfolyam jelen van, akkor az információs jogkezelési adatterület-tárolónak is jelen KELL lennie.

## Referenciák ##

* [MS-DOC fájlformálási specifikációk](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

