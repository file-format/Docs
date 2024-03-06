{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"Saspiests audio video",
"Fails",
"Pagarinājums",
"Faila formāts",
"Multivides konteiners",
"XVId",
"DivX",
"Kodeki",
"Resursu apmaiņas faila formāts",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AVI faila formāts — audio video interleave fails",
  "description": "Uzziniet par AVI failu formātu un API, kas var izveidot un atvērt AVI failus.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-lvi"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir AVI fails? ##

**AVI** faila formāts ir audio video multivides konteinera faila formāts, ko ieviesa Microsoft. Tajā ir audio un video dati, kas izveidoti un saspiesti, izmantojot vairākus kodekus (kodētājus/dekodētājus), piemēram, **XVid** un **DivX**. Tā kā AVI satura kodēšanai var izmantot dažādus kodekus, izguves lietojumprogrammām, ti, AVI atskaņotājiem, vajadzētu tos atvērt tikai tad, ja tajās ir instalēti nepieciešamie kodeki, ar kuriem tika izveidots AVI saturs. Formāts pēc noklusējuma tiek atbalstīts visās **Microsoft Windows** platformās, kā arī gandrīz visās citās galvenajās platformās. Vairākas lietojumprogrammas un API nodrošina iespēju izveidot/saglabāt, lasīt un pārveidot AVI citos populāros formātos, piemēram, MP4, MOV, WMV utt.

## AVI faila formāts ##

Fails ar paplašinājumu .avi ir AVI fails. Tas ir resursu apmaiņas faila formāta (RIFF) apakšformāts. RIFF sakārto datus blokos vai gabalos, kas tiek identificēti ar FourCC tagu. AVI fails ir vienkārši viens gabals RIFF formāta failā.

Pirmajā apakšgabalā faila galveni identificē ar hdrl tagu; tā saturs ietver videoklipa platumu, augstumu un kadru ātrumu. Otrajā apakšdaļā kustības tags apzīmē videoklipa kadru ātrumu. AVI video šajā daļā veido faktiskie audio/vizuālie dati. Ir arī trešais neobligāts apakšgabals ar tagu idx1, kas norāda failam piederošo atsevišķu datu gabalu atrašanās vietu failā.

### Ierobežojumi ###

* Informācija par malu attiecību nevar tikt kodēta sākotnējā AVI specifikācijā, lai gan jaunākā OpenDML specifikācija (AVI 2.0) piedāvā standartizētu metodi.

* Lai gan AVI faili tiek plaši izmantoti filmu un televīzijas pēcapstrādē, dažādas pieejas laika koda pievienošanai tiem konkurē, ietekmējot formāta lietojamību.

* Video failā, kas kodēts AVI formātā, nevar izmantot saspiešanas paņēmienu, kas prasa turpmākos kadru datus ārpus kodējamā kadra (B kadrs).

* Ir problemātiski izmantot AVI failus ar mainīgu bitu pārraides ātrumu (VBR) (piemēram, MP3 audio ar izlases frekvenci zem 32 kHz)

* AVI fails, kas kodē standarta izšķirtspējas mākslas filmas, kā parasti tiek izmantots, atkarībā no faila izmantošanas veida, visticamāk, radīs aptuveni 5 MB stundā.

* Subtitri ir jāiekodē video straumē vai jāizplata atsevišķā failā, ja AVI failos nevar ievietot pielikumus, piemēram, fontus un subtitrus.


## Īsa vēsture ##

AVI ieviesa Microsoft 1992. gadā ar mērķi nodrošināt spēcīgāku un modernāku audio un video failu formātu. Formāts ātri kļuva populārs, izmantojot internetu, ļaujot personām tieši un netieši koplietot video failus, izmantojot mākoņa multivides krātuvi.

## Atsauces Nr.

* [AVI — Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


