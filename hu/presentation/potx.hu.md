{
  "date" : "2019-10-11",
  "keywords" :[ "potx fájl", "potx fájlformátum", "mi az a potx fájl", "fájl", "potx példa", "potx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX – Microsoft PowerPoint bemutatósablon",
  "description":"További információ a POTX fájlformátumról és az API-król, amelyek POTX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a POTX fájl?

A .POTX kiterjesztésű fájlok a Microsoft PowerPoint 2007 vagy újabb verziójával létrehozott Microsoft PowerPoint sablonprezentációkat képviselik. Ezt a formátumot a [POT](/hu/presentation/pot/) fájlformátum helyettesítésére hozták létre, amely a bináris fájlformátumon alapul, és amelyet a PowerPoint 97-2003 támogat. Az előállított fájlok felhasználhatók olyan prezentációk létrehozására, amelyek azonos elrendezésűek, és más beállításokat is alkalmazni kell az új fájlokra. Ezek a beállítások tartalmazhatnak stílusokat, háttereket, színpalettát, betűtípusokat és alapértelmezett értékeket. Az ilyen fájlok a hivatalos használatra kész sablonfájlok létrehozása érdekében jönnek létre.

## Rövid története ##

2000 elején a Microsoft a változtatás mellett döntött, hogy megfeleljen az **Office Open XML** szabványnak. Az új szabvány szerinti különböző típusú dokumentumokat úgy azonosították, hogy "X"-et fűztek a kiterjesztéseikhez, ahol az "X" az XML-t jelenti. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül. Az új fájltípus további előnyökkel jár a kis fájlméret, a kisebb sérülések és a jól formázott képek megjelenítése miatt.

## Fájlformátum specifikációi ##

Az Office Open XML fájlformátummal generált fájlok XML fájlok gyűjteménye más fájlokkal együtt, amelyek hivatkozásokat biztosítanak az összes fájl között. Ez a gyűjtemény tulajdonképpen egy tömörített archívum, amelyből ki lehet bontani a tartalmat. Ehhez egyszerűen nevezze át a POTX fájlkiterjesztést zip-re, és bontsa ki a tartalmának megfigyeléséhez.

A következő szakaszok mindegyikre rávilágítanak.

### [Content_Types].xml ###

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik. A következő egy diarész tartalomtípusa:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Ha új részeket kell hozzáadni a csomaghoz, azt az új rész hozzáadásával és a .rels fájlokon belüli kapcsolatok frissítésével teheti meg. Szem előtt kell tartani, hogy egy ilyen változtatáshoz a Content_Types.xml fájlt is frissíteni kell.

### \_rels (mappa) ###

A többi részek és a csomagon kívüli erőforrások közötti kapcsolatokat a kapcsolatok rész tartja fenn. A Relationships mappa egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. A PPTX fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja a kapcsolatot az elsődleges irodai dokumentumokkal, amelyek ppt/presentation.xml formátumban találhatók, és a docProps egyéb részeihez, mint alapvető és kiterjesztett tulajdonságokhoz.
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

Egy implicit kapcsolat esetében nincs ilyen közvetlen hivatkozás a `-ra<Relationship> Id`. Ehelyett a hivatkozás érthető.

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

