{
  "date": "2023-05-31",
  "keywords": [
"comhad deisce",
"cad is comhad deisce ann",
"cad atá i gcomhad deisce",
"comhad deisce sampla",
"conas a oscailt comhad deisce",
"cad é formáid an chomhaid deisce",
"comhad",
"síneadh comhad deisce",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid DESKTOP - Comhad Iontrála Deisce",
  "description": "Foghlaim faoi fhormáid DESKTOP agus APIs ar féidir leo comhaid DESKTOP a chruthú agus a oscailt.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-ga",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## Cad is comhad DESKTOP ann?

Is comhad cumraíochta é comhad .desktop a úsáideann timpeallachtaí deisce Linux chun aicearraí feidhmchláir agus lainseálaithe a shainiú. Soláthraíonn sé meiteashonraí maidir le feidhmchlár mar a ainm, deilbhín, ordú forghníomhaithe agus airíonna eile. Úsáidtear na comhaid seo de ghnáth chun aicearraí a chruthú i mbiachláir feidhmchlár, i lainseálaithe deisce nó i bpainéil i gcórais bunaithe ar Linux.

## Cad atá i gcomhad DESKTOP?

Leanann comhad .desktop formáid ar leith agus tá roinnt príomhréimsí ann:

- **[Iontráil Deisce]:** Seo é an príomhcheanntásc don chomhad .desktop.
- **Ainm:** Sonraítear ainm an iarratais.
- **Comment:** Provides brief description or comment about application.
- **Exec:** Sainmhíníonn an t-ordú a fhorghníomhú agus an feidhmchlár á sheoladh.
- ** Deilbhín:** Sonraítear cosán chuig an gcomhad deilbhín a bhaineann leis an bhfeidhmchlár.
- **Teirminéal:** Sonraítear ar cheart feidhmchlár a rith i bhfuinneog teirminéil.
- **Cineál:** Sonraítear an cineál iontrála mar Iarratas nó Nasc.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** Sonraítear ar cheart fógra tosaithe a thaispeáint don fheidhmchlár i dtimpeallacht na deisce.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **Gníomhartha:** Sainmhínítear gníomhartha breise is féidir a dhéanamh ar iarratas, mar shampla comhad sonrach a oscailt.

## Comhad DESKTOP samplach

Seo sampla de chomhad .desktop d’eagarthóir téacs bréige dar teideal MyTextEditor”:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Sa sampla seo, sainmhíníonn an comhad .desktop feidhmchlár MyTextEditor agus na hairíonna a bhaineann leis. Áiríonn sé freisin dhá ghníomh breise, Oscail Fuinneog Nua agus Oscail Comhad atá ann cheana, ar féidir rochtain a fháil orthu ó roghchlár comhthéacs an tosaitheoir feidhmchlár.

Trí chomhad .desktop a chur in eolairí ar leith ar nós `/ usr/share/applications` nó `~/.local/share/applications`, aithneoidh timpeallacht na deisce é agus taispeánfaidh sé feidhmchlár dá réir i roghchláir nó ceadóidh sé é a sheoladh ó deasc.

## Conas comhad DESKTOP a oscailt?

Is féidir le roinnt ríomhchlár bogearraí comhaid .deisce a oscailt agus a láimhseáil. Go hiondúil is bainisteoirí comhad nó timpeallachtaí deisce ar chórais Linux-bhunaithe iad na cláir seo. Seo roinnt samplaí:

- **Nautilus (Comhaid):** An bainisteoir réamhshocraithe comhad do thimpeallacht deisce GNOME.
- ** Nemo:** An bainisteoir comhad le haghaidh timpeallacht deisce Cinnamon.
- **Deilf:** An bainisteoir réamhshocraithe comhad le haghaidh timpeallacht deisce Plasma KDE.
- **Thunar:** An bainisteoir réamhshocraithe comhad do thimpeallacht deisce Xfce.
- **Eagarthóir Roghchláir KDE:** Uirlis a bhaineann go sonrach le timpeallacht deisce Plasma KDE a ligeann duit comhaid .deisce a fheiceáil agus a chur in eagar.

Soláthraíonn na bainisteoirí comhad agus timpeallachtaí deisce comhéadan grafach chun comhaid .desktop a bhainistiú. Ligeann siad duit airíonna comhaid .desktop a fheiceáil agus a chur in eagar, lainseálaithe feidhmchlár a chruthú agus aicearraí a eagrú i mbiachláir feidhmchláir nó ar an deasc.

Is comhaid gnáth-théacs iad na comhaid .desktop, ionas gur féidir leat iad a oscailt agus a chur in eagar le do rogha eagarthóir téacs. Níl ort ach cliceáil ar dheis ar an gcomhad .desktop agus roghnaigh Oscail le nó Oscail le feidhmchlár eile chun eagarthóir téacs a roghnú ó liosta na gclár suiteáilte.

## Cad é formáid an chomhaid DESKTOP?

Leanann formáid an chomhaid .desktop struchtúr agus formáid ar leith. Is comhad gnáth-théacs é le sraith de phéirí eochairluacha eagraithe i gcodanna. Seo forbhreathnú ar an bhformáid:

- **Ceanntásca Ranna:** Tosaíonn gach cuid le ceanntásc faoi iamh idir lúibíní cearnacha ([]). Is gnách go dtugtar [Iontráil Deisce] ar an mbunchuid, ina bhfuil na príomh-mheiteashonraí don fheidhmchlár nó don tosaitheoir.
- **Péirí Príomhluacha:** Laistigh de gach cuid, sainmhíníonn tú airíonna trí úsáid a bhaint as péirí eochairluacha. Is é an fhormáid Eochair=Luach. Soláthraíonn an eochair a shainaithníonn maoin agus luach sonraí comhfhreagracha.
- ** Comhréir Maoine:** Is féidir na luachanna maoine a bheith de chineálacha éagsúla lena n-áirítear teaghráin, luachanna Boole, cosáin comhaid nó liostaí. Braitheann an fhormáid do gach luach maoine ar a chineál.
- **Tuairimí:** Is féidir leat tuairimí a chur san áireamh i gcomhad .desktop ag baint úsáide as siombail '#'. Breathnaítear ar aon rud a leanann ‘#’ ar líne mar nóta agus déantar neamhaird de.

## Tagairtí
* [Comhaid Iontrála Deisce](https://www.baeldung.com/linux/desktop-entry-files)


