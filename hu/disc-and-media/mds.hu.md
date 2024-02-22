{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg az MDS fájlformátumot és az API-kat, amelyek MDS fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "MDS fájlformátum – Médialeíró oldalsó fájl",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-hu",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Mi az MDS fájl?

Az MDS (Media Descriptor Sidecar File) az Alcohol 120% és a Daemon Tools szoftverhez kapcsolódó fájl, mindkettő virtuális CD- és DVD-meghajtók létrehozására és kezelésére szolgál. Az MDS fájl információkat tartalmaz a lemezen lévő adatok elrendezéséről, beleértve az összes fájl helyét és a lemez szerkezetét. Ez lehetővé teszi a virtuális meghajtó számára, hogy emulálja a fizikai lemez viselkedését, így a szoftver úgy tudja olvasni a virtuális lemezen lévő adatokat, mintha az valódi lemez lenne.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## 120%-os kapcsolat az alkohollal

Az Alcohol 120% egy népszerű szoftver a virtuális CD- és DVD-meghajtók létrehozására és kezelésére, és az MDS fájlformátumot használja a lemezképek mentésére és elérésére. Az MDS fájlformátum az Alcohol 120% tulajdona, és csak az Alcohol 120% szoftverrel vagy más, azt támogató szoftverrel nyitható meg és használható.

## MDS fájl - Mivel nyitható meg egy MDS fájl?

Egy MDS fájl megnyitásához az Alcohol 120%-ban, telepítenie kell a szoftvert a számítógépére. Az Alcohol 120% telepítése után a következőképpen nyithatja meg az MDS fájlt:

1. Indítsa el a 120%-os alkoholt.
2. Kattintson a Fájl menüre, és válassza a Megnyitás lehetőséget.
3. Keresse meg az MDS fájl helyét a számítógépén, és válassza ki azt.
4. Az MDS-fájl most megnyílik az Alcohol 120%-ban, és a rendszer kéri, hogy válassza ki a megfelelő képfájlt (például ISO, BIN vagy CUE).
5. A képfájl kiválasztása után az Alcohol 120% felcsatolja a képet egy virtuális meghajtóra.

Alternatív megoldásként megnyithat egy MDS fájlt dupla kattintással is, ha az Alcohol 120% be van állítva az MDS fájlok megnyitásának alapértelmezett programjaként. Más olyan szoftvereket is használhat, amelyek támogatják az MDS formátumot, mint például a Daemon Tools, a Virtual CloneDrive, a Virtual Drive Manager és a MagicISO.

## Hivatkozások
* [Alcohol 120% – CD- és DVD-író szoftver](https://www.alcohol-soft.com/)


