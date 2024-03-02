{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT - Comhad Teimpléad Ríomhphoist Microsoft Outlook",
  "description": "Foghlaim faoi fhormáid comhaid OFT agus APIanna ar féidir leo comhaid OFT a chruthú agus a oscailt.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-gat"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad OFT ann?

Is comhaid teimpléid iad comhaid le síneadh .oft a chruthaítear trí úsáid a bhaint as Microsoft Outlook. Úsáidtear an leagan amach réamhfhormáidithe do theimpléid teachtaireachta ansin chun ríomhphoist a sheoladh amach le faisnéis choiteann chun am a shábháil. Is féidir comhaid den sórt sin a ghiniúint trí ríomhphost nua a chruthú, an fhaisnéis riachtanach a chur leis agus ansin an Teimpléad Oifige Save As (.oft) a úsáid ó Microsoft Outlook. Is féidir le húsáideoirí na comhaid OFT a oscailt trí chliceáil faoi dhó air agus osclófar iad san fheidhmchlár gaolmhar ar an gcóras áirithe sin.

## Struchtúr Comhad OFT ##

Úsáideann formáid comhaid .OFT an fhormáid comhaid [MSG](/email/msg/) mar bhunáit. Is é an t-aon difríocht ná go bhfuil CLSID_TEMPLATEMESSAGE ({0006F046-0000-0000-C000-000000000046}) mar chomhaid OFT) mar an aicme stórála (WriteClassSTG), agus úsáideann comhaid MSG CLSID_MAILMESSAGE ({00020d0b-0000-0000-C000-00000000}).

Is í formáid CFB_3 bun an chomhaid MSG. Tá an paradigm bunaithe ar na coincheapa stórála agus sruthanna, gar go leor d'eolairí agus do chomhaid. Mar sin difríocht mhór sa chéad cheann is ea an t-ordlathas iomlán, atá pacáistithe i gcomhad ar leith, ar a dtugtar comhad cumaisc. Is ionann réada agus na comhaid teachtaireachta agus is airí amháin nó a bailiúcháin atá iontu. Éascaíonn an cumas seo feidhmchláir sonraí casta, struchtúrtha a stóráil i gcomhad amháin. Sonraíonn an fhormáid seo freisin stórais iolracha, seasann gach stóras don réad Teachtaireacht mar phríomh-chomhpháirt. Tá roinnt sruthanna sna stórais seo a léiríonn airí den chomhpháirt sin. Is féidir stóráil a neadú freisin.

### Airíonna OFT

Ag barrleibhéal an chomhaid .msg, bíonn sruthanna i stórais a stórálann airíonna iontu. Is féidir airíonna a chatagóiriú mar seo a leanas:

* Airíonna fad seasta

* Airíonna faid athraitheach

* Airíonna illuacha


Beag beann ar an gcatagóir, is éard atá i maoin ná clib nó ainmnithe. Mar sin féin, tá faisnéis oiriúnach léarscáilithe ag teastáil le haghaidh maoine ainmnithe mar atá sonraithe ag a stór mapála.

### Stórais OFT

Is iad stórais na príomhchodanna den réad Teachtaireachta. Luann formáid comhaid MSG na stórais seo a leanas:

### Struchtúr Ardleibhéil

Is ionann réad teachtaireachta agus barrleibhéal iomlán na formáide comhaid Msg. Ag brath ar an gcineál, airíonna, líon na bhfaighteoirí agus réada Iatán, is féidir le réad teachtaireachta stórais srutha éagsúla a bheith ina chomhad .MSG comhfhreagrach.

#### Gaol le Struchtúir Eile

Tá na caidrimh seo a leanas ag formáid comhaid MSG/OFT le struchtúir eile:

* Is é an bonn de .msg Formáid Comhad Dénártha Comhdhúile.

* Úsáideann an fhormáid seo na hairíonna a úsáideann Teachtaireacht agus Prótacal Oibiachta Iatán.


## Tagairtí

* [[MS-OXMSG]: Formáid Chomhaid Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


