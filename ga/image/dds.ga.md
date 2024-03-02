{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid DDS- Comhad Íomhá Dromchla DirectDraw",
  "description": "Foghlaim faoi fhormáid comhaid DDS agus APIanna ar féidir leo comhaid DDS a chruthú agus a oscailt.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-gas"
}
},
  "lastmod": "2022-04-02"
}

## Cad is comhad DDS ann?

Is comhad íomhá raster é comhad DDS a úsáideann formáid coimeádáin DirectDraw Surface (DDS). Stórálann sé uigeachtaí neamh-chomhbhrúite agus comhbhrúite (DXTn) agus cuireann sé cineálacha éagsúla i bhfeidhm chun cineálacha éagsúla sonraí a stóráil. Tacaíonn sé freisin le roinnt cineálacha éagsúla sonraí ar nós uigeachtaí aonchiseal, uigeachtaí le mipmaps, léarscáileanna ciúb, léarscáileanna toirte agus eagair uigeachta. Ligeann sé seo do na comhaid DDS samhlacha aonad uigeachta físchluiche a stóráil chomh maith le grianghraif dhigiteacha agus chúlraí deisce Windows. D'fhorbair Microsoft formáid comhaid DDS le húsáid le DirectX SDK.

## Formáid Chomhaid DDS

Sábháltar comhaid DDS mar chomhaid dhénártha agus is féidir iad a úsáid le DirectX SDK. Úsáideann sé cumhacht DirectX chun feidhmchláir rindreála fíor-ama ar nós cluichí 3D a fhorbairt.

### Leagan Amach Comhad DDS

Tá an [DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) doiciméadaithe go mion ag Microsoft. Tá an fhaisnéis seo a leanas i gcomhad dénártha DDS.

 * DWORD (uimhir draíochta) ina bhfuil an luach cód ceithre charachtar 'DDS' (0x20534444).
 * A description of the data in the file.

Déanann an DDS_HEADER cur síos ar na sonraí agus déanann an DDS_PIXELFORMAT cur síos ar an bhformáid picteilín. Tagann an dá cheann seo in ionad struchtúir DDSURFACEDESC2, DDSCAPS2 agus DDPIXELFORMAT DirectDraw 7 atá dímheasta.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

Déanann an [programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) mionsonraí teicniúla na formáide comhaid seo a mhionsaothrú tuilleadh.

## Tagairtí

* [DDS - Le Vicipéid](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [Lámhleabhar Tagartha Teicniúil Formáid Chomhaid ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)


