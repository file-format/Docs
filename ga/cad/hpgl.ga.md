{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Formáid Chomhaid",
"Oscail",
"Léigh",
"Cruthaigh",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid HPGL agus APIanna ar féidir leo comhaid HPGL a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid HPGL - Foghlaim ó Shaineolaithe Formáid Chomhaid!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-gal"
}
},
  "lastmod": "2020-07-28"
}

## Cad is comhad HPGL ann?

I gcomhad HPGFL (Teanga Grafaic Hewlett-Packard) tá tacar treoracha le haghaidh rialú breacaire arna fhorbairt ag HP. Úsáideann breacairí HP an comhad seo chun ábhar veicteoireach agus raster a tharraingt agus a phriontáil ar an bpáipéar.

### Ordú HPGL

Cuimsíonn ordú HPGL iad seo a leanas.
 * Roinn ordaithe den aibítir de dhá charachtair
 * Alt paraiméadar
 * Alt Críochnóra

Ní mór deighilteoir a roinnt ar gach paraiméadar sa chomhad i gcás paraiméadair iolracha.

### Sampla Ordú HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Córas Comhordaithe

Cuimsíonn córais chomhordanáidí táscairí tomhais déthoiseacha chun aon láthair ar leith a aimsiú. Úsáideann an HPGL córas comhordanáidí Breacaire agus comhordanáidí úsáideora araon chun na críche seo.

#### Córas Comhordaithe Breacaire

Úsáidtear an córas comhordanáide seo chun líníochtaí a bhreacadh bunaithe ar ghluaiseacht na blotaire. Is é 0.025mm aonad tipiciúil XY d’íosghluaiseacht breacaire. Athraíonn raon féideartha na líníochta de réir na gcineálacha breacaire.

#### Córas comhordanáidí úsáideora

Is féidir córas comhordanáidí úsáideora sonraithe a bhunú ag baint úsáide as an scála agus an tionscnamh. Déantar iad seo a thiontú go comhordanáidí breacaire ag baint úsáide as an ordú IP agus an ordú SC. Úsáidtear comhordanáidí córais breacaire de réir réamhshocraithe mura ndéantar an tiontú seo.

## Formáid Comhaid HPGL
Tá comhaid HPGL i bhformáid ASCII (comhad téacs) agus is beag orduithe socraithe a thosaíonn siad. Socraíonn sé seo paraiméadair áirithe don bhreatóir le haghaidh breacadh. Breathnaíonn gnáthchomhad HPGL mar seo a leanas.

|Ordú|Brí
---|---|
|IN;|tosaigh, cuir tús le post breactha|
|IP;|socraigh na pointí scálaithe (P1 agus P2) chuig a suíomhanna réamhshocraithe|
|SP1;|roghnaigh peann 1|
|PU0,0;|ardaigh Peann Suas agus bog go dtí an pointe tosaigh don chéad ghníomhaíocht eile|
|PD100,0,100,100,0,100,0,0;|cuir Peann Síos agus bog chuig na suíomhanna seo a leanas (tarraing bosca timpeall an leathanaigh)|
|PU50,50;|Peann Suas agus bog go X,Y comhordanáidí 50,50|
|CI25;|tarraing ciorcal dar ga 25|
|SS;|roghnaigh an tacar carachtar caighdeánach|
|DT*,1;|socraigh an teormharcóir téacs don réiltín, agus ná priontáil iad (an 1, a chiallaíonn fíor) |
|PU20,80;|ardaigh an peann agus bog go 20,80|
|LBHello World*;|tarraing lipéad|

## Tagairtí
 * [HPGL le Vicipéid](https://ga.wikipedia.org/wiki/HP-GL)
 * [Treoir Tagartha HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

