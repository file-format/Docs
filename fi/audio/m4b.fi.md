{
  "date": "2021-06-09",
  "keywords": [
"m4b",
"mp3",
"tiedosto",
"laajennus",
"muoto",
"mikä on m4b-tiedostomuoto",
"musiikkia",
"m4b tiedostomuoto",
"M4b vs MP3",
"m4b-tiedostomuodon määrittely"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi M4B-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata M4B-tiedostoja.",
  "title": "M4B - MPEG-4 äänikirjan tiedostomuoto",
  "linktitle": "M4B",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-fib"
}
},
  "lastmod": "2021-06-09"
}

## Mikä on M4B-tiedosto?

Tiedosto, jonka laajennus on .m4b, on äänikirja, jota yleensä käyttävät Apple Books ja iTunes. Tässä muodossa käytetty ääni tallennetaan MPEG-4-muodossa ja pakataan AAC-koodauksella. M4B-tiedosto on hyvin samankaltainen kuin M4A, mutta se tukee äänikirjaan liittyviä ominaisuuksia, kuten kirjanmerkkejä ja luvun taukoja. M4B-tiedostot ovat saatavilla sekä DRM-yhteensopivana että DRM-vapaana versiona. DRM-salatut äänikirjat ovat yleensä maksullisia äänikirjoja iTunes Storesta. DRM-vapaa sen sijaan löytyy helposti Internetistä.

## M4B tiedostomuoto

Äänikirjatiedostot, jotka sisältävät metatietoja, kuvia, kirjanmerkkejä ja hyperlinkkejä, voidaan tallentaa .m4a-tunnisteella, mutta yleensä tallennuksen aikana käytetään .m4b-tunnistetta, vain sen määrittämiseksi, että tiedostolla on äänikirjatiedostomuoto. App käyttää M4B-tiedostojensa suojaamiseen Fairplay DRM:ää (Digital Rights Management). Joten iTunesista ladattuja tiedostoja voidaan toistaa vain valtuutetuilla laitteilla tai tietokoneilla.


## M4B vs M4A

Sekä M4B että [MP3](/audio/mp3/) ovat vain äänitiedostomuotoja.

**M4B**: Voittaa MP3:een verrattuna, jos ne koodaavat molemmat samalla bittinopeudella. M4B on äänikirjatiedosto, joka on pakattu AAC-koodauksella. Se liittyy periaatteessa MPEG-4 Audio Layeriin. M4b-laajennuksella varustetut tiedostot ovat MPEG-4-elokuvien äänikerros, mutta niissä on ylimääräisiä äänikirjaan liittyviä ominaisuuksia. Sen tavoitteena on ohittaa MP3 ja tulla uudeksi standardiksi äänenpakkauksessa. Se on monella tapaa hyvin lähellä MP3:a, mutta kehitetty parantamaan laatua samassa tai jopa pienemmässä tiedostokoossa. M4B-muodon esitteli ensimmäisenä Apple. Muototyyppi on myös toteutettu Applen häviöttömänä Encoderina (ALE).

Siksi tällä hetkellä M4B ei voinut saada MP3:n valtavirran menestystä, koska äänimuoto ei ole vielä yleisesti toistettavissa.

**Mp3**: Digitaalinen äänimuoto, joka on kaikille tuttu. Aivan ensimmäinen pakkausformaatti näyttämöllä, ja siitä tuli erittäin kuuluisa musiikin kuuntelijoiden keskuudessa. Sen valtavirran menestys on niin nopea, että tiedostotyyppiä voidaan toistaa yleisesti ja se on yhteensopiva melkein minkä tahansa, laitteiston tai ohjelmiston kanssa. Yleisesti ottaen M4A tuottaa paremman äänenlaadun, mutta monet väittävät, että olipa se totta tai ei, ääniero ei ole vertailukelpoinen, ja olisi ajanhukkaa yrittää muuntaa MP3-tiedostoja M4A-tiedostoiksi. Lopuksi muunnos vain saa sinut menettämään alkuperäisen äänenlaadun.

## M4B-tiedostomuodon määrittely

Kuten {{HYPERLINKKI}}, M4B-tiedostot koostuvat myös peräkkäisistä paloista. Jokaisella palalla on 8-tavuinen otsikko ja se on jaettu seuraavasti:
- 4-tavuinen palakoko (big-endian, korkea tavu ensin)
- 4-tavuinen osatyyppi - yksi ennalta määritetyistä allekirjoituksista: ftyp, mdat, moov, pnot, moof, udta, uuid, free, ctab, skip, jP2, wide, load, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT , scpt, ssrc.

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. M4B on määritelty alatyypillä, jonka on oltava M4B_.

Toistaa paloja, kunnes tuntemattoman tyyppinen kappale havaitaan, se muodostaa M4B (MPEG-4 Audio) -tiedoston.

## Viitteet

* [MPEG-4, osa 14 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) muoto ja palautusesimerkki](https://www.file-recovery.com/m4a-signature-format.htm)


