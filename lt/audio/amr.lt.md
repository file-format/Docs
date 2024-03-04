{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"failą",
"pratęsimas",
"formatu",
"kas yra amr failas",
"muzika",
"amr failo formatas",
"amr failą",
"Konvertuoti amr failą į mp3",
"paleisti amr failą"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie AMR failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti AMR failus.",
  "title": "AMR – prisitaikantis kelių spartų kodeko failas",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-ltr"
}
},
  "lastmod": "2021-04-29"
}

## Kas yra AMR failas?
Failas su plėtiniu .amr yra garso duomenų formatas, susijęs su **Adaptive Multi-Rate** garso kodeku; susideda iš kelių spartų siaurajuosčio kalbos kodeko, kuris koduoja siaurajuosčius signalus 4,75–12,2 kbit/s bitų sparta, o mokamos kokybės kalba prasideda nuo 7,4 kbit/s; naudoja nuorodų pritaikymą, kad pasirinktų vieną iš aštuonių skirtingų bitų spartų.

## AMR failo formatas
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR failo formatas taip pat naudojamas sakytiniam garsui saugoti naudojant **Adaptive Multi-Rate** garso kodeką, kurį daugelis išmaniųjų telefonų naudoja įrašytoms kalboms saugoti.

### Failo formato struktūra
AMR (Adaptive Multi-Rate) yra garso formatas; plačiai naudojamas įvairiose mobiliosiose programose ir įrenginiuose, paprastai garso grotuvuose / įrašymo įrenginiuose arba VoIP programose. AMR galima toliau klasifikuoti kaip:

1. AMR-NB (siaurajuostė)
2. AMR-WB (plačiajuostis)

Paprastai AMR reiškia AMR-NB. AMR failo formatas turi tokią struktūrą:

Kiekviename AMR faile yra 6 baitų antraštė, kuri atpažįsta failą kaip AMR garso įrašą. Ši antraštė visada nustatoma taip:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Paprastai tai yra panašu į visus AMR-NB failus. Jei antraštė atitinka standartą, tikėtina, kad failas yra sugadintas ir neturėtų būti naudojamas. AMR failą sudaro visas supakuotų garso kadrų skaičius. Kiekvienas iš šių kadrų sudaro 20 ms garso. Kiekvienas kadras gali būti užkoduotas naudojant bet kurį iš galiojančių AMR-NB režimų (0-7, 8 SID DTX režimu). Kadangi kadrai gali būti koduojami skirtingu bitų dažniu, šis tipinis metodas vadinamas adaptyviuoju kelių spartų (AMR).
#### AMR režimai
Toliau pateikiami skirtingi AMR režimai ir atitinkami bitų dažniai:

|REŽIMAS| BITŲ RATAI|
---|---|
|0| AMR 4.75 – koduoja 4.75 kbit/s|
|1 | AMR 5.15 – koduoja 5.15 kbit/s|
|2 | AMR 5.9 – koduoja 5.9 kbit/s|
|3 | AMR 6.7 – koduoja 6.7kbit/s|
|4 | AMR 7.4 – koduoja 7,4 kbit/s|
|5 | AMR 7.95 – koduoja 7.95 kbit/s|
|6 | AMR 10.2 – koduoja 10.2kbit/s|
|7 | AMR 12.2 – koduoja 12,2 kbit/s|

AMR režimų kadro dydis baitais (įskaitant antraštės baitą) pateiktas toliau:

|CMR |REŽIMAS |KADRO DYDIS (baitais )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Nuorodos Nr.

* [Adaptive Multi-Rate garso kodekas – Vikipedijos](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [RTP naudingosios apkrovos formatas ir failų saugojimo formatas, skirtas AMR ir AMR-WB garso kodekams](https://tools.ietf.org/html/rfc4867#page-35)


