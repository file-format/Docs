{
  "date": "2020-03-16",
  "keywords": [
"Comhad STL",
"Formáid",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid STL agus APInna ar féidir leo comhaid STL a chruthú agus a oscailt.",
  "title": "Formáid Comhaid STL",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad é an comhad STL?

Is formáid comhaid idirmhalartaithe é STL, giorrúchán le haghaidh stereolithrography, a léiríonn céimseata dromchla 3thoiseach. Aimsítear an fhormáid comhaid i réimsí éagsúla cosúil le fréamhshamhail tapa, priontáil 3D agus déantúsaíocht ríomhchuidithe. Léiríonn sé dromchla mar shraith de thriantáin bheaga, ar a dtugtar aghaidheanna, ina gcuirtear síos ar gach gné de réir treo ingearach agus trí phointe a sheasann do rinn an triantáin. Úsáideann feidhmchláir sonraí na dtorthaí chun an trasghearradh den chruth 3D a bheidh le tógáil ag an bhfabber a chinneadh. Níl aon fhaisnéis ar fáil i bhformáid comhaid STL chun dath, uigeacht nó tréithe coitianta samhlacha [CAD](/cad/) a léiriú.

## Stair Ghearr ##

The development of STL file format dates back to 1987. D'fhorbair 3D Systems é le húsáid i gclódóirí 3D tráchtála. Moladh leagan athbhreithnithe d’fhormáid comhaid STL, ar a dtugtar STL 2.0, in 2009 agus nuashonraíodh an fhormáid comhaid.

## Sonraíochtaí Formáid Chomhaid ##

Seasann comhad STL do chéimseata dromchla agus úsáid á baint as gnéithe. Sainmhíníonn na gnéithe dromchla ruda 3D agus sainaithnítear é go huathúil le gnáthaonad, atá ingearach leis an triantán le fad 1.0, agus trí rinn. Tá iomlán de 12 uimhir stóráilte do gach gné mar Ghnáth agus sonraítear gach rinn ag trí chomhordanáid an ceann. Níl aon fhaisnéis scála sa chomhad StL; is aonaid threallacha na comhordanáidí.

Is féidir sonraíochtaí formáid comhaid STL a scrúdú ó dhá ghné a leanúint.

### Treoshuíomh Facets ###

Cinntear treoshuíomh gné de réir ghnáththreo an aonaid agus an t-ord ina liostaítear na rinn. Sonraítear treoshuíomh na ngnéithe ar dhá bhealach mar seo a leanas:

* Tá treo an ghnáthbhealaigh amach

* Tá na rinn liostaithe in ord tuathalach ón taobh amuigh, ag cloí le riail na láimhe deise.


### Riail Vertex go Vertex ###

De réir na rialach seo, roinneann gach triantán dhá rinn le gach ceann dá thriantáin chóngaracha. Mar sin, ní féidir le rinn triantáin amháin luí ar thaobh triantáin eile.

## Formáidí Comhaid ##

Tá STL ar fáil in ASCII chomh maith le huiríll Dénártha le haghaidh formáid chomhaid dhlúth.

### Formáid STL ASCII ###

Tá leagan ASCII de fhormáid comhaid STL scríofa i simplí ASCII. Mar gheall ar a méid mór, áfach, ní roghnaítear an fhormáid comhaid mar fhormáid is fearr le húsáid. Seo a leanas comhréir chomhaid STL ASCII:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. D’fhéadfadh príomhchomhartha lúide a bheith ag comhordanáid **gnáthghné**; ní fhéadfaidh comhordanáid ** rinn**.

### Formáid Dénártha STL ###

Úsáideann an fhormáid dhénártha an tslánuimhir IEEE agus léiriú uimhriúil snámhphointe. Léirítear formáid an chomhaid mar seo a leanas:

| Réimse | Eolas |
---|---|
|Ceanntásc|80 carachtar|
|Líon Triantán|Slánuimhir endian beag 4-bheart gan síniú |
|Sonraí le haghaidh gach triantáin |12 uimhreacha snámhphointe 32-giotán |

Tá léargas níos mionsonraithe ar fhormáid an chomhaid mar a thaispeántar thíos.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Tagairtí ##

* [An Formáid STL](http://www.fabbers.com/tech/STL_Format)

* [STL - le Vicipéid]( https://ga.wikipedia.org/wiki/STL_(file_format))


