{
  "date": "2019-10-11",
  "keywords": [
"comhad obj",
"formáid comhaid obj",
"cad is comhad obj ann",
"comhad",
"sampla obj",
"síneadh comhad obj saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid OBJ",
  "description": "Foghlaim faoi fhormáid comhaid OBJ agus APIs is féidir comhaid OBJ a oscailt agus a chruthú.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-gaj"
}
},
  "lastmod": "2019-09-10"
}

## Cad is Comhad OBJ ann?

Úsáideann feidhmchlár Advanced Visualizer Wavefront comhaid **OBJ** chun na réada geoiméadracha a shainiú agus a stóráil. Is féidir sonraí geoiméadracha a tharchur siar agus ar aghaidh trí chomhaid OBJ. Tacaíonn formáid OBJ leis an dá chéimseata polagánach amhail pointí, línte, rinn uigeachta, aghaidheanna agus céimseata saorfhoirme (cuair agus dromchlaí). Ní thacaíonn an fhormáid seo le beochan nó faisnéis a bhaineann le solas agus suíomh radharc.

Is gnách go mbíonn comhad OBJ ina tháirge deiridh den phróiseas samhaltaithe 3D a ghineann CAD (Dearadh Ríomhchuidithe). Is é an t-ordú réamhshocraithe chun rinn a stóráil tuathal a sheachnaíonn gnáthnósanna aghaidhe a dhearbhú go follasach. Cé go ndearbhaítear i gcomhaid OBJ faisnéis scála i líne tráchta fós níor dearbhaíodh aonaid ar bith do chomhordanáidí OBJ.

## Stair na bhformáid 3d obj saor in aisce,

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Tá an fhormáid comhaid oscailte agus curtha i bhfeidhm ag díoltóirí eile dá bhfeidhmchlár grafaicí 3D. Choinnigh Wavefront Technologies an fhormáid comhaid seo foinse oscailte agus neodrach.

## Formáid Chomhaid OBJ

I réada 3D, is obair dhúshlánach é ionchódú na céimseata dromchla a bhain formáid comhaid OBJ go han-mhaith amach. Tá an fhormáid seo ilúsáideach mar go dtugann sé roinnt roghanna chun céimseata dromchla a ionchódú. Seo a leanas trí fhormáid cheadaithe a bhfuil a mbuntáistí agus a n-easnaimh féin acu:

### Teasalú le Aghaidheanna Polagánacha

Éascaíonn formáid comhaid OBJ don úsáideoir dromchla múnla 3D a theisiliú ag baint úsáide as cruthanna simplí nó casta geoiméadracha. Le haghaidh ionchódú céimseata dromchla ar shamhail, stórálann comhad na rinn agus na gnáth-reanna do gach polagán. Cé go méadaíonn teisiliúchán garbh an tsamhail, fós féin is gá an chothromaíocht cheart a fháil idir méid comhaid agus a cháilíocht priontála.

### Cuar saor in aisce

Ligeann formáid comhaid OBJ do na cuair dromchla saorfhoirme atá sainithe ag an úsáideoir céimseata dromchla na samhla a shonrú. Toisc go bhfuil cuair shaorfhoirmeacha níos casta ná aghaidheanna polagánacha mar, agus gan mórán paraiméadair matamaitice acu, is fearr línte cuartha a shainiú le cuair shaorfhoirmeacha. Mar sin, le níos lú sonraí i gcomparáid le teisilithe polagánacha, úsáidtear cuair shaorfhoirmeacha chun ionchódú ardcháilíochta ar aon mhúnla 3D a ghiniúint gan méid an chomhaid a leathnú.

### Dromchlaí Saorfhoirme

Sonraíonn formáid comhaid OBJ freisin tiling na céimseata dromchla le paistí dromchla saorfhoirme. Tá an cineál seo paistí dromchla saorfhoirme (NURBS) an-oiriúnach do dhromchlaí gan toisí dochta gathacha cosúil le corp trucaile, sciatháin héileacaptair nó cabhlach báid. Tá sé an-bhuntáisteach dromchlaí saorfhoirme a úsáid mar go bhfuil siad níos cruinne chun méideanna comhaid a choinneáil níos lú ag cruinneas níos airde. Tá na dromchlaí seo mar chuid riachtanach den tionscal aeraspáis agus feithicleach áit a bhfuil an cruinneas íseal unforgiving.

Socraítear na heochairfhocail seo a leanas de réir cineáil sonraí chun céimseata dromchla a shainiú.


| Eilimintí | Cuar saorfhoirme/ráitis choirp an dromchla | Cuar saorfhoirme/tréithe dromchla
---|---|---|
|p|Pointe|parm|Luachanna paraiméadair|céim|Céim
|l|Líne|Baile Átha Troim|Lúb scamhadh seachtrach|bmat|Bun-mhitrís
|f|Aghaidh|poll|Lúb scamhadh istigh|céim|Méid na céime
|cuar|Cuar|scrv|Cuar speisialta|ctype|Cuar nó cineál dromchla
|cuar2|Cuar 2T|sp|Pointe speisialta|**Nascacht agus Grúpáil dromchlaí**
|surf|Dromchla|deireadh|Ráiteas deiridh|con|ceangal
|**Aitreabúidí taispeána/rindreála**|g|Ainm an ghrúpa
|bevel|Idirshuíomh bevel|scáth_obj|Teilgin scáth|s|Grúpa smúdála
|lod|Leibhéal mionsonraí|trace_obj|Rianú gatha|mg|Grúpa cumasc
|d_interp|Tuaslag idirshuíomh|ctech|Teicníc comhfhogasú cuar|o|Ainm an ábhair
|c_interp|Idirshuíomh dathanna|stech|Teicníc comhfhogasú dromchla|
|usemtl|Ainm an ábhair|mtllib|Leabharlann ábhair|
|**Rinneanna geoiméadracha** |
|v|Rinneanna geoiméadracha|vn|Gnormáltaí rinn|
|vt|Reanna uigeachta|vp|Rinneoga spáis pharaiméadar|

### Dath agus Uigeacht

Ceadaíonn comhad OBJ faisnéis datha agus uigeachta a stóráil i bhformáid comhaid ghaolmhar ar a dtugtar an Leabharlann Ábhar Teimpléad (MTL). Rindreáil samhlacha geoiméadracha il-dathanna ag baint úsáide as an dá chomhad seo le chéile. Tá comhaid MTL bunaithe ar ASCII agus éascaíonn siad rindreáil ríomhaire trí chur síos a dhéanamh ar airíonna frithchaiteacha an tsolais ag baint úsáide as samhail fhrithchaitheamh Phong. Tá an caighdeán glactha ag líon mór díoltóirí bogearraí a bhaineann leas as ábhar a idirmhalartú. Tá formáid MTL beagán as dáta toisc nach bhfuil tacaíocht aici sna teicneolaíochtaí is déanaí mar léarscáileanna specular agus parallax.

## Tagairtí

* [Comhad Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


