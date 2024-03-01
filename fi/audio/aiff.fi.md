{
  "date": "2021-04-26",
  "keywords": [
"aiff",
"tiedosto",
"laajennus",
"muoto",
"äänenvaihdon tiedostomuoto",
"musiikkia",
"aiff-tiedostomuoto",
"aiff mp3:lle",
"aiff vs wav",
"muuntaa aiff mp3-muotoon"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi AIFF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata AIFF-tiedostoja.",
  "title": "AIFF - Audio Interchange File Format",
  "linktitle": "AIFF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aif-fif"
}
},
  "lastmod": "2021-04-26"
}

## Mikä on AIFF-tiedosto?
AIFF (Audio Interchange File Format) on pakkaamaton äänitiedostomuoto, jonka Apple on kehittänyt vuonna 1998, mutta se perustuu **EA IFF 85** -standardiin (Electronic Artsin kehittämä standardi Interchange Format Files -tiedostoille), Amiga-järjestelmissä käytettävään kääremuotoon. . Tämä tiedostomuoto sisältää standardin näyteäänien tallentamista varten. Formaatti on riittävän hyvä joustavuuden suhteen ja mahdollistaa mono- tai monikanavaisten näytteistysäänien tallentamisen eri näytteenottotaajuuksilla ja -leveyksillä. Koska AIFF-tiedostot ovat pakkaamattomia, tämä tekee niistä suurempia kuin muut häviölliset tiedostot, kuten [MP3](/audio/mp3/).

AIFF-tiedostot sisältävät 2 kanavaa pakkaamatonta stereoääntä 16-bittisellä näytekoolla, tallennettuna taajuudella 44,1 khz. Korkean äänenlaadun vuoksi 5 minuutin ääni voi viedä jopa 50 Mt levytilaa, mikä on samanlainen kuin [WAV](/audio/wav/)-tiedostomuoto.

## AIFF vs WAV

AIFF ja WAV ovat laadultaan lähes samat. Molemmat käyttävät samaa PCM (pulse-code modulation) -koodausta, mikä tekee niistä kooltaan suurempia verrattuna muihin häviöllisiin muotoihin, kuten [MP3](/audio/mp3/), [M4A](/audio/m4a/). Jotkut yleisistä eroista on kirjoitettu alla olevaan taulukkoon:

|AIFF|WAV|
---|---|
|Käytetään enimmäkseen MACille|Käytetään enimmäkseen PC:ille|
|Sallii metatiedot| Ei salli metatietoa|

## AIFF-tiedostorakenne

**EA IFF 85** määrittää yleisen rakenteen tietojen tallentamiseksi tiedostoihin. **EA IFF 85** -tiedosto koostuu useista tietopaloista. AIFF-tiedoston rakennuslohko koostuu joistakin otsikkotiedoista, joita seuraa data:
{{< figure src="../chunk.png" alt="AIFF-pala" >}}

AIFF-tiedosto on kokoelma useita erityyppisiä paloja. On olemassa kaksi yleistä osien tyyppiä, jotka ovat tärkeitä AIFF-tiedostokappaleen muodostamiseksi:
- **Common Chunk**: Sisältää tärkeitä parametrejä, jotka kuvaavat näyteääntä, kuten sen pituuden ja näytteenottotaajuuden.
- **Sound Data Chunk**: Sisältää todelliset ääninäytteet.
On monia muita valinnaisia paloja, jotka luettelevat instrumenttiparametreja, määrittävät merkkejä, tallentavat sovelluskohtaisia tietoja jne.

### Paikalliset palatyypit

AIFF:n muodostavat palatyypit on annettu alla olevassa taulukossa:

|Pakkatyyppi| Kuvaus|
---|---|
|Common Chunk|Common Chunk kuvaa näytteistetyn äänen perusparametrit|
|Sound Data Chunk|Äänitietokappale sisältää todelliset näytekehykset|
|Marker Chunk|Marker Chunk sisältää merkkejä, jotka osoittavat paikkoihin äänidatassa|
|Instrument Chunk|Instrument Chunk määrittelee perusparametrit, joita instrumentti, kuten sampleri, voi käyttää äänidatan toistamiseen|
|MIDI Data Chunk|MIDI Data Chunkia voidaan käyttää MIDI-tietojen tallentamiseen|
|Äänitallennusosio|Äänitallennusosio sisältää äänentallennuslaitteita koskevia tietoja|
|Sovelluskohtainen osio|Sovellusten valmistajat voivat käyttää sovelluskohtaista osaa mihin tahansa tarkoitukseen|
|Kommenttipala|Kommenttiosaa käytetään kommenttien tallentamiseen FORM AIFF|:iin
|Tekstipalat - nimi, tekijä, tekijänoikeus, huomautus| Kaikki ovat tekstipalstoja|

## Viitteet ##

* [Audio Interchange -tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


