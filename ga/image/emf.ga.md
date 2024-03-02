{
  "date": "2019-10-11",
  "keywords": [
"comhad emf",
"formáid comhaid emf",
"cad is comhad emf ann",
"comhad",
"emf shampla",
"síneadh comhad emf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF - Formáid Meiteafile Feabhsaithe",
  "description": "Foghlaim faoi fhormáid comhaid EMF agus APIanna ar féidir leo comhaid EMF a chruthú agus a oscailt.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad EMF ann?

Stórálann **Formáid mheiteashonraí feabhsaithe (EMF)** íomhánna grafacha go neamhspleách gléas. Is éard atá i meitichomhaid EMF taifid ar fhad athraitheach in ord croineolaíoch ar féidir leo an íomhá stóráilte a sholáthar tar éis parsáil a dhéanamh ar aon fheiste aschuir. Is féidir leis na taifid fad athróg seo a bheith ina sainmhínithe ar rudaí faoi iamh, orduithe le haghaidh líníochta, agus airíonna grafacha atá ríthábhachtach chun an íomhá a thabhairt go cruinn. Nuair a osclaíonn feiste meiteashonraí EMF ag baint úsáide as a timpeallacht ghrafaice féin, fanann comhréireanna, toisí, dathanna agus airíonna grafacha eile na buníomhá mar an gcéanna beag beann ar ardán an ghléis tosaigh.

## Stair Ghearr ##

Sa bhliain 1990, dhear Microsoft formáid comhaid íomhá Windows Metafile ([WMF](/image/wmf/)) do Microsoft Windows. Tá Windows Metafiles formáid 16-giotán a d'fhéadfadh go bhfuil roinnt comhpháirteanna bitmap. Is féidir WMF comhdhéanta de grafaicí veicteoir agus tá sé beartaithe a choinneáil iniompartha i measc feidhmeanna éagsúla. I 1993, d'fhógair Win32/GDI an Metafile Feabhsaithe (EMF), leagan níos nuaí le solúbthacht agus inscálaitheacht feabhsaithe. D'úsáid EMF freisin mar na horduithe teanga grafaicí chun na tiománaithe printéir a rith. Molann Microsoft anois an fhormáid mheiteashonraí feabhsaithe (EMF) thar Windows-format (WMF). Nuair a tugadh isteach Windows XP, eisíodh an leagan Feabhsaithe Metafile Format Plus (EMF+). Faigheann an leagan níos nuaí seo a bhealach trí ghlaonna GDI+ API a shraithiú mar an gcéanna glaonna taifid WMF/EMF chuig GDI. Tá leagan comhbhrúite gzip de EMF ann ar a dtugtar EMZ.

## Formáid Meiteashonraí EMF ##

Seo a leanas na heilimintí riachtanacha den fhormáid mheiteashonraí feabhsaithe:

* EMR_HEADER (leagan, méid, taifeach an phictiúir ag an gcruthú)

* Tábla le haghaidh rudaí GDI

* Pailéad in áirithe (roghnach)

* Taifid metafile eagraithe i struchtúr eagair (socruithe airí, rudaí sainithe, orduithe líníochta)

* Taifead EMR_EOF (taifead deiridh i meitibileán EMF)


## Leaganacha EMF ##
* **Bunaidh**: Sonraíonn an bunleagan an taifead atá riachtanach chun an bhuníomhá a choinneáil agus chun a gléas a choinneáil neamhspleách. Thairis sin tacaíonn an taifead ina bhfuil rudaí grafaicí agus orduithe le haghaidh líníocht.

* **Leagan 1**: Chuir an dara leagan de EMF feabhas ar sholúbthacht agus neamhspleáchas an ghléis tríd an taifead maidir le formáid agus soláthar picteilín a chur leis chun ordú OpenGL a úsáid.

* **Leagan 2**: Chuir an tríú leagan feabhas ar an gcruinneas tríd an gcóras méadrach a chur leis chun fad dromchla an fheiste a thomhas, rud a d’fhág go raibh an taifead níos inscálaithe.


## Taifid Meitifileacha Feabhsaithe ##

Socraítear taifid mheitifileacha i bhfoirm eagair. Tá struchtúr ENHMETARECORD agus fad athraitheach ag na taifid seo. Sonraíonn ENHMETARECORD sonraí a shainíonn feidhmeanna GDI chun pictiúr a chruthú ag baint úsáide as formáid mheiteashonraí feabhsaithe. Is é struchtúr **ENHMETAHEADER** an chéad taifead san fhormáid seo i gcónaí. Tá an fhaisnéis seo a leanas sa cheannteideal EMF seo.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Ba cheart go mbeadh taifead EMF amháin ar a laghad i ngach meiteashonraí. Tá an fhaisnéis a thrasnaítear ó thaifead amháin go ceann eile ag brath ar thaifid EMF agus mar sin ní mór na taifid sin a shocrú taobh le taobh. Ag aon taifead ar leith sa mheiteashonraí seachas EOF_record, sainmhíníonn fad an taifid áirithe sin chun bogadh go dtí an chéad taifead eile.

## Cruthú Meiteashonraí Feabhsaithe ##

Úsáidtear an fheidhm **CreateEnhMetaFile** chun meiteashonraí feabhsaithe a chruthú. Úsáidtear argóintí na bhfeidhmeanna seo le toisí agus stóráil pictiúr ar dhiosca/chuimhne. Ina theannta sin, éilíonn an fheidhm seo toise na feiste inar léiríodh an pictiúr ar dtús (feiste tagartha) agus comhthéacs na feiste tagartha (DC). Mar sin ní mór na hargóintí chun an DC seo a láimhseáil a sholáthar agus an fheidhm **CreateEnhMetaFile** á ghlaoch. Seo a leanas comhréir na feidhme:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** láimhseáil chuig gléas tagartha.

**lptoFilename:** Pointeoir chuig ainm an chomhaid.

**lprc:** Sonraíonn an pointeoir don struchtúr ubhchruthach toisí an phictiúir i mm.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Oibríochtaí Meiteafile Feabhsaithe ##

Seo a leanas na poist is féidir a chur i gcrích trí úsáid a bhaint as an láimhseáil go meiteashonraí feabhsaithe.

* Taispeáin agus cuir in eagar don phictiúr atá stóráilte.

* Cóipeanna meitifileacha feabhsaithe a tháirgeadh.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Déan na dathanna sa phailéad arís.


## Réada Grafaice ##

In oibríochtaí líníochta agus péintéireachta, is féidir taifid chruthaithe réad a chruthú le grafaicí réad agus is féidir iad a shábháil le haghaidh tuilleadh úsáide. Is féidir le taifead `EMR_SELECTOBJECT` na réada grafaice seo a aisghabháil trí úsáid a bhaint as comhthéacs an ghléis athsheinm. Is cineálacha réad ath-inúsáidte iad pinn, pailéid, scuaba, spásanna datha, clónna, agus réada stoic.

## Ordú Beart ##

Baintear úsáid as formáid bheag-endian chun sonraí a stóráil i dtaifid mheiteashonraí.

## Leagan ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Tá foráil ag leaganacha leathnaithe do thaifid OpenGL agus tuairisceoir roghnach don fhormáid inmheánach picteilín. Cuirtear saoráid tomhais i millilítear leis le haghaidh toisí ar taispeáint.

## Tagairtí ##

* [ Meiteashonraí Formáideacha Feabhsaithe | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Formáid agus Sonraíocht Meiteafile Feabhsaithe](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


