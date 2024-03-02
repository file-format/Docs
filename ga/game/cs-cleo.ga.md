{
   "date":"2023-01-04",
   "keywords":[
"cs",
"comhad cs",
"Cs cleo scripteanna saincheaptha",
"Conas a oscailt comhad cs",
"comhad",
"Síneadh comhad cs",
"síneadh",
"comhad"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Formáid Comhaid CS - Script Chustaim CLEO",
   "description":"Foghlaim faoi fhormáid Script Chustaim CS CLEO agus APIs ar féidir leo comhaid CS a chruthú agus a oscailt.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo-ga",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## Cad is comhad CS ann?

Tagraíonn comhad .CS i gcomhthéacs CLEO (gearr do Leabharlann CLEO) de ghnáth do chomhad scripte saincheaptha a úsáidtear i sraith cluichí físeáin Grand Theft Auto (GTA). Is creat modding coitianta é CLEO a ligeann d’imreoirí scripteanna saincheaptha a chruthú agus a chur le cluichí GTA a chuireann ar a gcumas gameplay a mhodhnú, gnéithe nua a chur leis agus an taithí cluichíochta iomlán a fheabhsú.

## Forbhreathnú ar chomhad CS

Seo forbhreathnú bunúsach ar cad a d’fhéadfadh a bheith i gcomhad .cs in CLEO:

1.  **Cód Scripte**: Tá cód scripte scríofa i dteanga scriptithe CLEO i gcomhad .cs. Baineann an teanga scriptithe seo go sonrach le CLEO agus úsáidtear í chun iompar scripteanna saincheaptha laistigh den chluiche a shainiú. Is féidir an cód a scríobh le heagarthóir téacs agus de ghnáth leanann sé comhréir ar leith.
    
2.  **Modifications**: CLEO scripts can make various modifications to game such as changing behavior of in-game objects, creating custom missions, adding new vehicles, weapons and more. The possibilities are extensive and depend on creativity and programming skills of script author.
    
3.  ** Truicear**: Is minic go n-áiríonn scripteanna CLEO truicear a chinneann cathain agus conas ba cheart script shaincheaptha a rith. Féadfaidh na truicear seo a bheith bunaithe ar imeachtaí i gcluiche, ar ghníomhaíochtaí imreora nó ar choinníollacha sonracha.
    
4.  **Athróga agus Feidhmeanna**: Is féidir le scripteanna CLEO athróga a úsáid chun sonraí a stóráil agus a ionramháil, chomh maith le feidhmeanna chun cód a chuimsiú agus a athúsáid. Úsáidtear na hathróga agus na feidhmeanna seo chun iompar na scripte a rialú.

## Sampla de chomhad CS

Seo sampla simplí de script CLEO .cs a athraíonn an aimsir sa chluiche:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## Leabharlann CLEO

Is creat modhála cumhachtach é an **Leabharlann CLEO**, ar a dtugtar CLEO” go minic do shraith cluichí físeáin Grand Theft Auto (GTA). Ligeann sé d’imreoirí agus do modders scripteanna saincheaptha a chruthú agus a chur le cluichí GTA ar a gcumas gameplay a mhodhnú, gnéithe nua a chur leis agus an taithí cluichíochta iomlán a fheabhsú. Tá clú ar CLEO go háirithe mar gheall ar a solúbthacht agus éascaíocht úsáide i bpobal modding GTA.

Seo a leanas roinnt príomhghnéithe agus gnéithe de Leabharlann CLEO:

1.  **Teanga Scriptithe**: Tugann CLEO isteach a theanga scriptithe, a bhaineann go sonrach leis an gcreat modhála. Tá an teanga scriptithe deartha le bheith sách éasca le tuiscint agus oibriú léi, rud a fhágann go mbeidh sé inrochtana do modders nua-aimseartha agus taithí.
    
2.  **Scripteanna Saincheaptha **: Le CLEO, is féidir leat scripteanna saincheaptha a chruthú ar féidir leo raon leathan feidhmeanna a chomhlíonadh laistigh de shaol an chluiche. Féadfaidh na scripteanna seo iompar in-chluiche a athrú misin nua a chur leis, feithiclí nó airm nua a thabhairt isteach, fisic cluiche a athrú agus go leor eile.
    
3.  **Trúigeoirí agus Imeachtaí**: Is féidir le himeachtaí éagsúla in-chluiche, gníomhartha imreora nó coinníollacha sonracha scripteanna CLEO a spreagadh. Ligeann sé seo do modders ábhar dinimiciúil agus idirghníomhach a chruthú laistigh den chluiche.
    
4.  **Support for Multiple GTA Versions**: CLEO has versions tailored to different GTA games, including GTA III, GTA Vice City, GTA San Andreas, GTA IV and others. This means that modders can create and share their custom scripts for different GTA titles.

## Formáidí Comhaid Úsáidte ag Leabharlann CLEO

I modding CLEO do chluichí Grand Theft Auto (GTA), úsáidtear roinnt formáidí comhaid go coitianta chun mods a chruthú agus a shuiteáil. Feidhmíonn na formáidí comhaid seo chun críocha éagsúla ó scripteanna iarbhír a bheith ann go stóráil acmhainní breise mar uigeachtaí, samhlacha nó fuaime. Seo cuid de na formáidí tábhachtacha comhaid a úsáidtear i modding CLEO:

1.  **.cs (Script Chustaim)**: Is comhaid scripte saincheaptha iad comhaid CLEO .cs scríofa i dteanga scriptithe CLEO. Tá cód sna comhaid seo a shainíonn iompar agus feidhmiúlacht mod. Tá comhaid .cs mar chroílár modding CLEO agus déantar iad a fhorghníomhú ag cluiche chun gnéithe saincheaptha a chur i bhfeidhm.
    
2.  **.CSA (Cartlann an Chustaim Scripteanna)**: Is cartlann iad comhaid .CSA ar féidir comhaid scripte .cs iolracha a stóráil. Is minic a úsáidtear iad chun scripteanna gaolmhara a phacáistiú le chéile chun iad a shuiteáil agus a bhainistiú níos éasca.
    
3.  **.fxt (Comhaid Théacs)**: Is comhaid téacs iad comhaid .fxt ar féidir iad a úsáid chun aistriúcháin téacs a logánú nó a sholáthar do mhodhanna CLEO. Tá teaghráin téacs iontu ar féidir iad a thaispeáint sa chluiche, rud a fhágann go bhfuil mods inrochtana ag imreoirí i dteangacha éagsúla.
    
4.  **[.bmp](/image/bmp/), [.png](/image/png/), [.jpg](/image/jpeg/) (Formáidí Íomhá)**: Úsáidtear na formáidí íomhánna seo chun uigeachtaí agus íomhánna le haghaidh modhnuithe a stóráil. Is féidir iad a úsáid le haghaidh craicne saincheaptha, uigeachtaí feithicle, eilimintí HUD agus níos mó. Ag brath ar chluiche, b'fhéidir gur fearr formáidí éagsúla íomhá.

## Conas comhad CS a oscailt?

Chun a bhfuil i gcomhad CLEO .cs (Script Chustaim) a oscailt agus a fheiceáil, is féidir leat eagarthóir téacs nó eagarthóir cód de do rogha féin a úsáid. I measc na roghanna coitianta tá:

- **Notepad**: Eagarthóir téacs simplí a thagann réamhshuiteáilte le Windows.
- **Notepad++**: Eagarthóir téacs níos saibhre atá deartha le haghaidh códaithe agus scriptithe.
- **Cód Amharc-Stiúideo**: Eagarthóir cód móréilimh, saor in aisce agus an-sínte.
- **Téacs sublime**: Eagarthóir cód eile a bhfuil aithne air as a luas agus a solúbthacht.
- **Atom**: Eagarthóir cód foinse oscailte arna fhorbairt ag GitHub.

## Comhaid CS eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.cs**.

**Comhaid Sonraí & Cluiche**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Clárú**
- [CS - CSharp Code File](/programming/cs/)

## Tagairtí
* [leabharlann CLEO]( https://cleo.li/)


