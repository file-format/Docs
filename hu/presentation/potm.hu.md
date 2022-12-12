{
  "date" : "2019-10-11",
  "keywords" :[ "potm fájl", "potm fájlformátum", "mi az a potm fájl", "fájl", "potm példa", "potm fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM – Microsoft PowerPoint sablonfájl makróval",
  "description":"További információ a POTM-fájlformátumról és az API-król, amelyek POTM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a POTM fájl?

A POTM kiterjesztésű fájlok olyan Microsoft PowerPoint sablonfájlok, amelyek támogatják a makrókat. A POTM-fájlok a PowerPoint 2007 vagy újabb verziójával jönnek létre, és olyan alapértelmezett beállításokat tartalmaznak, amelyek további prezentációs fájlok létrehozásához használhatók. Ezek a beállítások tartalmazhatnak stílusokat, háttereket, színpalettát, betűtípusokat és alapértelmezett beállításokat, valamint olyan makrókat, amelyek egyedi funkciókat tartalmaznak egy adott feladat elvégzéséhez. Ezeket a PowerPoint korábbi verziója is megnyithatja, amelyre telepítve van az Open XML dokumentum támogatása. A POTM-fájlok a Microsoft PowerPointban megnyithatók szerkesztés céljából, mint bármely más PowerPoint-fájl.

## Fájlformátum specifikációi ##

A POTM fájlformátum az Office OpenXML specifikációin alapul, és hasonlít a [PPTX](/hu/presentation/pptx/) fájl szerkezetére, amely egy tömörített [ZIP](/hu/compression/zip/) archívum.

A POTM-fájlon belüli diák szöveget, képeket, videókat, grafikákat és egyéb objektumokat tartalmazhat, amelyek szabadon elrendezhetők az oldalon. A POTM-sablonokat ezután több fájl létrehozására használják, amelyek öröklik a fájl összes formázási beállítását. A POTM-fájlban található makrókat ezért más prezentációk is öröklik. Beágyazásuk a dokumentum szerkezetébe az MS Office-ban található Makrórögzítőn keresztül történik, amely parancssorozatokat menthet, és makrókat hozhat létre azok automatikus replikálásához.

Az Office Open XML fájlformátummal generált fájlok XML-fájlok gyűjteménye más fájlokkal együtt, amelyek hivatkozásokat biztosítanak az összes fájl között. Ez a gyűjtemény tulajdonképpen egy tömörített archívum, amelyet ki lehet bontani a tartalom megtekintéséhez. Ehhez egyszerűen nevezze át a POTM fájlkiterjesztést zip-re, és bontsa ki a tartalmának megfigyeléséhez.

A következő szakaszok mindegyikre rávilágítanak.

### [Content_Types].xml ###

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik. A következő egy diarész tartalomtípusa:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Ha új részeket kell hozzáadni a csomaghoz, azt az új rész hozzáadásával és a .rels fájlokon belüli kapcsolatok frissítésével teheti meg. Szem előtt kell tartani, hogy egy ilyen változtatáshoz a Content_Types.xml fájlt is frissíteni kell.

### \_rels (mappa) ###

A többi részek és a csomagon kívüli erőforrások közötti kapcsolatokat a kapcsolatok rész tartja fenn. A Relationships mappa egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. A prezentációs fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja a kapcsolatot az elsődleges irodai dokumentumokkal, amelyek ppt/presentation.xml formátumban találhatók, és a docProps egyéb részeihez, mint alapvető és kiterjesztett tulajdonságokhoz.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
A dokumentum minden olyan részének, amely egy vagy több kapcsolat forrása, megvan a maga kapcsolati része, ahol minden ilyen kapcsolatrész a rész \_rels almappájában található, és a '.rels' nevéhez fűzve nevezik el őket. rész. A fő tartalmi résznek (presentation.xml) megvan a maga kapcsolati része (presentation.xml.rels). Kapcsolatokat tartalmaz a tartalom más részeihez, például a slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, valamint a külső hivatkozások URI-jéhez.

#### Explicit kapcsolat ####

Explicit kapcsolat esetén az erőforrásra az a Id attribútum használatával hivatkozunk<Relationship> elem. Ez azt jelenti, hogy a forrásban lévő Id közvetlenül egy kapcsolatelem azonosítójára képezi le, kifejezett hivatkozással a célra.

Például egy dia tartalmazhat egy ilyen hiperhivatkozást:
```
<a:hlinkClick r:id#"rId2">
```
Az r:id#"rId2" a következő kapcsolatra hivatkozik a dia kapcsolatok részében (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implicit kapcsolat ####

Egy implicit kapcsolat esetén nincs ilyen közvetlen hivatkozás a `-ra<Relationship> Id`. Ehelyett a hivatkozás érthető.

### ppt mappa ###

Ez a fő mappa, amely a Prezentáció tartalmával kapcsolatos összes részletet tartalmazza. Alapértelmezés szerint a következő mappákkal rendelkezik:

* \_rels
* téma
* diák
* slideLayouts
* slideMasters

és a következő xml fájlok:

* bemutató.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referenciák ##

* [[MS-PPTX] – PPTX fájlformátum](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

