{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extension", "file", "format", "image", "Device-Independent Bitmap", "Cursor File Format", "Cursor", "Windows", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - kurzorfájl formátum",
  "description":"További információ a CUR fájlformátumról és az API-król, amelyek CUR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a CUR fájl? ##

A CUR fájl egy statikus Microsoft Windows kurzorfájl formátum. Alapvetően helyhez kötött képek, amelyek minden tekintetben megegyeznek az ICO (ikon) fájlokkal, kivéve a kiterjesztést. Mind a CUR, mind az [ICO](/hu/image/ico/) a Device-Independent Bitmap [DIB](/hu/image/dib/) (Device-Independent Bitmap) specifikáció alapján jön létre. Az alapértelmezett, valamint az egyéni kurzorok, például a Windows egérmutató a Windows operációs rendszerhez, CUR-fájlokban tárolódnak. Ez lehet egy nyíl normál használathoz, egy forgó homokóra a várakozási idők bemutatásához, vagy egy I-sáv a szövegszerkesztéshez. A CUR fájlok az egyéni asztali témák telepítőcsomagjával együtt érkeznek, hogy biztosítsák, hogy a Windows kurzor megfeleljen az egyéni asztali témának.

## Műszaki specifikáció ##

A CUR fájlok bináris rendszerfájlok, amelyek a Microsoft Windows operációs rendszeren működő eszközökön találhatók. A CUR mutatóképek különböző szabványos méretűek, például 16×16, 32×32 stb. A CUR fájlok nagyon hasonlóak az ICO fájlokhoz; mindkettő kis állóképekből áll. Csak a CUR és ICO fájlok kiterjesztése különbözik. Ezenkívül a CUR fájl fejlécében található hotspot magyarázata eltér az ICO fájltól. A hotspot értelmezi a pixeleltolást a bal felső saroktól az egérmutató helyéig. A Windows rendszerek továbbra is a CUR fájlokat használják, de most az animált kurzorok általában ANI kiterjesztéssel rendelkeznek CUR helyett.

## Rövid története ##

A CUR fájl az ICO fájlból készül. Az első CUR fájlformátumot 1981-ben építették be a Microsoft Windows 1.0 operációs rendszerébe, hogy megkönnyítsék a kereskedelmi használatot. Hamarosan újabb interaktív kurzorokat vezettek be, amelyek lehetővé teszik a felhasználók számára, hogy módosítsák kurzorbeállításaikat az előre telepített lehetőségek közül. A CUR fájlt azonban könnyű önállóan szerkeszteni, még akkor is, ha nem rendelkezik megfelelő műszaki ismeretekkel.


## CUR példa ##

A CUR fájlok a *C:\Windows\Cursors* címen találhatók:

{{< figure src="../cur.png" alt="CUR fájlformátum" >}}

