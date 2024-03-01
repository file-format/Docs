{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"tiedosto",
"laajennus",
"muoto",
"äänen vaihdon tiedostomuoto",
"musiikkia"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WAV-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata WAV-tiedostoja.",
  "title": "WAV - Waveform Audio File Format",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-fiv"
}
},
  "lastmod": "2019-12-13"
}

## Mikä on WAV-tiedosto?

WAV, joka tunnetaan nimellä WAVE (Waveform Audio File Format), on osajoukko Microsoftin Resource Interchange File Format (RIFF) -spesifikaatiosta digitaalisten äänitiedostojen tallentamiseen. Muoto ei pakkaa bittivirtaa ja tallentaa äänitallenteet erilaisilla näytteenottotaajuuksilla ja bittinopeuksilla. Se on ollut ja on yksi ääni-CD-levyjen vakioformaateista. Wave-tiedostot ovat kooltaan suurempia verrattuna uusiin äänitiedostomuotoihin, kuten [MP3](/audio/mp3/), jotka käyttävät häviöllistä pakkausta pienentämään tiedostokokoa säilyttäen samalla äänenlaadun samana. WAV-tiedostoja voidaan kuitenkin pakata käyttämällä Audio Compression Manager (ACM) -koodekkeja. Saatavilla on useita sovellusliittymiä ja sovelluksia, jotka voivat muuntaa WAV-tiedostoja muihin suosittuihin äänitiedostomuotoihin.

**Tiesitkö?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WAV-tiedostomuoto ##

WAVE-tiedostomuoto, joka on osa Microsoftin RIFF-spesifikaatiota, alkaa tiedoston otsikolla, jota seuraa tietopalojen sarja. WAVE-tiedostossa on yksi WAVE-osa, joka koostuu kahdesta osasta:

* "fmt"-kappale - määrittää tietomuodon

* "data" -osa - sisältää todelliset näytetiedot


### WAV-tiedoston otsikko ###

WAV (RIFF) -tiedoston otsikko on 44 tavua pitkä ja sen muoto on seuraava:


|Positions|Näytearvo|Kuvaus
---|---|---|
|1 - 4|RIFF|Merkitsee tiedoston riff-tiedostoksi. Merkit ovat kukin 1 tavun pituisia.
|5 - 8|Tiedoston koko (kokonaisluku)|Koko tiedoston koko - 8 tavua, tavuina (32-bittinen kokonaisluku). Yleensä täytät tämän luomisen jälkeen.
|9 -12|WAVE|Tiedostotyypin otsikko. Meidän tarkoituksiinmme se on aina yhtä kuin WAVE.
|13-16|fmt |Muotoile palamerkki. Sisältää lopussa olevan nollan
|17-20|16|Muototietojen pituus yllä olevan luettelon mukaisesti
|21-22|1|Muotoilutyyppi (1 on PCM) - 2 tavun kokonaisluku
|23-24|2|Kanavien määrä - 2 tavun kokonaisluku
|25-28|44100|Näytteistysnopeus - 32 tavua kokonaisluku. Yleiset arvot ovat 44100 (CD), 48000 (DAT). Näytetaajuus = Näytteiden määrä sekunnissa tai hertsejä.
|29-32|176400|(Sample Rate * BitsPerSample * Kanavat) / 8.
|33-34|4|(BitsPerSample * Kanavat) / 8.1 - 8 bit mono2 - 8 bit stereo / 16 bit mono 4 - 16 bit stereo
|35-36|16|Bittejä näytettä kohti
|37-40|data|data-osan otsikko. Merkitsee dataosion alun.
|41-44|Tiedoston koko (data)|Tietoosion koko.
|Yllä on esimerkkiarvot 16-bittiselle stereolähteelle.

## Viitteet ##

* [WAV - Wikipedia](https://en.wikipedia.org/wiki/WAV)


