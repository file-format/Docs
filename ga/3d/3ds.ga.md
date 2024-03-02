{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"comhad",
"formáid",
"cineál comhaid",
"síneadh",
"Cad is comhad 3DS ann?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid 3DS agus APIs is féidir comhaid 3DS a oscailt agus a chruthú.",
  "title": "Formáid Comhaid 3DS",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds"
}
},
  "lastmod": "2019-09-10"
}

## Cad é comhad 3DS?

Léiríonn comhad le síneadh .3ds formáid comhaid mogalra 3D Sudio (DOS) a úsáideann Autodesk 3D Studio. Tá Autodesk 3D Studio ar an margadh formáid comhaid 3D ó na 1990idí agus tá sé tagtha chun cinn anois go 3D Studio MAX chun oibriú le samhaltú, beochan agus rindreáil 3D. Tá sonraí i gcomhad 3DS chun radhairc agus íomhánna a léiriú i 3D agus tá sé ar cheann de na formáidí comhaid coitianta le haghaidh allmhairiú agus onnmhairiú sonraí 3D. Breithníonn sé faisnéis ar nós láithreacha ceamara, sonraí mogaill, faisnéis soilsithe, cumraíochtaí amharcphoirt, sonraí grúpa smúdála, tagairtí giotánmap agus tréithe chun rinn agus polagáin a chruthú chun radharc a dhéanamh.

## Formáid Chomhaid 3DS - Tuilleadh Eolais
Ag a bhonn, is formáid dhénártha comhaid é 3DS agus leanann sé struchtúr réamhshainithe chun sonraí a stóráil agus a aisghabháil. Cuireann an fhormáid comhaid dhénártha ar chumas an fhormáid comhaid 3DS níos tapúla i gcomparáid le formáidí comhaid téacs-bhunaithe. Stóráiltear sonraí taobh istigh de chomhad 3DS i bhfoirm smután.

### 3DS Chunk

Is bloc sonraí é gach smután i gcomhad 3DS ina bhfuil ID, fad an bhloic le haghaidh suíomh an chéad bhloc eile agus na sonraí féin. Ligeann an ID smután do léitheoirí formáid comhaid 3DS na bloic nach n-aithníonn siad a scipeáil. Cuidíonn sé freisin i extensibility an fhormáid. Stórálann gach smután faisnéis a bhaineann le cruthanna, soilsiú agus faisnéis féachana a thugann an radharc le chéile. Socraítear smután i struchtúr ordlathach i gcomhad 3DS agus tá siad cosúil le crann Oibiachta Doiciméid XML mar léiriú.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-gat.

**Fad an smután:** Tá slánuimhir 4 beart (i endian beag) a sheasann do fhad an smuga ina dhiaidh sin ar an Chunk ID. Áiríonn an fad seo freisin fad na sonraí, fad a fho-bhloic agus an ceanntásc 6-bheart.

**Pá-ualach:** Tar éis fad an smutáin tá bearta iarbhír sonraí don smután, agus a fho-phíosaí ina dhiaidh sin sa struchtúr ordlathach céanna ar féidir iad a leathnú go leibhéil éagsúla domhain.

### Struchtúr cuinne

Tá struchtúr ordlathach smután simplí mar a thaispeántar thíos:

**Blua**

|tús|deireadh|méid|ainm
--- | --- | --- | ---
|0|1|2|Aitheantas Snámh
|2|5|4|Cuta Eile

Tá ordlathas forchurtha ag smuillí orthu a shainaithnítear lena ID. I gcomhad 3ds tá an Príomh-ID smután 4D4Dh. Is é seo an chéad smután den chomhad i gcónaí. Sa smután bunscoile atá na smután is mó.

**Príomhshlua**

|id|Cur Síos
--- | ---
|3D3D|Tosaigh sonraí mogaill oibiachta.
|B000|Tosaigh sonraí an fhráma eochrach.

Díríonn an pointeoir Next Chunk tar éis an bhloc aitheantais go dtí an chéad smután eile.
Go díreach i ndiaidh Príomhshlua tá smután eile. D’fhéadfadh sé seo a bheith ina aon chineál smután eile a bheadh ceadaithe laistigh dá raon feidhme príomhstocaí.
For the Mesh description (3D3D) they could be any multiples of.

**Fo-chodanna de 3D3D - Bloc Mogall**


|id|Cur Síos
--- | ---
|1100|anaithnid
|1200|Dath Cúlra.
|1201|anaithnid
|1300|anaithnid
|1400|anaithnid
|1420|anaithnid
|1450|anaithnid
|1500|anaithnid
|2100|Bloc Dathanna Comhthimpeallach
|2200|ceo?
|2201|ceo?
|2210|ceo?
|2300|anaithnid
|3000|anaithnid
|4000|Bloc Cuspóir
|7001|anaithnid
|AFFF|anaithnid

**Fo-phíosaí de 4000 - Bloc Cur Síos ar an Réada**
Teaghrán ASCIIZ d'ainm an oibiachta is ea an chéad mhír de Subchunk 4000.
Cuimhnigh gur féidir le réad a bheith ina mhogalra, ina sholas nó ina cheamara.

|id|Cur Síos
--- | ---
|4010|anaithnid
|4012|scáth?
|4100|Réad Polagán Triantánach
|4600|Solas
|4700|Ceamara

## Tagairtí

* [Formáidí Comhaid Céimseata - Autodesk]( https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS - Le Vicipéid]( https://ga.wikipedia.org/wiki/.3ds)


