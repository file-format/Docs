{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DDS-tiedostomuoto - DirectDraw Surface -kuvatiedosto",
  "description": "Opi DDS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DDS-tiedostoja.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-fis"
}
},
  "lastmod": "2022-04-02"
}

## Mikä on DDS-tiedosto?

DDS-tiedosto on rasterikuvatiedosto, joka käyttää DirectDraw Surface (DDS) -säilömuotoa. Se tallentaa pakkaamattomia ja pakattuja (DXTn) pintakuvioita ja toteuttaa erilaisia tyyppejä erityyppisten tietojen tallentamiseen. Se tukee myös useita erityyppisiä tietoja, kuten yksikerroksisia tekstuureja, pintakuvioita mipmapsilla, kuutiokarttoja, volyymikarttoja ja pintakuviotaulukoita. Tämän ansiosta DDS-tiedostot voivat tallentaa videopelien pintakuvioyksikkömalleja digitaalisten valokuvien ja Windows-työpöydän taustakuvien lisäksi. Microsoft on kehittänyt DDS-tiedostomuodon käytettäväksi DirectX SDK:n kanssa.

## DDS tiedostomuoto

DDS-tiedostot tallennetaan binääritiedostoina ja niitä voidaan käyttää DirectX SDK:n kanssa. Se hyödyntää DirectX:n tehoa reaaliaikaisten renderöintisovellusten, kuten 3D-pelien, kehittämiseen.

### DDS-tiedoston asettelu

Microsoft on dokumentoinut [DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) yksityiskohtaisesti. Binääri DDS-tiedosto sisältää seuraavat tiedot.

 * DWORD (maaginen numero), joka sisältää nelimerkkisen koodiarvon 'DDS' (0x20534444).
 * A description of the data in the file.

DDS_HEADER kuvaa dataa ja DDS_PIXELFORMAT kuvaa pikselimuotoa. Molemmat korvaavat vanhentuneet DDSURFACEDESC2-, DDSCAPS2- ja DDPIXELFORMAT DirectDraw 7 -rakenteet.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) tarkentaa tämän tiedostomuodon teknisiä yksityiskohtia.

## Viitteet

* [DDS – Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)

