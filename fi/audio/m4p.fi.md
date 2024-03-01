{
  "date": "2021-06-09",
  "keywords": [
"m4p",
"mp3",
"tiedosto",
"laajennus",
"muoto",
"mikä on m4p-tiedostomuoto",
"musiikkia",
"m4p tiedostomuoto",
"M4b vs MP3",
"m4p-tiedostomuodon määrittely"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi M4P-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata M4P-tiedostoja.",
  "title": "M4P - MPEG-4 äänikirjan tiedostomuoto",
  "linktitle": "M4P",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-fip"
}
},
  "lastmod": "2021-06-09"
}

## Mikä on M4P-tiedosto?
Tiedosto, jonka laajennus on .m4p, on äänitiedosto, joka on yleensä ladattavissa Apple iTunes Storesta. Toisin sanoen voimme sanoa, että M4P on AAC-tiedosto, mutta kopiosuojattu käyttämällä digitaalista oikeuksien hallintaa (DRM). Se tarkoittaa, että M4P-tiedostoja voidaan toistaa vain valtuutetuissa järjestelmissä tai laitteissa. Yleensä M4P-tiedostot ovat Applen multimedialaitteita koskevia. Näitä tiedostoja voi siis toistaa vain Applen macbookeissa, podcasteissa ja älypuhelimissa, kuten iPhone 6 tai iPhone 7.

## M4P tiedostomuoto
M4P tulee sanoista MPEG 4 Protected (audio), ja se koodaa äänen edistyneellä audiokoodekilla (AAC) ja suojaa tiedostoa tiedoston luvattomalta käytöltä. Tätä tiedostomuotoa pidetään yleensä iTunes Music Storen äänitiedostomuotona. Apple käyttää FairPlay Digital Rights Management (DRM) -järjestelmää M4P-tiedostojen suojaamiseen. FairPlay DRM perustuu Veridiscin kehittämään teknologiaan. Sen suojausmekanismi toimii salaamalla AAC-äänivirran AES-salauksella. Käyttäjä saa pääavaimen, joka on määritetty hänen tililleen salauksen purkamista varten. Tämä tiedostomuoto otettiin käyttöön MP3-tiedostomuodon korvaajana, koska MP3:a ei alun perin ollut tarkoitettu äänitiedostoksi, vaan kerrokseksi III MPEG 1- tai 2-videotiedostossa.


## M4P-tiedostomuodon tekniset tiedot

Samoin kuin {{HYPERLINKKI}}, M4P-tiedostot koostuvat myös peräkkäisistä paloista. Jokaisella palalla on 8-tavuinen otsikko ja se on jaettu seuraavasti:
- 4-tavuinen palakoko (big-endian, korkea tavu ensin)
- 4-tavuinen osatyyppi - yksi ennalta määritetyistä allekirjoituksista: mdat, moov, pnot, moof, udta, uuid, free, skip, ftyp, jP2, leveä, lataus, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT, scpt , ctab, ssrc.

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. M4P on määritetty alatyypin mukaan, jonka on oltava M4P_.

Toistamalla paloja, kunnes tuntemattoman tyyppinen kappale havaitaan, se muodostaa M4P (MPEG-4 Audio) -tiedoston.

## Viitteet ##

* [MPEG-4, osa 14 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) muoto ja palautusesimerkki](https://www.file-recovery.com/m4a-signature-format.htm)


