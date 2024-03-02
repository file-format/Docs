{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"comhad",
"síneadh",
"formáid",
"fuaime",
"smaf",
"síneadh mmf",
"Comhaid mmf",
"Comhad ceoil soghluaiste",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid MMF agus APIanna ar féidir leo comhaid MMF a chruthú agus a oscailt.",
  "title": "MMF - Formáid Chomhaid Cheoil Soghluaiste",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-gaf"
}
},
  "lastmod": "2021-08-09"
}

## Cad is comhad MMF ann?

Is iarmhír comhaid é MMF a bhaineann le comhad SMAF. Seasann an CMA do Mobile Music File ach seasann an SMAF d’Fhormáid Feidhmchláir Soghluaiste le ceol sintéiseach. Sna comhaid MMF laistigh d'fhón cliste tá glórtha an chórais, fuaim agus féadann grafaicí agus taispeáint téacs a bheith iontu freisin. Tá trí chineál paraiméadair ionstraime sa CMA freisin lena n-áirítear FM, PCM, agus Stream PCM. Tá na formáidí comhaid seo comhoiriúnach leis an ardán córais Windows. Déantar na comhaid CMA a chatagóiriú mar chomhaid sonraí. De ghnáth, tacaíonn Microsoft Mail le comhaid MMF. Is féidir an comhad a bhfuil iarmhír MMF aige a chóipeáil chuig aon ghléas soghluaiste nó ardán córais.

Ina theannta sin, tá na comhaid seo i bhfad níos lú i gcomparáid le comhaid chaighdeánacha MIDI. Is féidir comhaid [WAV](/audio/wav/) agus [MID](/audio/mid/) a thiontú go formáid MMF ar féidir iad a roinnt agus a dháileadh mar ábhar fuaime ansin. Is féidir na comhaid seo a fháil trí ríomhphost díreach chuig fóin agus PC.


## Stair Achomair ar Fhormáid Chomhaid CMA

D'fhorbair Yamaha uirlisí SMAF mar chomhaid fuaime ionas gur féidir le fóin chliste líon níos mó clingthoin uathúla a stóráil. Thug Yamaha isteach SMAF le táirgeadh a sliseanna fuaime MA-1, MA-2, MA-3, MA-5, agus MA-7 LSI. Éiríonn na formáidí seo go léir sách eolach ar fhóin phóca i Margadh na hÁise Thoir go luath i 2000.

Ar an leibhéal idirnáisiúnta, d'údaraigh Samsung an fhormáid CMA. Le cabhair ó fhormáid MMF, bhí Samsung in ann raon leathan de ringtones polyphonic a dhearadh le húsáid i bhfóin chliste Samsung.

Bhí Yamaha ag iarraidh an fhormáid a dhéanamh níos mó tóir fós agus mar sin de na comhaid oifigiúla Yamaha SMAF, d'fhoilsigh sé níos mó uirlisí a bhí ag luí leis an bhformáid seo. Leis seo is féidir le húsáideoirí anois comhaid MMF a imirt go héasca ar a gcuid ríomhairí.


## Sonraíochtaí Formáid Chomhaid MMF ##

Déantar comhaid CMA a chatagóiriú i rannáin sonraí. Úsáidtear struchtúr réimír timpeall ar 8 nbeart chun cur síos a dhéanamh ar gach mír.
Áirítear ar an lipéad 4-beart CNTI, OPDA, MSTR, MTR, agus ATR. Is é méid sonraí móide 8 mbeart an méid smután; ríomhtar an méid comhaid iomlán trí na méideanna smután go léir a achoimriú. Mura bhfuil damáiste déanta do chomhad, ba cheart go mbeadh méid an chomhaid achoimrithe mar an gcéanna le méid ceanntásca príomhúil.

### Ceanntásc ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Seo sampla de chomhad MMF:

![](../mmf.png)

## Tagairtí

* [MMF - Le Vicipéid]( https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


