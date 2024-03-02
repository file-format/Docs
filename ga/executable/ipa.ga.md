{
  "date": "2021-08-30",
  "keywords": [
"comhad ipa",
"formáid comhaid ipa",
"Cad is comhad ipa ann",
"comhad",
"sampla ipa",
"síneadh comhad ipa",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid IPA agus APIanna ar féidir leo comhaid IPA a chruthú agus a oscailt.",
  "title": "IPA - Comhad Pacáiste Feidhmchláir iOS",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-gaa"
}
},
  "lastmod": "2021-08-30"
}

## Cad is comhad IPA ann?
Baineann comhad le síneadh .ipa leis an iOS agus tugtar comhad pacáiste feidhmchláir air. Comhad cartlainne é seo (comhbhrúite le comhbhrú [ZIP](/compression/zip/)) a stórálann feidhmchlár iOS, ach ní féidir an feidhmchlár sin a shuiteáil ach ar ghléasanna MacOS iOS nó ARM, mar iPad, iPhone nó iPod Touch. Go príomha, is féidir iTunes, Apple Configurator 2, nó aon bhogearraí tríú páirtí a úsáid chun comhaid IPA a shuiteáil.

## Formáid comhaid IPA
Tá na forbróirí IOS atá ag forbairt na n-aipeanna ag baint úsáide as an Apple Xcode an-eolach ar chomhaid IPA mar go gcaithfidh siad a gcuid apps forbartha a phacáistiú mar chomhaid IPA chun críocha imscaradh siopa app a thástáil. Cé gur eol go bhfuil na comhaid IPA suiteáilte mar apps iOS, áfach, is féidir leat iad a dhí-chomhbhrú freisin chun na sonraí app atá ann a fheiceáil. Ós rud é nach bhfuil ach dénártha amháin i gcomhad IPA le haghaidh ailtireacht ARM na nguthán póca agus nach bhfuil dénártha ann don ailtireacht x86, ní féidir go leor comhad .ipa a shuiteáil ar an Insamhlóir iPhone.
### Struchtúr an chomhaid .ipa
Léiríonn an sampla seo a leanas struchtúr IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Is struchtúr ionsuite é an méid thuas chun iTunes agus App Store a aithint. De réir an struchtúir seo:
- Tá na sonraí app go léir san eolaire Pá-Ualach.
- Is íomhá PNG 512 × 512 picteilín é comhad Artwork iTunes, ina bhfuil íocón na haipe le taispeáint in iTunes agus an aip App Store ar an iPad.
- Tá píosaí éagsúla faisnéise sa iTunesMetadata.plist, ó ainm agus ID an fhorbróra, an fhaisnéis chóipchirt, aitheantóir cuachta, ainm an aip, seánra, dáta eisiúna, dáta ceannaigh, etc.
- Níl san fhillteán META-INF ach meiteashonraí faoin gclár a úsáideadh chun an IPA a chruthú.


## Tagairtí 

* [.ipa - le Vicipéid](https://ga.wikipedia.org/wiki/.ipa)



