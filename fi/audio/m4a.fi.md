{
  "date": "2021-04-26",
  "keywords": [
"m4a",
"mp3",
"tiedosto",
"laajennus",
"muoto",
"mikä on m4a-tiedostomuoto",
"musiikkia",
"m4a tiedostomuoto",
"M4A vs MP3",
"m4a-tiedostomuodon määrittely"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi M4A-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata M4A-tiedostoja.",
  "title": "M4A - MPEG-4-äänitiedosto",
  "linktitle": "M4A",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-fia"
}
},
  "lastmod": "2021-04-26"
}

## Mikä on M4A-tiedosto?

**M4A-tiedostomuoto** on äänitiedosto, joka on luotu käyttämällä AAC-tekniikkaa (Advanced Audio Coding), joka tunnetaan häviöllisenä pakkauksena. Sana M4A lyhennettynä MPEG 4 Audio. Näillä äänitiedostoilla on yleensä .m4a-tiedostotunniste. Tämä koskee erityisesti suojaamatonta sisältöä. Se voi tallentaa erityyppistä äänisisältöä, kuten äänikirjoja, kappaleita ja podcasteja. M4A on yleensä toteutettu edistyneempänä muotona kuin MP3, jota ei tyypillisesti ollut suunniteltu vain äänelle. Se on vain äänikerros MPEG 1 tai 2 -videotiedostoissa.

M4A-muoto on FairPlay Digital Rights Managementin salaama, sillä iTunes Storen kautta myydyt tiedostot käyttävät .m4p-laajennusta. Applen iPhonet käyttävät MPEG-4-ääntä soittoäänissään, mutta nämä äänitiedostot käyttävät .m4r-laajennusta.


## M4A vs MP3

Sekä M4A että [MP3](/audio/mp3/) ovat vain äänitiedostomuotoja.

**M4A**: Laadun ja koon suhteen parempi kuin MP3, kun se koodataan samalla bittinopeudella. .m4a-tiedostotunniste on niin yleinen, koska Apple on käyttänyt niitä iTunes Music Storessa. M4A on äänitiedosto, joka on pakattu MPEG-4-tekniikalla; algoritmi häviölliseen pakkaamiseen. Se liittyy pohjimmiltaan MPEG-4 Audio Layeriin, tiedostot, joiden tiedostopääte on .m4a, ovat MPEG-4-elokuvien äänikerros. Sen on tarkoitus ohittaa MP3 ja tulla uudeksi standardiksi äänenpakkauksessa. Se on monella tapaa hyvin lähellä MP3:a, mutta otettiin käyttöön paremman laadun vuoksi samassa tai jopa pienemmässä tiedostokoossa. M4A-muodon esitteli ensimmäisenä Apple. Muototyyppi on myös toteutettu Applen häviöttömänä Encoderina (ALE).

Siksi tällä hetkellä M4A ei voinut saada MP3:n valtavirtaa, koska äänimuoto ei ole vielä yleisesti toistettavissa. Se on jotenkin rajoitettu vain MacOS:iin, iPodiin ja muihin Applen tuotteisiin.

**Mp3**: Tunnetuin digitaalinen äänimuoto. Se oli myös yksi ensimmäisistä pakkausformaateista, ja siitä tuli erittäin suosittu musiikin ystävien keskuudessa. Sen valtavirran menestys on niin nopea, että tiedostotyyppiä voidaan toistaa yleisesti ja melkein millä tahansa, laitteistolla tai ohjelmistolla. Yleisesti ottaen M4A tuottaa paremman äänenlaadun, mutta monet väittävät, että olipa se totta tai ei, ääniero ei ole havaittavissa, ja olisi ajanhukkaa yrittää muuntaa MP3-tiedostoja M4A-tiedostoiksi. Lopulta muunnos vain saa sinut menettämään alkuperäisen äänenlaadun.

## M4A-tiedostomuodon määritys

M4A-tiedostot koostuvat peräkkäisistä paloista. Jokaisella palalla on 8-tavuinen otsikko ja se on jaettu seuraavasti:
- 4-tavuinen palakoko (big-endian, korkea tavu ensin)
- 4-tavuinen osatyyppi - yksi ennalta määritetyistä allekirjoituksista: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, leveä, lataus, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt , ssrc, PICT.

First chunk will be of type "ftype" and has a sub-type at offset 8. Alatyypin M4A on oltava M4A_, M4B-alatyypin on oltava M4B_ ja M4P-alatyypin on oltava M4P_.

Toistamalla paloja, kunnes tuntemattoman tyyppinen kappale havaitaan, se muodostaa M4A (MPEG-4 Audio) -tiedoston.

## Viitteet ##

* [MPEG-4, osa 14 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) muoto ja palautusesimerkki](https://www.file-recovery.com/m4a-signature-format.htm)


