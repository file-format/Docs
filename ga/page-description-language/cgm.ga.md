{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Metafile grafaicí ríomhaire",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Grafaicí veicteoir",
"Tuairisceoir Metafile"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid CGM",
  "description": "Foghlaim faoi fhormáid comhaid CGM agus APIanna ar féidir leo comhaid CGM a chruthú agus a oscailt.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-gam"
}
},
  "lastmod": "2021-04-23"
}

## Cad is comhad CGM ann? ##

Is formáid mheiteashonraí caighdeánach idirnáisiúnta é Metafile Ríomhaireachta (CGM) saor in aisce, ardán-neamhspleách, chun grafaic veicteora (2D), grafaic raster, agus téacs a stóráil agus a mhalartú. Úsáideann CGM cur chuige atá dírithe ar oibiachtaí agus go leor forálacha feidhm chun íomhá a tháirgeadh. Úsáideann CGM na tréithe seo atá dírithe ar oibiachtaí chun eilimintí grafacha a athmhúnlú chun íomhá a sholáthar. Tá an fhaisnéis riachtanach i meiteashonraí a shainíonn comhaid eile. In CGM, tá gach eilimint ghrafach is féidir a chur le chéile i gcomhad dénártha i gcomhad foinse bunaithe ar théacs. Go bunúsach, is bealach é CGM chun idirmhalartú sonraí grafacha 2D a éascú, neamhspleách ar aon ardán nó feiste ar leith.

Soláthraíonn formáid CGM gnéithe éagsúla chun feidhmeanna a chomhlíonadh, agus rudaí a shíniú chun primitives geoiméadracha agus faisnéis ghrafach a choigeartú. Cé go bhfuil formáidí eile curtha in ionad CGM chun na healaíona grafacha a thaispeáint ar leathanaigh ghréasáin toisc nach bhfuil tacaíocht mhaith ag leathanaigh ghréasáin dó, tá an-tóir air fós i measc feidhmeanna tionsclaíocha, aerloingseoireachta agus teicniúla eile. Cé go bhfuil WebCGM forbartha ag Cuibhreannas an Ghréasáin Dhomhanda, cur chuige eile maidir le húsáid CGM ar an nGréasán. Léiriú a bhí sa phríomhfheidhmiú CGM ar sheicheamh oibríochtaí bunúsacha an Chórais Eithne Grafaigh (GKS). Níl mórán glactha leis i ndearaí gairmiúla ach tá formáidí eile cosúil le DXF agus SVG curtha ina áit den chuid is mó.

## Stair ##

Tháinig CGM amach mar chaighdeán idirnáisiúnta i 1987 (ISO 8632-1987) agus ghlac BSI agus SAM ag ANSI é mar chaighdeán náisiúnta sa RA. Tar éis roinnt leasuithe a dhéanamh i 1991 eisíodh caighdeán athbhreithnithe CGM i 1992 (ISO 8632:1992). I 2001, d'fhorbair Cuibhreannas an Ghréasáin Dhomhanda WebCGM le cumas feabhsaithe le húsáid leis na leathanaigh ghréasáin. In 2007 eisíodh an dara leagan de WebCGM agus eisíodh an tríú leagan in 2010 le cumais fheabhsaithe.

## Formáid Chomhaid CGM ##

Go bunúsach is bunachar sonraí iad meiteashonraí grafaice ríomhaire le haghaidh faisnéise grafacha agus cuireann siad modhanna ar fáil chun sonraí grafacha a ghabháil, a stóráil agus a tharchur. Dá bhrí sin, ní mór comhpháirt ghrafach chórais a bheith ann chun an bunachar sonraí a chruthú go comhuaineach mar aon le feidhmchlár a chur i gcrích i bhformáid meiteashonraí. I bhformhór na gcásanna, is é an gineadóir Metafile an chomhpháirt seo. Chomh maith leis sin, tá gá le comhpháirt eile atá in ann sonraí grafacha a fháil, a léirmhíniú agus a sholáthar i meitifile. Comhlíontar an riachtanas seo trí ateangaire meitifile a bheith i láthair. Léiríonn an figiúr seo a leanas an timpeallacht oibre meiteashonraí grafach.

Léirítear gaol CGM le comhpháirteanna eile de ghnáthchóras grafaicí san fhigiúr thuas. Is léir freisin ón bhfigiúr nach bhfuil feidhmiúlacht an mheitibilí ag brath ar aschur an fheiste deiridh.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Tuairisceoir meiteafile
1. Bailiúchán d'íomhánna atá neamhspleách go loighciúil

Is éard atá i ngach pictiúr ná bailiúchán de thuairisceoirí pictiúir agus corp pictiúir lena n-áirítear sainmhíniú pictiúr. sainmhíníonn tuairisceoir meiteashonraí faisnéis thuairisciúil a bhaineann go cothrom le gach pictiúr den mheitibil sin. Cuidíonn an t-eolas seo leis an ateangaire meiteashonraí a pharsáil i gceart agus na hacmhainní atá ag teastáil chun pictiúr a rindreáil i gceart a aithint. Cé go gcuimsíonn an tuairisceoir pictiúir an fhaisnéis thuairisciúil freisin, ní féidir leis ach an pictiúr ina bhfuil an tuairisceoir a aithint. Sa bhformáid comhaid seo, tá gach sainmhíniú pictiúr féinchuimsitheach agus ceannasach go loighciúil. Tá siad neamhspleách ar gach sainmhíniú pictiúr eile i gcomhad. Díreach tar éis léirmhíniú an mheiti-thuairisceora, is féidir pictiúir a rochtain agus a léirmhíniú go randamach. Níl aon éifeacht ag athrú ar staid na bpictiúr roimhe seo ar a gcomharbaí. Gné shuntasach eile de CGM is ea an neamhspleáchas pictiúr seo de CGM. Is éard atá i gCGM spás comhordanáidí ar comhordanáidí 2D Cartesianacha ar a dtugtar comhordanáidí feiste fíorúla agus is féidir iad a léiriú trí uimhir nó cruinneas a ionadaíonn an raon agus an gráinneacht. Sonraíonn CGM roghnú díreach dathanna agus roghnú bunaithe ar innéacs. Ar an gcéad dul síos, is éard atá sa sonraíoir dath ná triarach RGB agus níos déanaí, léiríonn an sonróir dath innéacs i dtábla dathanna.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
