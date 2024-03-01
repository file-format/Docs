{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - Microsoft OneNote -tiedostomuoto",
  "description": "Opi ONETOC2-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ONETOC2-tiedostoja.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-fi2"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

Kun luot muistikirjan OneNote 2016:ssa, se tallennetaan automaattisesti uuteen 2010–2016 tiedostomuotoon. Tarvitset tätä muotoa, jos haluat, että kaikki OneNote 2016:n ominaisuudet, kuten matemaattiset yhtälöt ja linkitetyt muistiinpanot, toimivat oikein.

## ONETOC2-tiedostomuoto ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### Tiedostorakenne ###

Versiomuistitiedoston TÄYTYY alkaa rakenteella **Header**. Loput tiedostosta jaetaan tavulohkoihin, joissa kunkin lohkon koko ja rakenne määritellään siihen viittaavassa kentässä. Lohko on tavoitettavissa, jos siihen viitataan **Otsikko**-rakenteella tai jos siihen viitataan toisen saavutettavan lohkon kentällä. **Otsikko**-rakenteen ulkopuoliset tiedot ja kaikki tavoitettavissa olevat lohkot TÄYTYY jättää huomiotta.

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
:


|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 tavua):` Etumerkitön kokonaisluku. TÄYTYY olla jokin seuraavan taulukon arvoista riippuen tämän tiedoston tiedostomuodosta.


|Tiedostomuoto|Arvo
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Viitteet ##

* [[MS-ONESTORE] - OneNote-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


