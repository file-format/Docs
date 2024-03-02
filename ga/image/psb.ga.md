{
  "date": "2019-10-11",
  "keywords": [
"comhad psb",
"Formáid comhaid psb",
"Cad is comhad psb ann",
"comhad",
"sampla psb",
"Síneadh comhad psb",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB - Photoshop Formáid Comhaid Íomhá Mhór",
  "description": "Foghlaim faoi fhormáid comhaid PSB agus APInna ar féidir leo comhaid PSB a chruthú agus a oscailt.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-gab"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PSB ann?
Sábhálann Adobe photoshop comhaid i dhá fhormáid. Déantar comhaid a bhfuil 30,000 faoi 30,000 picteilín acu a shábháil le síneadh PSD agus déantar comhaid atá níos mó ná PSD suas le 300,000 faoi 300,000 picteilín a shábháil le síneadh PSB ar a dtugtar Photoshop Big”. Go sonrach, is féidir le comhaid PSB a bheith chomh mór le 4 EB (os cionn 4.2 billiún GB) le híomhánna a bhfuil airde agus leithead suas le 300,000 picteilín acu. Is féidir le PSDanna, ar an láimh eile, a bheith ag uasmhéid suas le 2 GB agus toisí íomhá de 30,000 picteilín.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Eolas Formáide Comhaid ##

Roinntear formáid comhaid Photoshop i gcúig mhórchuid le go leor marcóirí faid le bogadh idir rannóga.

| Formáid comhaid
---|
| Ceanntásc an Chomhaid
|Sonraí Mód Datha
| Acmhainní Íomhá
|Eolas Ciseal agus Masc
|(((
Sonraí Íomhá
)))

### Ceanntásc an Chomhaid ###

Tá fad seasta de 26 beart ag ceanntásc an chomhaid agus tá bun-airíonna na híomhá ann.

Síniú BYTE [4] – Comhionann le '8BPS'.

Leagan WORD [2] – Uimhir an Leagan, PSD # 1, PSB #2.

BYTE Forchoimeádta [6] – Curtha in áirithe agus nialas i gcónaí.

Cainéil WORD [2] – Líon na gcainéal datha san íomhá lena n-áirítear cainéil alfa. Tá a luach idir 1 agus 56.

Sraitheanna fada [4] – Airde na híomhá i bpicteil, PSD 1-30,000, PSB 1-300,000.

Colúin Fada [4] – Leithead na híomhá i bpicteilíní, PSD 1-30,000, PSB 1-300,000.

WORD Doimhneacht [2] – Líon na ngiotán in aghaidh an chainéil. Is iad na luachanna tacaithe ná 1,8,16 agus 32.

Mód WORD [2] – Mód Datha an chomhaid.

#### Cur síos ar an Mód ####


|Mód|Cur Síos
---|---|
|0|Giotán (monacróim)
|1|Scála liath
|2|Innéacsaithe
|3|RGB
|4|CMYK
|7|Ilchainéil
|8|Déatón (leathghón)
|9|Saotharlann

### Sonraí Mód Datha ###

Tar éis rannóg ceanntásca an chomhaid seo a leanas an t-alt sonraí mód datha. Tosaíonn an bloc le hUimhir LONG a thugann fad an bhloic i mbearta. Seo a leanas struchtúr na sonraí mód datha:

4 beart – Fad na sonraí datha seo a leanas.

Athróg – Sonraí Datha

Mura bhfuil an luach réimse mód sa chuid ceanntásc Dath Innéacsaithe nó duotone, beidh fad an bhloc 0 agus ní bheidh aon sonraí tar éis réimse fad.

I gcás Íomhánna Datha Innéacsaithe, beidh an fad 768 beart ina mbeidh pailéad dathanna 256. Maidir le duotone, beidh paraiméadair scáileáin agus faisnéis ghaolmhar eile sna sonraí.

### Acmhainní Íomhá ###

Tar éis an t-alt sonraí mód datha, is é an tríú bloc an t-alt acmhainní íomhá. Is uimhir fhada iad na chéad cheithre bheart a shonraíonn fad an bhloic agus sraith de bhloic acmhainne ina dhiaidh sin. Seo a leanas struchtúr an bhloc acmhainne íomhá:

Cineál BYTE [4] – Síniú '8BIM

ID WORD [2] – Aitheantas Acmhainní Íomhá. Tá liosta de na hAitheantais Acmhainní atá le feiceáil ón nasc tagartha.

Ainm BYTE [Athraitheach] – Ainm: Teaghrán Pascal le comhfhad. ** **

Méid FAD [4] – Méid Iarbhír na sonraí acmhainne a leanas.

Sonraí BYTE [Athróg} – Sonraí acmhainne. Tá sé padded a dhéanamh ar an méid cothrom.

Mínítear cuid de na formáidí acmhainne go hachomair thíos:

**Formáid Acmhainne Eangaí agus Treoraithe:** Stóráiltear faisnéis Eangaí agus Treoraithe sa bhloc acmhainní. Tá 16 ghreille beart agus ceanntásc treorach sna bloic acmhainne seo agus 5 bhloic bheart treorach ina dhiaidh sin.

**Formáid Acmhainne Mionsamhla:** Stóráiltear faisnéis mionsamhlacha i mbloc acmhainní íomhá le haghaidh taispeáint réamhamhairc ina bhfuil ceanntásc beart 28 agus mionsamhail JFIF in RGB.

**Samplálaithe datha Formáid Acmhainne:** Stóráiltear faisnéis maidir le samplóirí datha i mbloc acmhainní íomhá le ceanntásc 8 beart agus bloc faid athraitheach d’eolas samplálaithe datha ina dhiaidh sin.

### Eolas Ciseal agus Masc ###

Is bloc faisnéise ciseal agus masc é an bloc amach agus tá faisnéis ann faoi na sraitheanna agus na maisc. Stóráiltear faisnéis sraithe ar dtús agus ansin maisítear faisnéis.

**Eolas Sraithe:** Tosaíonn faisnéis sraithe le luach LONG a thaispeánann fad na faisnéise ciseal. Ina dhiaidh sin tá comhaireamh luach WORD a thaispeánann líon na dtaifead cisealta atá le leanúint.

[8] – fad na sraitheanna

[2] – Líon na Sraitheanna

[Athraitheach] – Eolas faoi gach ciseal.

[Athraitheach] – Sonraí íomhá an chainéil.** **

**Eolas Masc:** Tá an fhormáid seo a leanas ag struchtúr masc:


|Struchtúr Sonraí|Ainm Réimse| Cur síos
---|---|---|
|WORD| Spás Datha Forleagan| (Gan doiciméadaithe)
|BYTE[8]| Comhpháirteanna Dath | Comhpháirteanna datha beart 4x2
|WORD| Teimhneacht| 0#trédhearcach, 1#teimhneach
|BYTE| cineál| 0#inbhéartaithe, 1#cosanta, 128#úsáid luach stóráilte
|BYTE| stuáil| socraithe go nialas

### Sonraí Íomhá ###

Tá na sonraí picteilín íomhá sa chuid dheireanach. Stóráiltear na sonraí íomhá mar shraith seicheamh i bplánaí .i. na sonraí dearga go léir ar dtús, ansin na sonraí glasa go léir srl. Taispeánann WORD ag tús gach líne an méid i mbearta a bhaineann le gach líne scanadh.

[2] – Modh comhbhrúite:

[Athraitheach] – Sonraí Íomhá in ord pleanach ie RRRR, GGGG, BBBB etc.

Modhanna Comhbhrúite:

0 – Raw Sonraí Íomhá

1 – RLE Comhbhrúite

2 - Zip gan Tuar

3 - Zip le tuar

## Tagairt ##

* [Formáid Chomhaid PSB - Le Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB - Vicipéid](https://ga.wikipedia.org/wiki/Adobe_Photoshop#File_format)


