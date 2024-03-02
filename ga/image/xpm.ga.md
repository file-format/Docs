{
  "date": "2019-10-11",
  "keywords": [
"Comhad xpm",
"Formáid comhaid xpm",
"Cad is comhad xpm ann",
"comhad",
"sampla xpm",
"Síneadh comhad xpm",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM - X Formáid Chomhaid PixMap",
  "description": "Foghlaim faoi fhormáid comhaid XPM agus APIs ar féidir leo comhaid XPM a chruthú agus a oscailt.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-gam"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad XPM ann?

Is formáid comhaid íomhá é comhad le síneadh .xpm a d'úsáid Córas X Windows. Tacaíonn sé le picteilíní trédhearcacha agus de ghnáth díríonn sé ar chruthú deilbhíní pixmaps. Tacaíonn sé le sonraí monacrómacha, gra-scála, agus dath pixmap. Dearadh iad seo le bheith in eagar de láimh agus is féidir iad a áireamh sa chód [C](/programming/c/). Chun na críche sin, tá comhaid XPM i bhformáid gnáth-théacs agus leanann siad comhréir na teanga ríomhchlárúcháin C. Is féidir comhaid XPM a oscailt le héagsúlacht feidhmchláir féachana íomhá, mar shampla
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView, agus Canvas X.

## Formáid Comhaid XPM

Úsáideann formáid comhaid XPM comhréir C chun iad seo a chomhtháthú i gcláir C agus C++. Tá sé comhdhéanta de na sé rannóg éagsúla seo a leanas.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Is sraith teaghráin iad na hailt mar seo a leanas.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Seo a leanas sonraí gach rannáin.

`<Values> ` - Teaghrán is ea an roinn seo ina bhfuil ceithre nó sé slánuimhir atá i mbonn 10 agus a fhreagraíonn do:

 * leithead agus airde pixmap
 * líon na Dathanna
 * líon na gcarachtar in aghaidh an picteilín
 * comhordanáidí hotspot roghnach agus clib XPMEXT

`<Colors> ` - Tá an oiread teaghráin sa chuid seo agus atá dathanna. Seo a leanas gach teaghrán:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Tá an chuid seo comhdhéanta de<height> teaghráin agus<width> \*<chars_per_pixel> carachtair. Gach<chars_per_pixel> Ba chóir go mbeadh teaghrán fad ar cheann de na grúpaí sainithe roimhe seo sa<Colors> alt.

`<Extension> ` - Ní mór an t-alt síneadh a lipéadú, mura bhfuil sé folamh, sa<Values> alt. Féadfaidh sé a bheith comhdhéanta de roinnt<Extension> fo-ailt a fhéadfaidh a bheith den dá chineál seo a leanas:

 * teaghrán neamhspleách amháin comhdhéanta mar seo a leanas: XPMEXT<extension-name><extension-data>
 * nó bloc comhdhéanta de roinnt teaghráin:XPMEXT<extension-name><related extension-data composed of several strings>

## Tagairtí

* [XPM - Vicipéid](https://en.wikipedia.org/wiki/X_PixMap)

* [Lámhleabhar XPM](http://www.xfree86.org/current/xpm.pdf)


