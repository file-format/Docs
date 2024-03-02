{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad MDMP - Formáid Comhaid Minidump Windows",
  "description": "Foghlaim faoi fhormáid comhaid MDMP agus APIs ar féidir leo comhaid MDMP a chruthú agus a oscailt.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-gap"
}
},
  "lastmod": "2022-08-19"
}

## Cad is comhad MDMP ann?

Is éard is comhad MDMP ann ná dumpáil chuimhne d’fheidhmchlár ar Microsoft Windows a chruthaítear nuair a dhúnann an feidhmchlár go neamhghnách nó nuair a thuairteálann sé. Tá faisnéis agus dumpaí sonraí ann ar féidir a úsáid chun cúis na timpiste a dhífhabhtú. Tá comhaid MDMP infheidhme ar fheidhmchláir cruthaithe ag aon ardán ar nós Java, C++, .NET agus eile. Chomh maith le MDMP,

I measc na n-iarratas is féidir comhaid MDMP a oscailt tá Microsoft Visual Studio Debugger.

## Formáid Chomhaid MDMP

Déantar comhaid MDMP a shábháil mar chomhaid dhénártha ar diosca agus is féidir iad a oscailt le dífhabhtóir Microsoft Visual Studio. Tá an t-eolas seo a leanas ann chun cuidiú leis an gcúis leis an timpiste a aithint.

 * Sonraí na teachtaireachta Stop, a paraiméadair, agus sonraí eile
 * Liosta de na tiománaithe luchtaithe
 * Comhthéacs próiseálaí (PRCB) don phróiseálaí a stop ag obair
 * Faisnéis próisis agus comhthéacs eithne (EPROCESS) don phróiseas a stopadh
 * Faisnéis próiseála agus comhthéacs eithne (ETHREAD) don snáithe a stop
 * Stack glaonna mód eithne don snáithe a stopadh

Cuidíonn an t-eolas seo le fáil amach cad a tharla, an fhadhb a réiteach agus cosc a chur uirthi tarlú arís.

### Déan anailís ar Minidump

Éilíonn Windows comhad glaoireachta ar an toirt tosaithe chun comhad dumpála cuimhne a chruthú. Cruthaítear an comhad glaoireachta ar an toirt tosaithe agus ba cheart go mbeadh sé ar a laghad 2 meigibheart (MB) i méid. Cruthaítear an comhad dumpála nuair a thuairteann feidhmchlár. I gcás fadhb eile, cruthaítear an dara comhad dumpála cuimhne beag agus coimeádtar an ceann roimhe sin. Tá ainm an chomhaid dumpála ar leith chun aon fhorscríobh a sheachaint.

Coinníonn Windows liosta de na comhaid dumpála cuimhne ar fad san fhillteán %SystemRoot%\Minidump. Is féidir leat comhaid MDMP a anailísiú trína reáchtáil i Visual Studio Debugger mar atá liostaithe sna céimeanna thíos.

## Conas comhad MDMP a oscailt in Visual Studio?

Is féidir na céimeanna seo a leanas a úsáid chun comhad MDMP a oscailt in Visual Studio.

 * In Visual Studio, ón roghchlár Comhad, roghnaigh Oscail | Dumpáil Tuairteála .
 * Déan nascleanúint go dtí an comhad dumpála is mian leat a oscailt.
 * Roghnaigh Oscail.

## Tagairt

* [Conas an comhad dumpála cuimhne beag atá cruthaithe ag Windows a léamh má tharlaíonn timpiste](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -comhad)


