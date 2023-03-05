{
  "date" : "2019-10-11",
  "keywords" :[ "ppsm fájl", "ppsm fájlformátum", "mi az a ppsm fájl", "fájl", "ppsm példa", "ppsm fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM – makró-engedélyezett PowerPoint-bemutató fájl",
  "description":"További információ a PPSM fájlformátumról és az API-król, amelyek PPSM fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PPSM fájl?

A PPSM kiterjesztésű fájlok a Microsoft PowerPoint 2007 vagy újabb verziójával létrehozott makróképes diavetítés-fájlformátumot képviselik. Egy másik hasonló fájlformátum a [PPTM](/hu/presentation/pptm/), amely abban különbözik, hogy a Microsoft PowerPoint segítségével szerkeszthető formátumban nyílik meg, nem pedig diavetítésként. Diavetítésként futtatva a PPSM-fájl a bemutató diákjait sértetlen tartalommal jeleníti meg a diavetítésben, és alapértelmezés szerint csak olvasható módban van. A PPSM-fájlok továbbra is szerkeszthetők a Microsoft PowerPointban, ha megnyitják a PowerPointban.

## Fájlformátum ##

A PPSM fájlformátumot a PowerPoint 2007-ben vezették be, és az OpenXML fájlformátumon alapul, amely az XML és a [ZIP](/hu/compression/zip/) kombinációját használja a tartalom tárolására. Az Office Open XML fájlformátummal generált fájlok XML fájlok gyűjteménye más fájlokkal együtt, amelyek hivatkozásokat biztosítanak az összes fájl között. Ez a gyűjtemény tulajdonképpen egy tömörített archívum, amelyből ki lehet bontani a tartalmat. Ehhez egyszerűen nevezze át a PPSM fájlkiterjesztést zip-re, és bontsa ki a tartalmának megfigyeléséhez.

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

Explicit kapcsolat esetén az erőforrásra az a Id attribútum használatával hivatkozunk<Relationship> elem. Ez azt jelenti, hogy a forrásban lévő Id közvetlenül egy kapcsolatelem azonosítójára van leképezve, kifejezett hivatkozással a célra.

Például egy dia tartalmazhat egy ilyen hiperhivatkozást:
```
<a:hlinkClick r:id#"rId2">
```
Az r:id#"rId2" a következő kapcsolatra hivatkozik a dia kapcsolatok részén belül (slide1.xml.rels).
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

* [OpenXML prezentációs fájlformátum](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

