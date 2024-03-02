{
  "date": "2019-12-09",
  "keywords": [
"Comhad 3mf",
"Formáid comhaid 3mf saor in aisce,",
"Cad is comhad 3mf ann",
"comhad",
"3mf sampla",
"Síneadh comhad 3mf íoslódáil",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "Foghlaim faoi fhormáid comhaid 3MF agus APIs ar féidir leo comhaid 3MF a oscailt agus a chruthú.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-gaf"
}
},
  "lastmod": "2019-12-09"
}

## Cad is comhad 3MF ann?

Úsáideann feidhmchláir 3MF, Formáid Déantúsaíochta 3D, chun samhlacha réad 3D a sholáthar d’fheidhmchláir, ardáin, seirbhísí agus printéirí éagsúla eile. Tógadh é chun teorainneacha agus fadhbanna i bhformáidí comhaid 3D eile a sheachaint, amhail [STL](/cad/stl/), chun oibriú leis na leaganacha is déanaí de phriontálaithe 3D. Is formáid comhaid nua é 3MF atá forbartha agus foilsithe ag cuibhreannas 3MF. Tá sé saibhir go leor chun cur síos iomlán a dhéanamh ar shamhail, ag coimeád faisnéis inmheánach, dath, agus tréithe eile a fhágann go bhfuil sé in-sínte chun tacú le nuálaíochtaí nua sa phriontáil 3D. Tá an fhormáid sínte, in ann í a ghlacadh go forleathan agus saor ó cheisteanna a bhaineann le formáidí comhaid eile a úsáidtear go forleathan.

## Stair Ghearr i bhFormáid Chomhaid 3MF

De bharr na dteorainneacha atá ann cheana féin sna múnlaí formáidí comhaid tuairisciúla atá ar fáil, mar STL agus cinn eile, tá na brandaí is mó le rá ag teacht le chéile agus formáid comhaid níos fairsinge a chur le chéile le haghaidh priontála 3D. Cuireadh san áireamh conas ba cheart d’fheidhmchláir sonraí samhla a chur ar aghaidh chuig printéirí 3D. Mar sin, tháinig an cuibhreannas 3MF ar an saol chun tacú le formáid comhaid 3D nua ar a dtugtar 3MF agus é mar aidhm aige é a dhéanamh insínte go leor chun freastal ar riachtanais priontála 3D. Bhí roinnt cuideachtaí mar chuid den chuibhreannas seo lena n-áirítear Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP agus cinn eile. Bhronn Microsoft a chuid oibre i bhformáid comhaid 3D mar phointe tosaigh d’fhorbairt chomhoibríoch bhreise na sonraíochta ag Cuibhreannas 3MF.

## Formáid Chomhaid 3MF - Tuilleadh Eolais

Is formáid sonraí XML-bhunaithe é 3MF – XML comhbhrúite atá inléite ag an duine – lena n-áirítear sainmhínithe ar shonraí a bhaineann le déantúsaíocht 3D, lena n-áirítear fairsingeacht tríú páirtí le haghaidh sonraí saincheaptha. Dearadh an fhormáid comhaid 3MF agus na teorainneacha agus na saincheisteanna a bhíonn le sárú ag formáidí comhaid 3D eile á gcur san áireamh. Cruthaíodh formáid comhaid 3MF mar thoradh air seo:

* ** Críochnaigh:** An fhaisnéis riachtanach ar fad faoi mhúnla, ábhar agus maoin a bheith i gcartlann amháin

* **Inléite ag an duine:** Ag baint úsáide as struchtúir choiteanna ar nós OPC, [ZIP] (/compression/zip/), agus XML chun forbairt a éascú

* **Simplí:** Sonraíocht ghearr, shoiléir, a fhágann go bhfuil an fhorbairt éasca agus bailíochtaithe go tapa

* **Sínte:** Trí spásanna ainmneacha XML a ghiaráil is féidir síntí poiblí agus príobháideacha araon a dhéanamh agus an chomhoiriúnacht á coinneáil ag an am céanna

* ** Gan athbhrí:** Cinntíonn tástálacha soiléire teanga agus comhlíonta go mbíonn comhad comhsheasmhach i gcónaí ó dhigiteach go fisiciúil

* ** Saor in aisce:** Tá rochtain ar agus cur chun feidhme na sonraíochta 3MF saor ó dhleachtanna, paitinní agus ceadúnú


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## Sonraíochtaí Formáid Comhaid 3MF

Úsáideann formáid comhaid 3MF na sonraíochtaí Pacáistithe Oscailte i bhfoirm cartlainne ZIP dá samhail fhisiciúil. Áiríonn sé sraith dea-shainithe de chodanna agus de ghaolmhaireachtaí a chomhlíonann sainchuspóir sa doiciméad. Fágann sé seo freisin go leanann an fhormáid gné an phacáiste lena n-áirítear sínithe digiteacha agus mionsamhlacha.

### An Doiciméad 3MF - Forbhreathnú

Breathnaíonn doiciméad tipiciúil 3MF mar seo a leanas:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Ainm**|**Cur síos**|** Foinse an Chaidrimh**|**Riachtanach/Roghnach**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Croí-Airíonna|An chuid OPC ina bhfuil airíonna doiciméid éagsúla.|Pacáiste|ROGHNACH
|Bunús an Sínithe Digiteach|An chuid OPC atá mar fhréamh do shínithe digiteacha sa phacáiste.|Pacáiste|ROGHNACH
|Síniú Digiteach|Páirteanna OPC a bhfuil síniú digiteach ar gach ceann díobh.|Bunús Síniú Digiteach|ROGHNACH
|Deimhniú um Shíniú Digiteach|Páirteanna OPC ina bhfuil deimhniú sínithe digiteach.|Síniú Digiteach|ROGHNACH
|PrintTicket|Soláthraíonn sé socruithe atá le húsáid agus an réad(na) 3T a aschur sa chuid den tSamhail 3T.|Samhail 3T|ROGHNACH
|Mionsamhla|Tá íomhá bheag JPEG nó PNG ann a sheasann do na réada 3D sa phacáiste nó sa phacáiste ina iomláine.|Pacáiste|ROGHNACH
|Uigeacht 3D|Tá uigeacht ann a úsáidtear chun dath a chur i bhfeidhm ar réad 3T sa chuid den tSamhail 3T (ar fáil le haghaidh síntí)|Samhail 3T|ROGHNACH
|Páirteanna Saincheaptha|Páirteanna OPC a bhaineann le meiteashonraí|Pacáiste|ROGHNACH

Tugann na rannáin [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) agus [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) faisnéis mhionsonraithe faoin doiciméad 3MF.

## Tagairtí ##

* [Sonraíochtaí Formáid Chomhaid 3MF]( https://github.com/3MFConsortium/spec_core)

* [3MF - Le Vicipéid]( https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


