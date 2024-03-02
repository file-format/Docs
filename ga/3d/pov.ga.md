
{
  "date": "2023-01-05",
  "keywords": [
"comhad pov",
"formáid comhaid pov",
"cad is comhad pov ann",
"comhad",
"sampla pov",
"síneadh comhad pov",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid POV agus APIanna ar féidir comhaid POV a oscailt agus a chruthú.",
  "title": "POV - Marthanacht an Chomhaid Físe",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-gav"
}
},
  "lastmod": "2023-01-05"
}

## Cad is comhad POV ann?

Comhad gnáth-théacs is ea comhad POV ina bhfuil treoracha do na bogearraí rianaithe gathanna POV-Ray. Tá na treoracha seo scríofa i dteanga scriptithe speisialta a bhaineann go sonrach le POV-Ray. Sonraíonn sé an radharc atá le déanamh, lena n-áirítear na rudaí 3D, na hábhair, an soilsiú, agus airíonna eile a shainíonn cuma an radhairc. Úsáideann comhaid POV teanga scriptithe speisialta a bhaineann go sonrach le POV-Ray agus is féidir í a úsáid chun radhairc 3D casta agus mionsonraithe a chruthú. Is gnách gur .pov nó .povray an síneadh comhad le haghaidh comhad POV. Nuair a osclaíonn tú comhad POV in POV-Ray, léann na bogearraí na treoracha sa chomhad agus úsáideann iad chun íomhá rindreáilte den radharc a ghiniúint.

Is minic a úsáideann ealaíontóirí agus dearthóirí na comhaid .pov chun grafaic 3D agus beochan a chruthú le haghaidh feidhmeanna éagsúla, lena n-áirítear scannán, teilifís, cluichí físeáin agus ábhair mhargaíochta.

## Formáid Chomhaid POV

Tosaíonn an comhad **.pov** de ghnáth le sraith de ráitis **#include**, a úsáidtear chun leabharlanna dathanna réamhshainithe, uigeachtaí, agus acmhainní eile ar féidir a úsáid sa radharc a áireamh. Ansin, sainmhíníonn an comhad rudaí, ábhair agus airíonna eile an radhairc ag baint úsáide as sraith bloic. Tá go leor cineálacha eile rudaí, ábhair, agus airíonna eile ann ar féidir leat a shonrú i gcomhad .pov, agus is féidir leat lúba agus ráitis choinníollacha a úsáid chun radhairc níos casta agus níos mionsonraithe a chruthú.

## Feidhmchláir Bogearraí le haghaidh POV

Úsáideann bogearraí rianaithe gatha POV-Ray an fhormáid comhaid .pov, mar sin is é an príomhfheidhmchlár chun comhaid .pov a oscailt ná na bogearraí POV-Ray féin. Is féidir leat an leagan is déanaí de POV-Ray a íoslódáil ón láithreán gréasáin oifigiúil ag https://www.povray.org/.

Chomh maith le POV-Ray, tá roinnt feidhmchlár eile ann ar féidir comhaid .pov a oscailt agus a chur in eagar, lena n-áirítear:

- BRL-CAD: Bogearraí samhaltaithe foinse oscailte 3D atá in ann comhaid .pov a allmhairiú agus a onnmhairiú
- MeshLab: Bogearraí próiseála mogalra 3D ar féidir leo comhaid .pov a allmhairiú agus a onnmhairiú
- Cumascóir: Bogearraí grafaic 3D foinse oscailte a bhfuil tóir orthu ar féidir leo comhaid .pov a allmhairiú agus a onnmhairiú

D'fhéadfadh go mbeadh feidhmchláir bogearraí eile ann ar féidir comhaid .pov a oscailt freisin, agus mar sin b'fhéidir gur mhaith leat triail a bhaint as breathnóir comhad nó uirlis tiontaire mura bhfuil tú in ann comhad .pov a oscailt leis na feidhmchláir thuas.

## Sampla POV

Mar shampla, seo sampla comhad .pov a shainíonn radharc le sorcóir gorm amháin:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Sa sampla seo, sonraíonn an bloc ceamara suíomh agus treoshuíomh an cheamara sa radharc, dearbhaíonn an bloc `foinse_solais` foinse solais agus sonraíonn sé a shuíomh agus a dath, agus dearbhaíonn an bloc `sorcóir` réad sorcóra agus sonraíonn sé a chríochphointí, ga, agus airíonna ábhar. Nuair a osclaíonn tú an comhad .pov seo sna bogearraí POV-Ray, soláthróidh sé íomhá de shorcóir gorm amháin.

## Tagairtí
 * [POV-Ray - Vicipéid](https://en.wikipedia.org/wiki/POV-Ray)
 * [Láithreán Gréasáin POV-Ray Doiciméadaithe](http://www.povray.org/documentation/)

