{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"tiedosto",
"laajennus",
"muoto",
"mikä on amr-tiedosto",
"musiikkia",
"amr tiedostomuoto",
"amr tiedosto",
"Muunna amr-tiedosto mp3-muotoon",
"toistaa amr-tiedostoa"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi AMR-tiedostomuodosta ja API-liittymistä, jotka voivat luoda, muuntaa ja avata AMR-tiedostoja.",
  "title": "AMR - Adaptive Multi-Rate Codec File",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-fir"
}
},
  "lastmod": "2021-04-29"
}

## Mikä on AMR-tiedosto?
Tiedosto, jonka laajennus on .amr, on **Adaptive Multi-Rate** -äänikoodekille relevantti äänidatamuoto; koostuu moninopeuksisesta kapeakaistaisesta puhekoodekista, joka koodaa kapeakaistaisia signaaleja bittinopeudella 4,75-12,2 kbit/s maksullisen puheen nopeudella alkaen 7,4 kbit/s; käyttää linkin mukauttamista valitakseen yhden kahdeksasta erilaisesta bittinopeudesta.

## AMR-tiedostomuoto
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR-tiedostomuotoa käytetään myös puhutun äänen tallentamiseen käyttämällä **Adaptive Multi-Rate** -äänikoodekkia, jota monet älypuhelimet käyttävät tallennettujen puheiden tallentamiseen.

### Tiedostomuotorakenne
AMR (Adaptive Multi-Rate) on äänimuoto; käytetään laajalti erilaisissa mobiilisovelluksissa ja laitteissa, tyypillisesti soittimissa/tallentimissa tai VoIP-tyyppisissä sovelluksissa. AMR voidaan luokitella edelleen seuraavasti:

1. AMR-NB (kapeakaistainen)
2. AMR-WB (laajakaista)

Yleensä AMR tarkoittaa AMR-NB:tä. AMR-tiedostomuodolla on seuraava rakenne:

Jokainen AMR-tiedosto sisältää 6-tavun otsikon, joka tunnistaa tiedoston AMR-ääneksi. Tämä otsikko on aina asetettu seuraavasti:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Tämä on yleensä samanlainen kaikissa AMR-NB-tiedostoissa. Jos otsikko noudattaa standardia, on todennäköistä, että tiedosto on vioittunut, eikä sitä tule käyttää. AMR-tiedosto koostuu kokonaisesta määrästä pakattuja äänikehyksiä. Nämä kehykset säveltävät kukin 20 ms ääntä. Jokainen kehys voidaan koodata käyttämällä mitä tahansa kelvollista AMR-NB-moodia (0-7, 8 SID DTX-tilassa). Koska kehykset voidaan koodata eri bittinopeuksilla, tätä tyypillistä menetelmää kutsutaan Adaptive Multi-Rate (AMR) -menetelmäksi.
#### AMR-tilat
Seuraavassa on eri AMR-tilat ja niitä vastaavat bittinopeudet:

|TILA| BITTINOPEAT|
---|---|
|0| AMR 4,75 - Koodaa nopeudella 4,75 kbit/s|
|1 | AMR 5.15 - Koodaa nopeudella 5,15 kbit/s|
|2 | AMR 5.9 - Koodaa nopeudella 5,9 kbit/s|
|3 | AMR 6.7 - Koodaa nopeudella 6,7 kbit/s|
|4 | AMR 7.4 - Koodaa nopeudella 7,4 kbit/s|
|5 | AMR 7,95 - Koodaa nopeudella 7,95 kbit/s|
|6 | AMR 10.2 - Koodaa nopeudella 10,2 kbit/s|
|7 | AMR 12.2 - Koodaa nopeudella 12,2 kbit/s|

AMR-tilojen kehyskoko tavuina (mukaan lukien otsikkotavu) on annettu alla:

|CMR |TILA |KEHYKSEN KOKO(tavuina )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5,15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Viitteet ##

* [Adaptive Multi-Rate audiokoodekki – Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [RTP-hyötykuormamuoto ja tiedostojen tallennusmuoto AMR- ja AMR-WB-äänikoodekkeille](https://tools.ietf.org/html/rfc4867#page-35)


