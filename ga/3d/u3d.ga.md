{
  "date": "2019-10-11",
  "keywords": [
"Comhad u3d",
"Formáid comhaid u3d saor in aisce,",
"Cad is comhad u3d ann",
"comhad",
"sampla u3d",
"Síneadh comhad u3d saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D - Formáid Comhaid Uilíoch 3D",
  "description": "Foghlaim faoi fhormáid comhaid U3D agus APIanna ar féidir leo comhaid U3D a oscailt agus a chruthú.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-gad"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad U3D ann?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. Tacaíonn doiciméid 3D [PDF](/pdf/) le neadú réad U3D agus is féidir iad a fheiceáil in Adobe Reader (leagan 7 agus ar aghaidh).

Forbraíodh formáid U3D agus aird á tabhairt ar an aidhm caighdeán uilíoch a bhunú maidir le stóráil agus malartú sonraí tríthoiseach. Mar sin féin, aimsíonn an fhormáid a príomhúsáid in ionchódú do PDF 3D seachas í a úsáid mar fhormáid idirmhalartaithe. Tiontaíonn Acrobat 3D cineál comhaid 3D le tacaíocht go U3D nó PRC ar é a thiontú go PDF.

## Formáid Comhaid U3D

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

Bhí an chéad eagrán de U3D dírithe ar na príomhléirithe d’airíonna grafaicí 3D amhail céimseata, dath, uigeachtaí, soilsiú, cnámha agus beochan bunaithe ar chlaochlú. Ceartaíodh roinnt earráidí sa chéad eagrán sa dara agus sa tríú eagrán, agus ba é an tríú leagan an cineál is coitianta a úsáidtear i mbogearraí tionscail. Soláthraíonn an ceathrú eagrán sainmhínithe ar phrimitives ard-ord (dromchlaí cuartha). Tá [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ar fáil ar líne le haghaidh tagartha úsáideora ar shuíomh Gréasáin ECMA.

### Cineálacha Sonraí i gcomhaid U3D

Beidh na cineálacha seo a leanas sa chomhad dénártha: U8, U16, U32, U64, I16, I32, F32, F64, agus Teaghrán.

 * U8 : Slánuimhir 8 giotán gan síniú
 * U16 : Slánuimhir 16 giotán gan síniú
 * U32 : Slánuimhir 32 giotán gan síniú
 * U64 : Slánuimhir 64 giotán gan síniú
 * I16 : Slánuimhir sínithe 16 giotán
 * F32: Snámhphointe beachtais aonair IEEE.
 * F64: Snámhphointe cruinneas dúbailte IEEE.
 * Teaghrán: Tosaíonn teaghráin i gcomhad U3D le slánuimhir 16-giotán gan síniú a shainíonn fad iomlán na gcarachtar sa teaghrán. Déantar teaghráin a phróiseáil i gcónaí mar chás-íogair.

## Struchtúr Comhad U3D

Tá seicheamh bloic i gcomhad U3D. Tá 3 chineál éagsúla bloc i ngach comhad U3D.

 * Bloc Ceanntásca Comhad
 * Bloc Dearbhaithe
 * Bloc Leanúint

Cinneann an lódóir deireadh bloc mura bhfuil na sonraí sa bhloc sin ag teastáil nó mura bhfuil díchódóir don chineál bloc sin ar fáil.

{{< figure src="../u3d.png" alt="Formáid Comhaid U3D" >}}

### Bloc Ceanntásca Comhad
Tá faisnéis chomhaid i mbloc ceanntásc comhaid a úsáideann an lucht lódáilte chun a chinneadh conas an comhad a léamh.

### Bloc Dearbhaithe

Tá faisnéis sna bloic dearbhaithe faoi na rudaí sa chomhad. Ní mór na rudaí i mbloc dearbhaithe a shainiú.

### Bloc Leanúint

Soláthraítear faisnéis bhreise sa bhloc leantach maidir le rudaí a dhearbhaítear i mbloc Dearbhaithe. Caithfidh gach Bloc Leanúnach a bheith comhcheangailte le Bloc Dearbhaithe.


## Tagairtí ##

* [Formáid Chomhaid U3D - Vicipéid](https://ga.wikipedia.org/wiki/Universal_3D)

* [Sonraíochtaí Formáid Comhaid ECMA U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


