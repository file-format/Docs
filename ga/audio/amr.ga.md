{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"comhad",
"síneadh",
"formáid",
"cad is comhad amr ann",
"Ceol",
"formáid comhaid amr",
"comhad amr",
"Comhad amr a thiontú go mp3",
"imirt comhad amr"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid AMR agus APIanna ar féidir comhaid AMR a chruthú, a thiontú agus a oscailt.",
  "title": "AMR - Comhad Codc Il-Ráta Oiriúnaitheach",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-gar"
}
},
  "lastmod": "2021-04-29"
}

## Cad is comhad AMR ann?
Is formáid sonraí fuaime é an comhad a bhfuil síneadh .amr air a bhaineann le CODEC fuaime **Ilráta Oiriúnaitheach**; comhdhéanta de chód cainte caolbhanda ilráta a ionchódaíonn comharthaí caolbhanda ag ráta giotán 4.75-12.2 kbit/s le cáilíocht chainte dola ag tosú ag 7.4 kbit/s; úsáideann oiriúnú nasc a roghnú as ceann amháin de ocht ráta giotán éagsúla bunaithe.

## Formáid Chomhaid AMR
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. Úsáidtear formáid comhaid AMR freisin chun an fhuaim labhartha a stóráil trí úsáid a bhaint as codec fuaime **Ilráta Oiriúnaitheach** a úsáideann go leor fóin chliste chun óráidí taifeadta a stóráil.

### Struchtúr formáid comhaid
Is formáid fuaime é an AMR (Ilráta Oiriúnaitheach); a úsáidtear go forleathan i bhfeidhmchláir agus gléasanna soghluaiste éagsúla, go hiondúil i seinnteoir fuaime/thaifeadán nó i bhfeidhmchláir de chineál VoIP. Is féidir AMR a rangú tuilleadh mar:

1. AMR- NB( Caolbhanda )
2. AMR- WB( Leathanbhanda )

De ghnáth, tagraíonn AMR do AMR-NB. Tá an struchtúr seo a leanas ag formáid comhaid AMR:

Tá ceanntásc 6 bheart i ngach comhad AMR a aithníonn an comhad mar fhuaim AMR. Socraítear an ceanntásc seo i gcónaí:
- 0×23
- 0×21
- 0×41
- 0x4d
- 0×52
- 0x0A

De ghnáth bíonn sé seo níos cosúla thar gach comhad AMR-NB. Má tá an ceanntásc tar éis caighdeán, is dócha go bhfuil an comhad truaillithe agus níor chóir é a úsáid. cuimsíonn an comhad AMR líon iomlán frámaí pacáilte fuaime. Cumann na frámaí seo 20m fuaime an ceann. Is féidir gach fráma a ionchódú trí úsáid a bhaint as aon cheann de na modhanna bailí AMR-NB (0-7, 8 SID i mód DTX). Ós rud é gur féidir na frámaí a ionchódú ag rátaí giotán éagsúla, tugtar Ilráta Oiriúnaitheach (AMR) ar an modh tipiciúil seo.
#### modhanna AMR
Seo a leanas na modhanna AMR éagsúla agus na rátaí giotán comhfhreagracha:

|MÓD| RÁTAÍ GIOMLÁN|
---|---|
|0| AMR 4.75 - Ionchódaíonn sé ag 4.75kbit/s|
|1 | AMR 5.15 - Ionchódaíonn sé ag 5.15kbit/s|
|2 | AMR 5.9 - Ionchódaíonn sé ag 5.9kbit/s|
|3 | AMR 6.7 - Ionchódaíonn sé ag 6.7kbit/s|
|4 | AMR 7.4 - Ionchódaíonn sé ag 7.4kbit/s|
|5 | AMR 7.95 - Ionchódaíonn sé ag 7.95kbit/s|
|6 | AMR 10.2 - Ionchódaíonn sé ag 10.2kbit/s|
|7 | AMR 12.2 - Ionchódaíonn sé ag 12.2kbit/s|

Tugtar méid fráma na modhanna AMR i mbeart (lena n-áirítear beart an cheanntásca) thíos:

|CMR |MÓD |MÉID AN FHRÉIM(i mbearta)|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMB 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMB 6.7 |18|
|4 |AMB 7.4 |20|
|5 |AMR 7.95 |21|

## Tagairtí ##

* [Codaitheoir fuaime Ilráta Oiriúnaitheach - De réir Vicipéid]( https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [Formáid Pála-Ualaigh RTP agus Formáid Stórála Comhad le haghaidh codecs Fuaime AMR agus AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)


