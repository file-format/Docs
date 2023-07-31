{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "fájl", "formátum", "fájl típusa", "kiterjesztés", "mi az a DOCX fájl?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"További információ a DOCX fájlformátumról és az API-król, amelyek DOCX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Mi az a DOCX fájl? ##

A DOCX a Microsoft Word dokumentumok jól ismert formátuma. A 2007-től, a Microsoft Office 2007 kiadásával bevezetett új dokumentumformátum szerkezete egyszerű binárisról XML és bináris fájlok kombinációjára módosult. A Docx fájlok megnyithatók a Word 2007 és oldalsó verzióival, de nem az MS Word korábbi verzióival, amelyek támogatják a DOC fájlkiterjesztéseket.

## Rövid története ##

Miután a Microsoft megnyitotta a DOC fájlformátum specifikációit, versenytársai könnyen visszafordíthatták a formátumot, és ugyanazt a támogatást biztosították saját alkalmazásaikban. Ezenkívül az Open Office versenye az Open Document Format formájában nyitottabb és szélesebb szabványok elfogadására kényszerítette a Microsoftot. 2000 elején a Microsoft úgy döntött, hogy a **Office Open XML** szabványhoz igazodó változtatás mellett döntött. Az új szabvány szerinti dokumentumok [.docx kiterjesztést](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), az "X"-et kapták. lévén XML-hez. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül. Az új fájltípus további előnyökkel jár: kis fájlméret, kevesebb sérülési változás és jól formázott képmegjelenítés.

## DOCX fájlformátum specifikációi – További információ

A Docx-fájl XML-fájlok gyűjteményéből áll, amelyek egy ZIP-archívumban találhatók. Egy új Word-dokumentum tartalma a tartalmának kicsomagolásával tekinthető meg. A gyűjtemény XML-fájlok listáját tartalmazza, amelyek a következő kategóriákba sorolhatók:

* MetaData Files – információkat tartalmaz az archívumban elérhető egyéb fájlokról
* Dokumentum – a dokumentum tényleges tartalmát tartalmazza

### Metaadat fájlok ###

A Microsoft Word ezeket a fájlokat használja a fájlok közötti kapcsolat és a dokumentum tartalmának megkeresésére. A Word-dokumentumarchívum kibontásakor számos ilyen fájlt tartalmaz az alábbiak szerint.

#### Kapcsolatok - \_rels/.rels ####

Ez a fájl olyan információkat tartalmaz, amelyek megmondják az MS Word számára, hogy hol keresse a dokumentum tartalmát és egyéb hivatkozásokat. Minden kapcsolatot egyedi kapcsolatazonosító azonosít, és a hivatkozott XML-fájlt határozza meg célként. A kapcsolati fájl minta a következőképpen jelenik meg:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Tartalomtípusok ####

Egy dokumentum többféle médiatípust tartalmazhat, például képeket, témákat, szöveges rajzokat stb. A [Content_Types].xml a dokumentumban található ilyen médiatípusokról tartalmaz információkat. Egy ilyen XML-fájl tartalma a következőképpen jelenik meg:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Hivatkozások a forrásokra - \_rels/document.xml.rels ####

Ebben az XML-fájlban hivatkoznak az erőforrásokra vonatkozó információk, például a dokumentumba ágyazott képek.

#### A fő dokumentum tartalma ####

Ez az archívum fő XML-fájljára vonatkozik, amely a dokumentum szöveges tartalmát tartalmazza. Ezt a tartalmat számos csomópont képviseli az OpenOffice XML specifikációi szerint. Ennek a fájlnak a tartalma többnyire bekezdésekből és táblázatokból áll, de ezek lehetnek más csomópontok is.

### Fájlformátum csomópontjai ###

A fő document.xml fájl csomópontok gyűjteménye a fájl teljes tartalmának megjelenítésére. Minden csomópontnak van egy eleje és vége, amelyek vagy további csomópontokat vagy a tartalmat foglalják magukba. Egy ilyen xml-fájl egyszerűsített példája a következő:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Az alábbiakban a DOCX-fájlban található néhány csomópontra vonatkozó információk találhatók a tartalom megjelenítéséhez.

`<w:document> ` - A fájl fő tartalmának gyökérelemét jelöli.

`<w:body> ` - A dokumentum törzsét jelöli, amely számos egyéb elemcsomópontot, például bekezdéseket, táblázatokat és szakaszokat tartalmazhat.

#### Bekezdések ####

A bekezdés a dokumentum fő tartalomhordozója. Ezt ** képviseli<w:p> ** elem egy dokumentumon belül. Egy bekezdés további egy vagy több futásból áll **<w:r> **, amely a bekezdés tényleges szövegét tartalmazza. A futtatásokon kívül a bekezdések más dokumentumelemeket is tartalmazhatnak, például hiperhivatkozásokat, megjegyzéseket stb. Egy példa bekezdésszerkezetre az alábbiakban látható:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Hivatkozások ##

* [MS – DOCX fájlformátum](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

