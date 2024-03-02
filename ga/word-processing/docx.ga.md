{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"comhad",
"formáid",
"cineál comhaid",
"síneadh",
"cad is comhad DOCX ann?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Foghlaim faoi fhormáid comhaid DOCX agus APIanna ar féidir comhaid DOCX a chruthú agus a oscailt.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-gax"
}
},
  "lastmod": "2019-12-03"
}

## Cad is comhad DOCX ann? ##

Is formáid aitheanta é DOCX do dhoiciméid Microsoft Word. Arna thabhairt isteach ó 2007 le heisiúint Microsoft Office 2007, athraíodh struchtúr an fhormáid nua Doiciméid seo ó dhénárthach simplí go meascán de chomhaid XML agus dhénártha. Is féidir comhaid Docx a oscailt le Word 2007 agus le leaganacha cliathánach ach ní leis na leaganacha níos luaithe de MS Word a thacaíonn le síntí comhaid DOC.

## Stair Ghearr ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## Sonraíochtaí Formáid Chomhaid DOCX - Tuilleadh Eolais

Cuimsíonn comhad Docx bailiúchán de chomhaid XML atá laistigh de chartlann ZIP. Is féidir a bhfuil i ndoiciméad Word nua a fheiceáil ach a bhfuil ann a dhísipeáil. Tá liosta de chomhaid XML sa bhailiúchán atá catagóirithe mar:

* Comhaid Meiteashonraí - tá faisnéis faoi chomhaid eile atá ar fáil sa chartlann

* Doiciméad - tá ábhar iarbhír an doiciméid


### Comhaid Meiteashonraí ###

Úsáideann Microsoft Word na comhaid seo chun an gaol idir comhaid a aimsiú agus chun inneachar an doiciméid a aimsiú. Nuair a bhaintear cartlann de dhoiciméid Word, tá roinnt comhad den sórt sin ann mar a shonraítear thíos.

#### Gaol - \_rels/.rels ####

Tá faisnéis sa chomhad seo a insíonn do MS Word cá háit le hinneachar an doiciméid agus tagairtí eile a chuardach. Sainaithnítear gach gaol le haitheantas caidrimh uathúil agus sonraítear an comhad XML tagartha mar sprioc. Taispeántar comhad caidrimh samplach mar seo a leanas:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Cineálacha Ábhair ####

Is féidir go bhfuil roinnt cineálacha meán istigh i ndoiciméad mar íomhánna, téamaí, ealaín focal, srl. Tá faisnéis sa [Content_Types].xml faoi na cineálacha meán sin atá sa doiciméad. Taispeántar a bhfuil i gcomhad XML dá leithéid mar seo a leanas:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Tagairtí d'Acmhainní - \_rels/document.xml.rels ####

Déantar tagairt d'fhaisnéis faoi acmhainní, ar nós íomhánna atá leabaithe sa doiciméad, sa chomhad XML seo.

#### Inneachar na Príomhcháipéise ####

Tagraíonn sé seo do phríomhchomhad XML na cartlainne ina bhfuil ábhar téacs an doiciméid. Léirítear an t-ábhar seo le héagsúlacht nóid de réir sonraíochtaí OpenOffice XML. Altanna agus Táblaí den chuid is mó atá in ábhar an chomhaid seo, cé gur féidir nóid eile a bheith iontu freisin.

### Nóid Formáid Chomhaid ###

Is éard atá sa phríomhchomhad document.xml ná bailiúchán nóid chun ábhar iomlán comhaid a léiriú. Tá tús agus deireadh ag gach nód a chuimsíonn nóid bhreise nó a bhfuil ann. Seo a leanas sampla simplithe de chomhad xml den sórt sin:

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

Seo a leanas an fhaisnéis faoi chuid de na nóid atá i gcomhad DOCX chun an t-ábhar a léiriú.

`<w:document> ` - Is ionann é agus buneilimint phríomhábhar an chomhaid.

`<w:body> ` - Léiríonn sé corpas an doiciméid ar féidir a bheith comhdhéanta de go leor nóid eiliminte eile mar ailt, táblaí agus ailt.

#### Ailt ####

Is éard is alt ann príomhshealbhóir an ábhair laistigh de dhoiciméad. Léirítear é ag **<w:p> ** eilimint laistigh de dhoiciméad. Is éard atá i mír eile ná ritheann amháin nó níos mó **<w:r> ** ina bhfuil téacs iarbhír na míre. Chomh maith le rití, féadfaidh míreanna doiciméid eile a bheith i míreanna cosúil le hipearnaisc, tuairimí, etc. Tá struchtúr alt mar shampla mar a thaispeántar thíos:

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

## DOCX CCanna

 * **An Síneadh Comhad é DOCX?** - úsáidtear DOCX mar shíneadh comhaid chun Microsoft Word 2007 a léiriú agus formáidí comhaid níos déanaí a úsáidtear chun comhaid Word a stóráil. Insíonn sé do OS freisin go n-éilíonn an comhad DOCX seo Microsoft Word 2007 chun é a oscailt agus a dheilbhín a thaispeáint.
 * **An ionann DOCX agus Word** - Is formáid comhaid é DOCX a úsáideann Microsoft Word chun doiciméid a shábháil i bhformáid Open XML. Ar an láimh eile, is bogearraí feidhmchláir é Word ó Microsoft Office a thacaíonn le formáidí comhaid eile cosúil le DOC, DOT, DOTM, agus cinn eile.
 * **Cad é an difríocht DOC agus DOCX** - is é DOC ná comhad focal a shábháiltear i Word 2007 agus formáid comhaid níos luaithe. Tá DOCX bunaithe ar fhormáid comhaid Open XML le tacaíocht ó Microsoft 2007 agus leaganacha níos déanaí. Seiceáil [Difríochtaí idir DOC agus DOCX](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) le haghaidh tuilleadh sonraí.

## Tagairtí ##

* [MS - Formáid Comhaid DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


