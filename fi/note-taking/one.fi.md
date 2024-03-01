{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONE - Microsoft OneNote -tiedostomuoto",
  "description": "Opi ONE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata YKSI tiedostoja.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-fie"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on .ONE-tiedosto? ##

.ONE-laajennuksella kuvatut tiedostot on luotu Microsoft OneNote -sovelluksella. OneNoten avulla voit kerätä tietoja sovelluksen avulla aivan kuin käyttäisit muistiinpanojen tekemiseen luonnoslehteä. OneNote-tiedostot voivat sisältää erilaisia elementtejä, jotka voidaan sijoittaa ei-kiinteisiin paikkoihin asiakirjasivuilla. Nämä elementit voivat sisältää tekstiä, digitoitua käsialaa ja muista sovelluksista kopioituja objekteja, kuten kuvia, piirustuksia ja multimedialeikkeitä (ääni/video). Microsoft tarjoaa nyt OneNoten online-version osana Office365:tä, jossa Notes voidaan jakaa muiden OneNote-käyttäjien kanssa Internetin kautta.

## .ONE tiedostomuodon tekniset tiedot ##

OneNote-tiedostomuoto tarjoaa tehokkaan tavan esittää digitaalisia muistiinpanoja hierarkkisina osioiden ja sivujen ryhminä. Jokainen sivu sisältää käyttäjän määrittämää sisältöä tietyssä rakenteessa, joka esitetään tiedostomuodossa Document Object Model (DOM). Tämän muodon tietomalli on alla olevan kuvan mukainen.

### Rakenteen yleiskatsaus ###

OneNote-tiedostomuodon tietomallin mukaisesti OneNote-asiakirja koostuu eri elementeistä.

#### Osio ####

Osio on OneNote-tiedoston ylin säilö, joka sisältää lisäksi erilaisia elementtejä, kuten:

* Sivut

* Metatiedot

* Ominaisuudet


Metatiedot ja ominaisuudet sisältävät osion nimen, osion sisältämien sivujen tunnisteen ja sivujen näyttöjärjestyksen. Termi osio viittaa kaikkiin osiossa oleviin sivuihin ja näiden tietojen esitykseen OneNote®-versiovarastotiedostossa, jonka tiedostotunniste on .one.

#### Sivu ####

OneNote-asiakirjan käyttäjän määrittämä sisältö sisältyy sivun sisään. Sivun tiedot sisältävät tekstiä, luetteloita, taulukoita, sivujen otsikoita, kuvia ja huomautustunnisteita. Sivu koostuu ääriviivaobjekteista, joihin on lisätty suurin osa sisältämistä objekteista. Jokaiselle sivulle voidaan antaa nimi mielekkäälle esitykselle ja myös objekteja voidaan lisätä suoraan sivuille. Sivu voi lisäksi sisältää alisivuja hierarkkisessa järjestelmässä.

#### Ominaisuudet ja ominaisuussarjat ####

OneNoten sisältö koostuu ominaisuuksista, ominaisuusjoukoista ja tiedostotieto-objekteista. Ominaisuusjoukko on kokoelma ominaisuuksia, jotka edustavat tietyntyyppistä sisältöä. Tiedostotietoobjekti on binääritietolohko, joka sisältää kuvia, upotettuja tiedostoja tai ääni-/videosisältöä.

#### OneNote-muistikirja ####

Muistikirja on kokoelma osatiedostoja, jotka on tallennettu samaan hakemistoon. Ominaisuuksien kokoelmaa käytetään määrittämään asetuksia, kuten muistikirjan osien järjestystä ja muistikirjan väriä.

### Tiedostorakenne ###

Versiomuistitiedoston TÄYTYY alkaa **Header**-rakenteella. Loput tiedostosta jaetaan tavulohkoihin, joissa kunkin lohkon koko ja rakenne määritellään siihen viittaavassa kentässä. Lohko on tavoitettavissa, jos siihen viitataan **Otsikko**-rakenteella tai jos siihen viittaa kenttä toisessa saavutettavassa lohkossa. **Otsikko**-rakenteen ulkopuoliset tiedot ja kaikki tavoitettavissa olevat lohkot TÄYTYY jättää huomiotta.

Kaikki rakenteet on kohdistettu 1-tavun rajoilla. Kaikki kokonaisluvut on allekirjoitettu, ellei toisin mainita. Kaikki kentät ovat [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), ellei toisin mainita.

#### Otsikko ####

ONE-tiedoston otsikko koostuu paloista, jotka sisältävät erilaisia yksilöllisiä tunnuksia ja kenttiä tiedostotietojen esittämiseksi seuraavasti:

`guidFileType (16 tavua): GUID, joka määrittää versiovarastotiedoston tyypin. TÄYTYY olla jokin seuraavan taulukon arvoista.


|Tiedostomuoto|Arvo
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 tavua):` GUID, joka määrittää tämän versiovarastotiedoston identiteetin. PITÄÄ olla maailmanlaajuisesti ainutlaatuinen.

`guidLegacyFileVersion (16 tavua):` TÄYTYY olla {00000000-0000-0000-0000-000000000000} ja TÄYTYY jättää huomiotta.

`guidFileFormat (16 tavua):` GUID, joka määrittää, että tiedosto on versiovarastotiedosto. TÄYTYY olla {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

`ffvLastCodeThatWroteToThisFile (4 tavua):` Etumerkitön kokonaisluku. TÄYTYY olla jokin seuraavan taulukon arvoista tiedostotyypistä riippuen.

|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 tavua):` Etumerkitön kokonaisluku. TÄYTYY olla jokin seuraavan taulukon arvoista riippuen tämän tiedoston tiedostomuodosta.


|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 tavua):` Etumerkitön kokonaisluku. TÄYTYY olla jokin seuraavan taulukon arvoista riippuen tämän tiedoston tiedostomuodosta.

|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 tavua):` Etumerkitön kokonaisluku. TÄYTYY olla jokin seuraavan taulukon arvoista riippuen tämän tiedoston tiedostomuodosta.

|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 tavua):` **FileChunkReference32**-rakenne, jonka TÄYTYY olla arvo fcrZero.

`fcrLegacyTransactionLog (8 tavua):` **FileChunkReference32**-rakenne, jonka TÄYTYY olla fcrNil.

`cTransactionsInLog (4 tavua):` Etumerkitön kokonaisluku, joka määrittää tapahtumien määrän tapahtumalokissa. EI SAA olla nolla.

`cbLegacyExpectedFileLength (4 tavua):` Etumerkitön kokonaisluku, jonka TÄYTYY olla nolla ja TÄYTYY jättää huomiotta.

`rgbPlaceholder (8 tavua):` Etumerkitön kokonaisluku, jonka TÄYTYY olla nolla ja TÄYTYY jättää huomiotta.

`fcrLegacyFileNodeListRoot (8 tavua):` **FileChunkReference32**-rakenne, jonka TÄYTYY olla fcrNil.

`cbLegacyFreeSpaceInFreeChunkList (4 tavua):` Etumerkitön kokonaisluku, jonka TÄYTYY olla nolla ja TÄYTYY jättää huomiotta.

`fNeedsDefrag (1 tavu):` TÄYTYY jättää huomiotta.

`fRepairedFile (1 tavu):` TÄYTYY jättää huomiotta.

`fNeedsGarbageCollect (1 tavu):' TÄYTYY jättää huomiotta.

`fHasNoEmbeddedFileObjects (1 tavu):` Etumerkitön kokonaisluku, jonka TÄYTYY olla nolla ja joka TÄYTYY jättää huomiotta.

`guidAncestor (16 tavua):` GUID, joka määrittää sisällysluettelotiedoston **Header.guidFile**-kentän seuraavan taulukon mukaan:


|Sisällysluettelotiedostomuoto|Sisällysluettelotiedoston sijainti
--- | --- |
|Osatiedosto - .One|Sisällysluettelotiedosto sijaitsee samassa hakemistossa kuin tämä tiedosto.
|Sisällysluettelotiedosto - .onetoc2|Sisällysluettelotiedosto sijaitsee tämän tiedoston päähakemistossa.

Jos GUID on 00000000-0000-0000-0000-000000000000}, tämä kenttä ei viittaa sisällysluettelotiedostoon.

`crcName (4 tavua):` Etumerkitön kokonaisluku, joka määrittää tämän versiovaraston tiedoston nimen CRC-arvon. Nimi on tiedostonimen Unicode-esitys, jonka pääte ja lopussa on ylimääräinen nollamerkki. Tämä CRC lasketaan aina käyttämällä CRC-algoritmia .one-tiedostolle, riippumatta tästä versiovaraston tiedostomuodosta.

`fcrHashedChunkList (12 tavua):` **FileChunkReference64x32**-rakenne, joka määrittää viittauksen tiivistetyn osaluettelon ensimmäiseen **FileNodeListFragment**-tiedostoon. Jos **FileChunkReference64x32**-rakenteen arvo on fcrZero tai fcrNil, tiivistettyä osaluetteloa ei ole olemassa.

`fcrTransactionLog (12 tavua): **FileChunkReference64x32**-rakenne, joka määrittää viittauksen tapahtumalokin ensimmäiseen **TransactionLogFragment**-rakenteeseen. **fcrTransactionLog**-kentän arvo EI SAA olla fcrZero eikä fcrNil.

`fcrFileNodeListRoot (12 tavua): **FileChunkReference64x32**-rakenne, joka määrittää viittauksen juuritiedoston solmuluetteloon. Kentän **fcrFileNodeListRoot** arvo EI SAA olla fcrZero eikä fcrNil.

`fcrFreeChunkList (12 tavua): **FileChunkReference64x32**-rakenne, joka määrittää viittauksen ensimmäiseen **FreeChunkListFragment**-rakenteeseen. Jos **FileChunkReference64x32**-rakenteen arvo on fcrZero tai fcrNil, ilmaista osaluetteloa ei ole olemassa.

`cbExpectedFileLength (8 tavua):` Etumerkitön kokonaisluku, joka määrittää tämän versiovaraston tiedoston koon tavuina.

`cbFreeSpaceInFreeChunkList (8 tavua):` Etumerkitön kokonaisluku, jonka PITÄISI määrittää vapaan kappaleluettelon määrittämän vapaan tilan koko tavuina.

`guidFileVersion (16 tavua): GUID. Kun joko **cTransactionsInLog**- tai **guidDenyReadFileVersion**-kentän arvoa muutetaan, **guidFileVersion** TÄYTYY muuttaa uudeksi GUID-tunnukseksi.

`nFileVersionGeneration (8 tavua):` Etumerkitön kokonaisluku, joka määrittää, kuinka monta kertaa tiedosto on muuttunut. TÄYTYY kasvattaa, kun **guidFileVersion**-kenttä muuttuu.

`guidDenyReadFileVersion (16 tavua): GUID. Kun tiedoston olemassa olevaa sisältöä muutetaan, lukuun ottamatta tiedoston **Header** rakennetta ja käyttämättömiä tallennuslohkoja, **guidDenyReadFileVersion** ON vaihdettava uuteen GUID-tunnukseen.

`grfDebugLogFlags (4 tavua):` PITÄÄ olla nolla. TÄYTYY jättää huomiotta.

`fcrDebugLog (12 tavua):` **FileChunkReference64x32**-rakenne, jonka TÄYTYY olla arvo fcrZero. TÄYTYY jättää huomiotta.

`fcrAllocVerificationFreeChunkList (12 tavua):` **FileChunkReference64x32**-rakenne, jonka TÄYTYY olla fcrZero. TÄYTYY jättää huomiotta.

`bnCreated (4 tavua):` Etumerkitön kokonaisluku, joka määrittää tämän versiosäilön tiedoston luoneen sovelluksen koontinumeron. PITÄÄ jättää huomiotta.

`bnLastWroteToThisFile (4 tavua):` Etumerkitön kokonaisluku, joka määrittää tähän versiovarastotiedostoon viimeksi kirjoittaneen sovelluksen koontiversion numeron. PITÄÄ jättää huomiotta.

`bnOldestWritten (4 tavua):` Etumerkitön kokonaisluku, joka määrittää vanhimman tähän versiovarastotiedostoon kirjoittaneen sovelluksen koontinumeron. PITÄÄ jättää huomiotta.

`bnNewestWritten (4 tavua):` Etumerkitön kokonaisluku, joka määrittää tähän versiovarastotiedostoon kirjoittaneen uusimman sovelluksen koontinumeron. PITÄÄ jättää huomiotta.

rgbReserved (728 tavua): TÄYTYY olla nolla. TÄYTYY jättää huomiotta.

## Viitteet ##

* [[MS-ONESTORE] - OneNote-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


