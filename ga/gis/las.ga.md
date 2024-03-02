{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS - Formáid Chomhaid Lidar LASer",
  "description": "Foghlaim faoi fhormáid comhaid LAS agus APInna ar féidir leo comhaid LAS a chruthú agus a oscailt.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-gas"
}
},
  "lastmod": "2023-07-18"
}

## Cad is Comhad LAS ann?

Is formáid comhaid dhénártha í formáid comhaid LAS (Lidar LASer) atá deartha go sonrach chun sonraí scamall pointe lidar a stóráil. Forbraíodh agus coimeádann an Cumann Meiriceánach um Fhótagraiméadracht agus Cianbhraiteacht (ASPRS) é mar fhormáid chaighdeánaithe le haghaidh malartú sonraí lidar agus idir-inoibritheacht.

Stórálann comhaid LAS faisnéis mhionsonraithe faoi phointí aonair lidar, lena n-áirítear a gcomhordanáidí 3D (x, y, agus z), luachanna déine, cóid aicmithe, agus tréithe breise. Tacaíonn an fhormáid le sonraí tuairisceáin scoite agus lánfhoirmeacha lidar araon, rud a ligeann do thuairisceáin iolracha a stóráil in aghaidh na bíge léasair.

## Formáid Chomhaid LAS

Tá trí phríomhchuid i struchtúr an chomhaid LAS: ceanntásc an chomhaid, na taifid ar fhad athraitheach (VLRanna), agus taifid sonraí na bpointí.

1. Ceanntásc an Chomhaid: Tá faisnéis riachtanach faoin gcomhad LAS i gceanntásc an chomhaid, mar shampla an leagan formáide sonraí, formáid sonraí pointe, líon na bpointí, comhordanáidí an bhosca teorann, an córas tagartha comhordanáidí (CRS), agus meiteashonraí eile. Soláthraíonn sé achoimre ar na sonraí lidar atá sa chomhad.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Taifid Sonraí Pointe: Stórálann na taifid sonraí pointe na tomhais lidar iarbhír. Léiríonn gach taifead sonraí pointe aon phointe lidar amháin agus tá tréithe ann amhail comhordanáidí x, y, agus z, luachanna déine, cóid aicmithe (m.sh. talamh, fásra, foirgnimh), agus tréithe eile arna sainiú ag an úsáideoir. Is féidir leis na taifid pointe stampaí ama a stóráil, comhaireamh tuairisceáin agus uillinneacha scanadh.

Tacaíonn comhaid LAS le formáidí éagsúla sonraí (0 go 10) chun freastal ar chineálacha éagsúla sonraí lidar agus ar an leibhéal faisnéise a theastaíonn. Mar shampla, is ionann formáid 0 agus formáid phointe shimplí le faisnéis bhunúsach, agus soláthraíonn formáidí 1 go 3 sonraí níos cuimsithí lena n-áirítear faisnéis maidir le tonnchruth le haghaidh gach tuairisceáin.

Tacaíonn bogearraí lidar agus uirlisí próiseála go forleathan le comhaid LAS, rud a fhágann gur formáid chaighdeánach iad le haghaidh malartú agus anailísiú sonraí lidar. Ina theannta sin, is féidir comhaid LAS a chomhbhrú trí úsáid a bhaint as teicnící comhbhrú gan chailliúint chun méid comhaid a laghdú agus dílseacht na sonraí bunaidh á gcaomhnú. Is minic a thugtar LAZ ar an leagan comhbhrúite de chomhaid LAS, rud a thairgeann cumas stórála agus aistrithe sonraí éifeachtach.

## Tagairtí

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
