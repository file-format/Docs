{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VPK-tiedosto - PlayStation Vita -sovelluspaketin tiedostomuoto",
  "description": "Opi VPK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VPK-tiedostoja.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-fik"
}
},
  "lastmod": "2022-03-01"
}

## Mikä on VPK-tiedosto?

Tiedosto, jonka laajennus on .vpk, on pakattu arkistopakettitiedosto, jota käytetään kolmannen osapuolen sovellusten asentamiseen Sony PlayStation Vita -pelikonsoliin. Nämä tiedostot voidaan asentaa vain HENkakun Jailbreak Vita PlayStationiin, joka mahdollisti PS Vitan ja PSTV:n käyttää räätälöityä käyttäjien luomaa sisältöä. VPK-arkistotiedosto sisältää kaiken sisällön, joka muodostaa pelin, mukaan lukien kuvat, kuten [PNG](/image/png/)-tiedostot, asetustiedostot, kuten [.bin](/disc-and-media/bin/), ja kaikki määritykset [XML](/web/xml/)-tiedostomuodossa.

## VPK tiedostomuoto

VPK-tiedostot tallennetaan levylle vakiopakattuna [ZIP](/compression/zip/)-arkistoon. Ne voivat sisältää useita kansioita ja muita liitettyjä tiedostoja kolmannen osapuolen sovelluksille, jotka asennetaan Vita Gaming Consoleen. Voit tarkastella VPK-pakettitiedoston sisältöä nimeämällä sen laajennuksen .vpu:sta .zip:ksi ja purkamalla sisällön käyttämällä tavallisia purkuapuohjelmia, kuten WinZip tai WinRAR.

Valvesoftwarella on yksityiskohtaisia tietoja [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format):sta, joihin voidaan viitata kehittäjän näkökulmasta.

## Kuinka asentaa VPK-tiedostoja?

VPK-tiedostot voidaan asentaa komentoriviohjelmasta VPK.exe. Windows-käyttöjärjestelmässä tiedostot voidaan pudottaa vpk.exe-tiedostoon, joka palauttaa \*.vpk-tiedoston, joka sisältää kaikki pakatut tiedostot. Vaihtoehtoisesti komentorivityökalua voidaan käyttää seuraavasti.

### Luo VPK ja lisää tiedostoja

```
vpk <dirname>
```

### Pura VPK-tiedostot

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Viitteet

* [VPK-tiedostomuoto](https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [VPK-tiedostot](https://developer.valvesoftware.com/wiki/VPK)


