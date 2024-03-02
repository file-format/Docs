{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"comhad",
"síneadh",
"formáid",
"3d",
"Grúpa Khronos 3d saor in aisce,"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi chomhaid GLTF agus APInna ar féidir leo comhaid GLTF a chruthú agus a oscailt.",
  "title": "GLTF - Formáid Chomhaid Tarchuir GL",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GLTF ann?

Is formáid comhaid 3D é glTF (GL Transmission Formáid) a stórálann faisnéis mhúnla 3D i bhformáid JSON. Laghdaíonn úsáid JSON méid na sócmhainní 3D agus an phróiseáil ama rite a theastaíonn chun na sócmhainní sin a dhíphacáil agus a úsáid. Glacadh leis chun radhairc agus samhlacha 3D a tharchur agus a luchtú go héifeachtach trí fheidhmchláir. D'fhorbair Grúpa Oibre Formáidí 3D Khronos Group glTF agus cuireann a cruthaitheoirí síos air mar [JPEG](/image/jpeg/) de 3D.

Sainmhíníonn formáid comhaid GLTF formáid chomhshínte, chomhchoiteann foilsitheoireachta le haghaidh uirlisí agus seirbhísí ábhair 3D a dhéanann sreafaí oibre an údair a chuíchóiriú agus a chumasaíonn úsáid idir-inoibritheach ábhair ar fud an tionscail. Ba é an rún a bhí taobh thiar de chruthú formáid comhaid glTF ná formáid fhoilsithe shínte, choiteann a shainiú le haghaidh uirlisí agus seirbhísí ábhair 3D ar cheart dóibh sreafaí oibre údaraithe a chuíchóiriú agus úsáid comh-inoibritheach ábhair a chumasú ar fud an tionscail. Laghdaíonn sé próiseáil ama rite ag feidhmchláir a úsáideann WebGL agus APIanna eile.

## Stair Achomair ar Chomhad GLTF

The first specifications for glTF file format 1.0 were announced in October 2015. Tháinig sé seo mar shraith iarrachtaí a thosaigh Khronos i mí an Mhárta 2012. Ba é aidhm na n-iarrachtaí seo measúnú a dhéanamh ar na deiseanna a bhaineann le tarraingt WebGL. Mar thoradh air sin, cuireadh an chéad taispeántas de fhormáid glTF, bunaithe ar fhormáid JSON i láthair ag an gcruinniú WebGl in 2012. Ghlac roinnt cuideachtaí leis an bhformáid ó am go chéile lena n-áirítear Cesium, 3D Tiles, Oculus, Microsoft, Archilogic agus eile.

Foilsíodh glTF 2.0 ar 5 Meitheamh, 2017 ag Comhdháil Web3D 2017. Tá liosta fada de na cuideachtaí a ghlac formáid comhaid glTF ina dhiaidh sin.

## Formáid Comhaid GLTF

Tá na sonraíochtaí formáid comhaid le haghaidh glTF 2.0 ar fáil [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) mar thagairt agus ba cheart breathnú orthu in aon chur i bhfeidhm a bhaineann le léamh/scríbhneoireacht chun tacú le formáid comhaid glTF.

Sainmhíníonn glTF sócmhainní mar chomhaid JSON le sonraí seachtracha tacaíochta. Léiríonn sé samhlacha 3D le cabhair ó:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Comhaid dhénártha (.bin) ina bhfuil sonraí céimseata agus beochana, agus sonraí eile atá bunaithe ar mhaoláin

* Comhaid íomhá ([.jpg] (/image/jpeg/), [.png] (/image/png/)) le haghaidh uigeachtaí


Stóráiltear aon sócmhainní seachtracha ar nós íomhánna i gcomhaid sheachtracha a ndéantar tagairt dóibh trí URI. Stóráiltear na URIanna seo taobh leis an gcoimeádán GLB nó leabaítear iad go díreach isteach sa JSON ag baint úsáide as URIanna sonraí. Ní mór do gach glTF bailí a leagan a shonrú.

Tá glTF deartha chun méid comhaid bheaga, luchtú tapa, léiriú radharc 3D iomlán agus síneadh a bhaint amach. Is iad na spriocanna dearaidh uathúla seo na príomhchúiseanna leis an éileamh atá ar fhormáid comhaid glTF san fhearann 3D. Seo a leanas na cineálacha mím a thacaíonn an fhormáid comhaid glTF le haghaidh cineálacha éagsúla comhaid:

* Úsáideann comhaid .gltf samhail/gltf+json

* Úsáideann comhaid .bin feidhmchlár/sruth octet

* Úsáideann comhaid uigeachta an cineál íomhá/* oifigiúil bunaithe ar an bhformáid íomhá ar leith. Chun comhoiriúnacht le brabhsálaithe gréasáin nua-aimseartha, tacaítear leis na formáidí íomhá seo a leanas: íomhá/jpeg, íomhá/png.


### Ionchódú JSON

Forchuireann glTF srianta breise ar fhormáid comhaid JSON

Chun cur i bhfeidhm ar thaobh an chliaint a shimpliú, tá srianta breise ag glTF ar fhormáid agus ar ionchódú JSON.

1. Ní mór do JSON ionchódú UTF-8 a úsáid gan BOM.
1. Ní úsáideann gach teaghrán a shainmhínítear sa sonraíocht seo (ainmneacha maoine, ainmneacha) ach tacar carachtair ASCII agus ní mór é a scríobh mar ghnáth-théacs, m.sh., maolán in ionad `\u0062\u0075\u0066\u0066\u0065\u0072`.
1. Caithfidh ainmneacha (eochracha) laistigh d'oibiachtaí JSON a bheith uathúil, .i. ní cheadaítear eochracha dúblacha.

### URIanna

Déantar tagairt do mhaoláin agus acmhainní Íomhá trí URIanna. Caithfidh na cliaint tacaíocht a thabhairt don dá chineál URI seo a leanas.

**URIs Sonraí:** Tá na URanna Sonraí mar atá sainmhínithe ag RFC 2397 agus úsáideann glTF iad chun acmhainní a leabú sa JSON.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Tagairtí ##

* [Sonraíochtaí glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)

* [Formáid Comhaid glTF - Le Vicipéid](https://ga.wikipedia.org/wiki/GlTF)


