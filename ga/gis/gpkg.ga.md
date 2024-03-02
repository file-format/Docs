{
  "date": "2021-07-29",
  "keywords": [
"comhad gpkg",
"formáid comhaid gpkg",
"cad is comhad gpkg ann",
"comhad",
"sampla gpkg",
"síneadh comhad gpkg",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG - Comhaid Formáide GeoPackage",
  "description": "Foghlaim faoi fhormáid comhaid GPKG agus APIs ar féidir leo comhaid GPKG a chruthú agus a oscailt.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## Cad is comhad GPKG ann?
Is éard atá i gcomhad le síneadh .gpkg ná córas faisnéise geografaí a chuirtear i bhfeidhm mar choimeádán bunachar sonraí SQLite ina bhfuil táblaí sonraí agus meiteashonraí le sainmhínithe tipiciúla, teorainneacha formáide, dearbhuithe sláine agus srianta inneachair. Foilsíodh é in 2014; sainithe ag an OGC (Cuibhreannas Geospásúil Oscailte) thar ceann míleata na SA. Tacaíonn rialtais éagsúla, eagraíochtaí tráchtála agus foinse oscailte go forleathan leis an GeoPackage.

## Formáid comhaid GPKG
Tá GeoPackage comhdhéanta mar chomhad bunachar sonraí SQLite 3 leathnaithe; sainmhíníonn caighdeán sraith rialacha (gnásanna riachtanacha) le haghaidh:
- Leagann tíl maitrís íomhánna a stóráil
- Gnéithe veicteoir
- Léarscáileanna Raster ar scálaí éagsúla
- Meiteashonraí agus scéimre

Is féidir leat GeoPackage a leathnú trí úsáid a bhaint as na rialacha síneadh mar atá sainmhínithe i gclásal 2.3 den chaighdeán. Ba é an cuspóir a bhí le GeoPackage a dhearadh ná bunachar sonraí éadrom a dhéanamh oiread agus is féidir agus é a áireamh i gcomhad aonair réidh le húsáid. Déanann sé seo an-oiriúnach le haghaidh feidhmchláir mhóibíleacha i mód as-líne agus comhroinnt tapa ar ghléasanna stórála scamall nó USB, etc.

### Ábhar GPKG
Tá roinnt táblaí sna GeoPackages, cosúil le bunachair shonraí choibhneasta eile. Is féidir na táblaí seo a bheith sainithe ag úsáideoirí nó táblaí meiteashonraí. Tá dhá thábla meiteashonraí éigeantacha i GeoPackages:

#### gpkg_contents
Clár ábhar do GeoPackage. Is iad na colúin éigeantacha sa tábla seo:

- **table_name**: ainm iarbhír an tábla sonraí atá sainithe ag an úsáideoir;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x, agus max_y**: fairsinge spásúlachta an ábhair. ;
- **srs_id**: córas tagartha spáis .

#### gpkg_spatial_ref_sys
Le haghaidh ábhar tagartha spáis; lena n-áirítear tíleanna agus gnéithe, ach gan a bheith teoranta dóibh, ní mór do gach sraith san ábhar tagairt a dhéanamh do chóras tagartha comhordanáidí; stóráilte sa tábla **gpkg_spatial_ref_sys**. Is iad na colúin éigeantacha sa tábla seo:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-gae;
- **eagraíocht**: Ainm cás-neamhíogair na heagraíochta sainithe.
- **organisation_coordsys_id**: ID uimhriúil an SRS arna sannadh ag an eagraíocht;
- **sainmhíniú**: Sainmhíniú Téacs Aithnidiúil ar an SRS.


## Tagairtí

* [GeoPackage - le Vicipéid](https://ga.wikipedia.org/wiki/GeoPackage)

* [Ag Tosú Le GeoPackage](http://www.geopackage.org/guidance/getting-started.html)


