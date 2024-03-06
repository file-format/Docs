{
  "date": "2021-03-12",
  "keywords": [
"VP9",
"Fails",
"Pagarinājums",
"Faila formāts",
"Video formāts",
"TrueMotion video",
"VPX",
"On2 tehnoloģijas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP9 — TrueMotion video fails",
  "description": "Uzziniet par VP9 faila formātu un API, kas var izveidot un atvērt VP9 failus.",
  "linktitle": "VP9",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-lv9"
}
},
  "lastmod": "2021-03-27"
}

## Kas ir VP9 fails?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. Sākotnēji tas tika izstrādāts, lai saspiestu ultra HD saturu pakalpojumā YouTube, jo tas paplašina un uzlabo tā priekšgājēja kodēšanas efektivitāti. Ja mēs runājam par oriģinālajiem VPX kodekiem, tie nāk no On2 Technologies, ko Google asimilēja 2010. gadā. Vēlāk Google kodeku ieguva ar atvērtā koda avotu. Abi formāti VP8 un VP9 ir pieejami ar bezmaksas BSD licenci, kas ļauj operatoriem organizēt šifrēšanas vai atšifrēšanas prasmes gan ekskluzīvajā programmatūrā, gan atvērtā pirmkoda programmatūrā, neatklājot to pirmkodu.

## VP9 tehniskās īpašības

* VP9 nodrošina maksimālo izšķirtspēju 8192x4352 ar ātrumu līdz 120 kadriem sekundē un vairākas krāsu telpas ar Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 un sRGB
* Šis formāts pilnībā atbalsta visu tīmekļa un mobilo ierīču lietošanas gadījumu klāstu no zema bitu pārraides ātruma saspiešanas līdz augstas kvalitātes ultra-HD ar papildu atbalstu 10/12 bitu kodēšanai un HDR.
* Tas var samazināt video bitu pārraides ātrumu pat par 50%, salīdzinot ar citiem
* Tas ir sagatavots adaptīvai straumēšanai, un to izmanto YouTube un citi labi zināmi tīmekļa video nodrošinātāji
* Chrome, Opera, Edge, Firefox un Android ierīces, kā arī miljoniem viedo televizoru atbalsta šī kodeka dekodēšanu.
* Video izšķirtspēja, kas lielāka par 1080p, tiek pārveidota, izmantojot VP9, un nodrošina bezzudumu saspiešanu
* Dažādas krāsu telpas, piemēram, Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 un sRGB atbalsta VP9
* VP9 var atbalstīt arī HDR video, izmantojot Hybrid Log-Gamma un Perceptual Quantizer


## Īsa vēsture

 *  VP9 video kodeku izstrāde tika uzsākta 2011. gadā, un tā dekodētājs tika pievienots Chromium tīmekļa pārlūkprogrammai 2012. gada decembrī.
 *  Tā pirmā tīmekļa pārlūkprogrammas Google Chrome versija tika izlaista 2013. gada februārī, un tajā laikā tika izlaista dekodēšana
 *  Google izlaida Chrome 29.0.1547 ar VP9 galīgo atbalstu 2013. gada augustā
 *  2013. gada oktobrī pakalpojumam FFmpeg tika pievienots instinktīvs VP9 dekodētājs
 *  Mozilla 2013. gada decembrī ir pievienojusi VP9 uzturlīdzekļus Firefox 2. versijā, kas pēc tam tika izlaista 2014. gada 18. martā.
 
## VP9 darbība

Parasti 4K video uzlabo attēla kvalitāti, samazinot noteiktus pikseļus, bet VP9 kodekis un HEVC padara tos lielākus, lai samazinātu bitu pārraides ātrumu un faila lielumu. Lai gan tas varētu šķist pretrunīgi, kodēšanas programma ņem lielākus pikseļus un maina tos uz labāku izšķirtspējas produktivitāti. Avota video, kas ietver video kadrus, tiek kodēts vai saspiests, lai izveidotu saspiestu video bitu straumi. Katrs atsevišķs kadrs vispirms tiek sadalīts pikseļu blokos. Pēc tam bloki tiek rūpīgi pārbaudīti, lai noteiktu trīsdimensiju atlaišanu, un tiek novērtēti secīgi savienojumi starp kadriem, lai izmantotu jomas, kuras nevar mainīt. Tie tiek kodēti, izmantojot kustības vektorus, kas nodrošina dotā bloka īpašības nākamajā kadrā. Atlikusī informācija tiek kodēta, izmantojot efektīvu bināro saspiešanu.

## Atsauces

 * [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Kokosrieksts](https://www.coconut.co/)

