{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4S fails — kas ir M4S fails?",
  "description": "Uzziniet par M4S failu formātu un API, kas var izveidot un atvērt M4S failus.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-lvs"
}
},
  "lastmod": "2022-07-18"
}

## Kas ir M4S fails?

M4S fails ir neliels videoklipa segments, kas tiek straumēts internetā, izmantojot **MPEG-DASH** straumēšanas paņēmienu. Tajā ir video segments bināro datu veidā. Saņēmēja lietojumprogramma (parasti tīmekļa pārlūkprogramma vai multivides atskaņotāji) atskaņo šos segmentus to saņemšanas secībā. Pirmais M4S segments tiek identificēts pēc tajā ietvertajiem inicializācijas datiem. **Kopsavilkumā** M4S faili ir nelieli atsevišķa faila multivides segmenti.

## M4S faila formāts

M4S faili ir balstīti uz [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Šos mazos liela faila segmentus var lejupielādēt neatkarīgi, izmantojot HTTP. Tādējādi, ja jums ir liels [MP4](/video/mp4/) filmas fails, to var straumēt, izmantojot MPEG-DASH (Dynamic Adaptive Streaming over HTTP) paņēmienu, segmentējot to kā M4S segmenta failus. Ja šis lielais filmas fails tiek lejupielādēts diskā kā M4S, tiek lejupielādēti vairāki M4S faili. Ja visi šie .m4s segmenti ir savienoti, tiek izveidots pilns atskaņojams fails. Multivides atskaņotāji nevar atskaņot failu, ja vien kopā ar failu nav pieejams arī pirmais inicializācijas segments.

## Par MPEG-DASH straumēšanu

MPEG-DASH izmanto adaptīvo bitu pārraides ātruma straumēšanas paņēmienu, kas ļauj straumēt augstas kvalitātes multivides saturu internetā. Tas tiek darīts, sadalot saturu mazos segmentos, kas tiek straumēti, izmantojot HTTP. Šādā veidā var straumēt lielus multivides failus, piemēram, filmas, aplādes vai sporta pasākuma tiešraidi. Šie segmenti ir kodēti ar dažādu bitu pārraides ātrumu. MPEG-DASH iespējotie multivides atskaņotāji automātiski atlasa segmentu ar lielāko bitu pārraides ātrumu, izmantojot bitu pārraides ātruma pielāgošanas algoritmu. Tas ļauj izvairīties no notikumu apstāšanās vai atkārtotas buferizācijas atskaņošanas laikā.

### Atvērtā koda API M4S failiem

Ir pieejamas atvērtā koda API, ko var izmantot M4S failu lasīšanai un konvertēšanai.

 * [libdash](https://github.com/bitmovin/libdash) — .NET API M4S failiem
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) — Javascript klients M4S failam
 * [Go Library for Create Dash Files](https://github.com/zencoder/go-dash)

### Atvērtā koda API, lai pārveidotu M4S uz MP4

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Atsauces ###

* [ISO bāzes multivides faila (ISOBMFF) formāts](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [Dinamiska adaptīvā straumēšana, izmantojot HTTP — MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


