---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lthuilleamh faoi fhormáid comhaid M3U agus APIs is féidir a chruthú agus a oscailt comhad M3Us.
title: MFoirm Chomhaid 3Uat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Cad is comhad M3U ann? ##

Is comhad seinmliosta fuaime é M3U (URL MP3) atá stóráilte leis an síneadh .m3u. Ní comhad fuaime iarbhír é M3U, ní dhíríonn sé ach ar chomhaid fuaime agus uaireanta físeáin. Forbraíodh M3U le húsáid le bogearraí Winplay3 ag Fraunhofer. Tá sé tacaíocht freisin ag imreoirí na meáin éagsúla agus bogearraí.

## Formáid Comhaid M3U

Níl aon sonraíocht oifigiúil ann maidir le formáid comhaid M3U, is caighdeán de-facto é. Is comhad gnáth-théacs é M3U a úsáideann an síneadh .m3u má tá an téacs ionchódaithe in ionchódú réamhshocraithe neamh-Unicode an chórais áitiúil nó leis an iarmhír .m3u8 má tá an téacs ionchódaithe UTF-8. Is féidir le gach iontráil sa chomhad M3U a bheith mar cheann díobh seo a leanas:

- Conair Absalóideach chuig an gcomhad
- Conair an chomhaid i gcoibhneas leis an gcomhad M3U.
- URL

### M3U Breisithe ###

Sa M3U leathnaithe, tugtar isteach treoracha breise a thosaíonn le # agus a chríochnaíonn le colon(:) má tá paraiméadair acu. Anseo thíos tá liosta de na treoracha le haghaidh M3U sínte.

- **#EXTM3U** - Is é ceanntásc an chomhaid é a léiríonn M3U Breisithe agus ní mór é a bheith mar chéad líne an chomhaid.
- **#EXTENC:** - Ionchódú téacs. Caithfidh sé a bheith ar an 2ú líne den chomhad.
- **#EXTINF:** - Úsáidtear é le haghaidh faisnéise rianta agus airíonna breise eile.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Cuir tús le grúpáil ainmneacha
- **#EXTALB:** - Eolas faoin albam
- **#EXTART:** - Ealaíontóir albam
- **#EXTGENRE** - Seánra Albam
- **#EXTM3A** - Seinmliosta comhaid singil do rianta albam nó caibidlí.
- **#EXTBYT:** - Méid comhaid i mbearta.
- **#EXTBIN:** - Seo a leanas na sonraí dénártha.
- **#EXTIMG:** - Lógó, Clúdach nó íomhánna eile.

### HLS M3U ###

Chruthaigh Apple HLS (HTTP Live Streaming) chun fuaim agus raidió a shruthú chuig gléasanna iOS. Tá sé bunaithe ar an M3U sínte ionchódaithe UTF-8. Caighdeánaíodh é mar RFC 8216 in 2017 ag IETF. Tosaíonn na clibeanna don seinmliosta HLS le #EXT-X-. Tugtar thíos liosta clibeanna do HLS

- **EXT-X-VERSION** - Léiríonn sé an leagan comhoiriúnachta den chomhad bunaithe ar na meáin agus ar a fhreastalaí.
- **#EXT-X-START:** - Léiríonn sé an pointe tosaigh roghnaithe don seinnliosta.
- **#EXT-X-Playlist-CINEÁL:** - Soláthraíonn sé an cineál seinnliosta (IMEACHTAS nó VOD).
- **#EXT-X-TARGETDURATION:** - Sonraíonn sé ré uasta na Deighleog.
- **#EXT-X-MEDIA-SEquENCE:** - Léiríonn sé Uimhir Sheichimh na Meán.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Léiríonn sé go bhfuil gach sampla meán neamhspleách agus gur féidir iad a dhíchódú gan deighleoga eile.
- **#EXT-X-MEDIA:** - Úsáidtear é chun Seinmliostaí Meán ina bhfuil léirithe malartacha den ábhar céanna a chomhcheangal.
- **#EXT-X-STREAM-INF:** - Sonraíonn sé Sruth Athróg atá mar chuid de na Léirithe.
- **#EXT-X-BYTERANGE:** - Léiríonn sé gur fo-raon den acmhainn atá sainaitheanta ina URI í Deighleog na Meán.
- **#EXT-X-ISCONTINUITY** - Léiríonn sé neamhleanúnachas idir na codanna meán roimhe seo agus na codanna seo a leanas.
- **#EXT-X-DISCONTINUITY-SEquENCE:** - Ceadaíonn sé sioncrónú idir léirithe éagsúla den Sruth Athróg céanna nó Sruthanna Athraitheacha éagsúla.
- **#EXT-X-KEY:** - Sonraítear conas Deighleoga Meáin a dhíchriptiú.
- **#EXT-X-MAP:** - Sonraítear conas Rannóg Túsaithe na Meán a fháil. Ní mór na Deighleoga Meán infheidhme a pharsáil.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - Comhcheanglaíonn sé Raon Sonraí.
- **#EXT-XI-FRAMES-ONLY** - Léiríonn sé go ndéanann gach Deighleog Meán sa Seinmliosta cur síos ar fhráma I amháin.
- **EXT-XI-FRAME-STREAM-INF** - Léiríonn sé go bhfuil frámaí I de chur i láthair Ilmheán sa chomhad seinmliosta.
- **#EXT-X-SESSION-DATA:** - Ceadaíonn sé sonraí seisiúin treallach a bheith
iompar i Máistir Seinmliosta.
- **#EXT-X-SESSION-KEY:** - Ceadaíonn sé eochracha criptithe. Is féidir leis an gcliant na heochracha seo a réamhlódáil gan an seinmliosta a léamh ar dtús.
- **#EXT-X-ENDLIST** - Tugann sé le fios nach gcuirfear a thuilleadh Deighleoga Meáin leis an gcomhad.

Seo a leanas liosta de na cineálacha meán Idirlín a úsáideann M3U:

- **app/vnd.apple.mpegurl**: Is é an t-aon chineál meán cláraithe (cláraithe in 2009) le haghaidh M3U a úsáidtear chun tagairt a dhéanamh do na seinmliostaí in feidhmchláir HLS.
- Úsáideann feidhmchláir neamh-HLS na cineálacha meán Idirlín seo a leanas.
  - "**iarratas/mpegurl**"
  - "**iarratas/x-mpegurl**"
  - "**fuaime/mpegurl**"
  - "**fuaime/x- mpegurl**"

## Sampla M3U ##

Is sampla é seo den chomhad M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Tagairtí ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

