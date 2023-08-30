{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR File Format - Mi az a HDR képfájl?",
  "description":"További információ a HDR fájlformátumról és az API-król, amelyek HDR-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Mi az a HDR fájl?

A HDR fájl egy nagy dinamikatartományú (HDR) raszteres képfájlformátum, amely digitális fényképezőgéppel készült fényképek tárolására szolgál. Lehetővé teszi a fotószerkesztők számára, hogy javítsák a korlátozott dinamikatartománnyal rendelkező digitális képek színét és fényerejét. Ezzel a módosítással javítható a sarkok körüli fényerő, ami természetközeli képet eredményez. A HDR-fájlokat általában 32 bites raszterképként menti a rendszer. Az Adobe Photoshop képes HDR-fájlok létrehozására és megnyitására.

A HDR fájlok HDRI néven is ismertek.

## HDR fájlformátum – További információ

A HDR fájlformátum az eredeti Radiance Picture (.pic) fájlformátumon alapul. A HDR-fájlok pixeladatait általában tömörítetlenül tárolják, de bizonyos esetekben egy egyszerű futáshosszúságú kódolórendszer segítségével tömörítik.

### HDR fájlstruktúra

A HDR képfájl a következő három részből áll:

* **Fejléc:** A HDR-fájlt a képfájl első bájtja, azaz a „#?RADIANCE” azonosítja.
* **Felbontási karakterlánc:** A fejlécet egyetlen felbontási sor követi, amely 4 értékből áll; egy X és Y címke, amelyet egy-egy numerikus egész szám követ. Az X és Y sorrendje a forgást jelzi. Az X és Y kombinációja pozitív és negatív értékekkel lefedi az összes lehetséges képtájolást és elforgatást.
* **Pixeladatok:** A HDR-fájlok képpontadatai vagy tömörítetlenek, vagy szabványos futáshosszúságú kódolással vannak tömörítve.

## Nyílt forráskódú HDR/HDRI API-k

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** – Platformokon átívelő szupergyors, egyfejléces [C++](/hu/programming/cpp/) könyvtár a képméret és -formátum eléréséhez betöltés/dekódolás nélkül.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** – Rozsdakönyvtár a képméret és -formátum eléréséhez betöltés/dekódolás nélkül. Támogatja az [.avif](/hu/image/avif/), [.bmp](/hu/image/bmp/), [.cur](/hu/image/cur/), [.dds](/hu/image/dds/), [. gif](/hu/image/gif/), hdr (pic), [heic (heif)](/hu/image/heic/), [.icns](/hu/image/icns/), [.ico](/hu/image/ico /), [.jp2](/hu/image/jp2/), [jpeg (jpg)](/hu/image/jpeg/), [jpx](/hu/image/jpx/), ktx, [png](/hu/image/png /), [psd](/hu/image/psd/), qoi, tga, tiff (tif) és webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** – A HdrHistogram Java implementációja.

## Hivatkozások

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo)

