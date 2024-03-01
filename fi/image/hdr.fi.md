{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDR-tiedostomuoto - mikä on HDR-kuvatiedosto?",
  "description": "Opi HDR-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata HDR-tiedostoja.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-fir"
}
},
  "lastmod": "2022-07-21"
}

## Mikä on HDR-tiedosto?

HDR-tiedosto on korkean dynaamisen alueen (HDR) rasterikuvatiedostomuoto digikamerakuvien tallentamiseen. Sen avulla valokuvaeditorit voivat parantaa digitaalisten kuvien värejä ja kirkkautta, joilla on rajoitettu dynaaminen alue. Tämä muutos voi parantaa kulmien kirkkautta, mikä johtaa luonnollista läheiseen kuvaan. HDR-tiedostot tallennetaan yleensä 32-bittisinä rasterikuvina. Adobe Photoshop voi luoda ja avata HDR-tiedostoja.

HDR-tiedostot tunnetaan myös nimellä HDRI.

## HDR-tiedostomuoto – lisätietoja

HDR-tiedostomuoto perustuu alkuperäiseen Radiance Picture (.pic) -tiedostomuotoon. HDR-tiedoston pikselitiedot tallennetaan yleensä pakkaamattomina, mutta joissain tapauksissa ne pakataan yksinkertaisella ajonpituisella koodausjärjestelmällä.

### HDR-tiedostorakenne

HDR-kuvatiedosto koostuu seuraavista kolmesta osasta:

 * **Otsikko:** HDR-tiedosto tunnistetaan kuvatiedoston ensimmäisistä tavuista eli #?RADIANCE.
 * **Resoluutiomerkkijono:** Otsikkoa seuraa yksi resoluutiorivi, joka koostuu 4 arvosta; X- ja Y-tunniste, jota seuraa numeerinen kokonaislukuarvo. X:n ja Y:n järjestys osoittaa pyörimisen. X:n ja Y:n yhdistelmä positiivisten ja negatiivisten arvojen kanssa kattaa kaikki mahdolliset kuvan suunnat ja kierrokset.
 * **Pikselitiedot:** HDR-tiedoston pikselitiedot on joko pakkaamaton tai pakattu käyttämällä tavallista ajonpituuskoodausta.

## Avoimen lähdekoodin HDR/HDRI-sovellusliittymät

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** – Eri alustojen huippunopea yhden otsikon [C++](/programming/cpp/) -kirjasto, jolla saat kuvan koon ja muodon lataamatta/dekoodaamatta.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** – Ruostekirjasto, josta saat kuvan koon ja muodon lataamatta/dekoodaamatta. Tukee [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (pic), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/ png/), [psd](/image/psd/), qoi, tga, tiff (tif) ja webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** – HdrHistogramin Java-toteutus.

## Viitteet

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

