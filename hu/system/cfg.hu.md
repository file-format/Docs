{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "kiterjesztés", "fájl", "formátum", "rendszer", "konfiguráció", "beállítások", "programok", "számítógép", "alkalmazás" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Fájlformátum",
  "description":"További információ a CFG fájlformátumról és az API-król, amelyek CFG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a CFG fájl? ##

A .cfg kiterjesztésű fájl egyfajta "beállítási" fájl. Ez egy népszerű fájltípus, és a számítógépes programok konfigurációjával és beállításaival kapcsolatos információk tárolására szolgál. A legtöbb CFG fájltípus szöveges formátumban van tárolva, és nem szabad kézzel megnyitni, hanem szövegszerkesztővel kell megnyitni. Vannak azonban különböző típusú CFG-fájlok, amelyek különböznek az információ tárolási formátumától. A CFG-fájlok által kínált funkciók alkalmazásonként változnak. Egyes számítógépes alkalmazások lehetővé teszik a felhasználók számára, hogy grafikus interferenciák segítségével módosítsák vagy fejlesszék konfigurációs fájljaik szintaxisát, míg mások csak szövegszerkesztővel teszik lehetővé a módosításokat. A fájlok módosítása után a felhasználók utasíthatják az alkalmazást, hogy olvassa újra ezeket a fájlokat, és alkalmazza a módosításokat a rendszeren.


## CFG fájlformátum ##

A CFG fájlokat különféle operációs rendszerek támogatják, például a Unix és a Unix-szerű operációs rendszerek, az MS-DOS, a macOS, a Microsoft Windows és az IBM OS/2. A fájlok tárolási és felhasználási formátuma az egyes operációs rendszerekben eltérő. A legtöbb rendszer ember által olvasható és szerkeszthető szöveges formátumban használja és tárolja ezeket a fájlokat, míg mások a fájlhasználattól és az operációs rendszer követelményeitől függően bonyolultabb formátumban tárolják.

A Unix és Unix-szerű operációs rendszerekben a legtöbb CFG fájl többféle formátumstílust használ a CFG fájlokhoz, azonban a legelterjedtebb formátum a könnyen olvasható szöveges formátum, és szinte mindegyik formátum lehetővé teszi megjegyzések készítését és szerkesztését. A CFG fájlok leggyakoribb fájlkiterjesztései ezekben az operációs rendszerekben a CNF, CONF, CF és INI.

Az MS-DOS operációs rendszerben kezdetben egyetlen konfigurációs fájlformátum volt, mégpedig a sima szöveges, de az MS-DOS 6 magával hozta az INI konfigurációs fájlformátum bevezetését.

A macOS szabványos tulajdonságlista-formátum-stíluskonfigurációs fájlt használ.

A Microsoft Windows rendszerben az egyszerű szöveges INI stílusú konfigurációs fájlok az információk tárolásának és szerkesztésének fontos forrásai voltak, azonban 1993-ban új adatbázisrendszert vezettek be, ami 1993 után a konfigurációs fájlok használatának csökkenéséhez vezetett a Microsoft Windows rendszerben.


## ## CFG példa

Egy minta CFG fájl az alábbiakban látható:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
