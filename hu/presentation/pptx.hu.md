{
  "date" : "2019-12-13",
  "keywords" :[ "pptx fájl", "pptx fájlformátum", "mi az a pptx fájl", "fájl", "pptx példa", "pptx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a PPTX fájlformátumról és az API-król, amelyek PPTX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PPTX - PowerPoint prezentációs fájlformátum",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PPTX fájl?

A PPTX kiterjesztésű fájlok a népszerű Microsoft PowerPoint alkalmazással létrehozott prezentációs fájlok. A PPT prezentációs fájlformátum korábbi verziójától eltérően, amely bináris volt, a PPTX formátum a Microsoft PowerPoint nyílt XML prezentációs fájlformátumán alapul. A prezentációs fájl olyan diák gyűjteménye, amelyben minden diák szöveget, képeket, formázást, animációt és egyéb médiát tartalmazhat. Ezeket a diákat egyéni prezentációs beállításokkal rendelkező diavetítések formájában mutatják be a közönségnek.

## Rövid története

A PPTX fájlformátumot 2007-ben vezették be, és a Microsoft által 2000-ben adaptált Open XML szabványt használja. A PPTX előtt az általánosan használt fájlformátum a PPT volt, amely tiszta bináris fájlformátum volt. Az új fájltípus további előnyökkel jár a kis fájlméret, a kisebb sérülések és a jól formázott képek megjelenítése miatt. 2000 elején a Microsoft a változtatás mellett döntött, hogy megfeleljen az **Office Open XML** szabványnak. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül.

## PPTX fájlformátum specifikációi

Az Office Open XML fájlformátummal generált fájlok XML fájlok gyűjteménye más fájlokkal együtt, amelyek hivatkozásokat biztosítanak az összes fájl között. Ez a gyűjtemény tulajdonképpen egy tömörített archívum, amelyet ki lehet bontani a tartalom megtekintéséhez. Ehhez egyszerűen nevezze át a PPTX fájlkiterjesztést zip-re, és bontsa ki a tartalmának megfigyeléséhez (lásd a [PPTX fájlformátum specifikációit](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/). efd8bb2d-d888-4e2e-af25-cad476730c9f) a Microsoft).

A következő szakaszok mindegyikre rávilágítanak.

### [Content_Types].xml

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik. A következő egy diarész tartalomtípusa:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Ha új részeket kell hozzáadni a csomaghoz, azt az új rész hozzáadásával és a .rels fájlokon belüli kapcsolatok frissítésével teheti meg. Szem előtt kell tartani, hogy egy ilyen változtatáshoz a Content_Types.xml fájlt is frissíteni kell.

### \_rels (mappa) ###

A többi részek és a csomagon kívüli erőforrások közötti kapcsolatokat a kapcsolatok rész tartja fenn. A Relationships mappa egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. A PPTX fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja a kapcsolatot az elsődleges irodai dokumentumokkal, amelyek ppt/presentation.xml formátumban találhatók, és a docProps egyéb részeihez, mint alapvető és kiterjesztett tulajdonságokhoz.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

A dokumentum minden olyan részének, amely egy vagy több kapcsolat forrása, megvan a maga kapcsolati része, ahol minden ilyen kapcsolatrész a rész \_rels almappájában található, és a '.rels' nevéhez fűzve nevezik el őket. rész. A fő tartalmi résznek (presentation.xml) megvan a maga kapcsolati része (presentation.xml.rels). Kapcsolatokat tartalmaz a tartalom más részeihez, például a slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, valamint a külső hivatkozások URI-jéhez.

#### Explicit kapcsolat ####

Explicit kapcsolat esetén az erőforrásra az a Id attribútum használatával hivatkozunk<Relationship> elem. Ez azt jelenti, hogy a forrásban lévő Id közvetlenül egy kapcsolatelem azonosítójára van leképezve, kifejezett hivatkozással a célra.

Például egy dia tartalmazhat egy ilyen hiperhivatkozást:

```
<a:hlinkClick r:id#"rId2">
```

Az r:id#"rId2" a következő kapcsolatra hivatkozik a dia kapcsolatok részében (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
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

* [[MS-PPTX] – PPTX fájlformátum](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

