{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid MKS",
  "keywords": [
"mks",
"Físeán matroska",
"Formáid mkv",
"comhad",
"formáid",
"físeán"
],
  "description": "Foghlaim faoi fhormáid comhaid MKS le haghaidh fotheidil a chruthaigh Matroska agus APIanna amháin ar féidir leo comhaid MKS a chruthú agus a oscailt.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-gas"
}
},
  "lastmod": "2021-25-02"
}

## Cad is comhad MKS ann?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- Na .mks”. bainfidh an comhad Matroska úsáid as an síneadh (nach mbeidh ach fotheidil ann).
- Tá **CodecPrivate** á úsáid chun gach faisnéis a bhaineann le codecs atá domhanda i sruth iomlán a stóráil.
- Bain na stampaí ama Tosaigh agus stop a úsáidtear i bhformáid stórála dúchais stampa ama. Ina áit sin, bain úsáid as stampa ama Bloic agus Fad.
- Is féidir leat aon rud a úsáid le ciseal trédhearcach, lena n-áirítear físeán.

## Formáidí Coiteann Fotheideal

Here are some brief notes about more common subtitle formats stored in Matroska:

### Íomhánna Fotheidil
Is í an fhormáid fotheideal VobSub an chéad fhormáid fotheideal íomhá a allmhairítear isteach i Matroska. Gintear an fhormáid seo trí na fotheidil a onnmhairiú ó DVD. Ba cheart na rianta a scaradh agus iad á stóráil i Matroska má tá an VobSub comhdhéanta de shraith sruthanna iolracha.

### Fotheidil SRT
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Uimhir a léiríonn seicheamh an fhotheideal.
 2. Tá an t-am láithrithe agus imithe as feidhm ag an bhfotheideal ar an scáileán.
 3. An fotheideal féin.
 4. Líne bhán chun tús an chéad fhotheideal eile a chur in iúl.
 
### Fotheidil SSA/ASS
Is formáid comhaid é Sub Station Alpha (SSA) a úsáideann an t-eagarthóir fotheideal coitianta SubStation Alpha. Úsáideann fansubbers na fotheidil SSA go forleathan. Tá an cumas aige gnéithe nua-aimseartha a thaispeáint, m.sh. karaoke, suíomh, stíliú, etc.
 
### Fotheidil WebVTT
D’fhorbair Cuibhreannas an Ghréasáin Dhomhanda (W3C) an WebVTT a ghiorrú mar Formáid Téacs Rianta Físeáin Gréasáin”. Tá an fhormáid seo á húsáid chun acmhainní rian téacs seachtracha a mharcáil i dtaca leis an eilimint HTML.

### Fotheidil grafaicí cur i láthair HDMV
Is sraith giotánmaps é formáid fotheideal grafaic léirithe HDMV (HDMV PGS) agus ní féidir linn téacs a rá ar chor ar bith. I bhfocail eile, is féidir leat a rá nach bhfuil ann ach seicheamh uainithe d’íomhánna grafacha. Chun an fhaisnéis a bhaint, is próiseas riachtanach é PGS a thiontú go SRT.

### Fotheidil téacs HDMV
Tugtar an fhormáid téacsúil fotheideal a úsáidtear ar Blu-rays ar an téacs HDMV. Ní cheadaíonn Matroska ach tacar carachtar UTF-8 Nuair a stórálann na fotheidil TextST.

### Fotheidil Chraolacháin Dhigiteacha Físe (DVB).
Tugadh isteach an fhormáid fotheideal DVB chun tarchur agus taispeáint roinnt teangacha fotheidealaithe ar chomharthaí teilifíse a rialú. Chuirfeadh gnáthfhormáid fotheidealaithe ar chumas aon lucht féachana féachaint ar tharchuir fhotheidealaithe DVB, is cuma cén déantúsóir atá ar na córais tarchurtha.


## Tagairtí ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

