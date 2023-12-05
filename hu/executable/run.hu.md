{
  "date" : "2023-01-31",
  "keywords" :["futtatási fájl", "mi az a futtatófájl", "fájl", "hogyan kell megnyitni a futtatófájlt", "fájl kiterjesztése", "kiterjesztés"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a RUN fájlformátumról és az API-król, amelyek RUN fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"Fájlformátum futtatása - Linux futtatható fájl",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Mi az a RUN fájl?

A .run fájlformátumot általában szoftverek vagy alkalmazástelepítők terjesztésére használják Linux környezetben. A szoftver telepítéséhez a fájlt futtathatóvá kell tenni, amit a következő paranccsal tehet meg:

```bash
chmod +x file_name.run 
```

Ezután a következő paranccsal futtathatja a fájlt:

```bash
./file_name.run 
```

A telepítési folyamat a telepíteni kívánt fájltól és programtól függően változhat.

A .run fájlformátum egyfajta shell szkript, amelyet szoftverek vagy alkalmazástelepítők Linux környezetben való terjesztésére használnak. Ez egy önálló csomag, amely mindent tartalmaz, ami a szoftver telepítéséhez szükséges, beleértve a bináris fájlokat, könyvtárakat és konfigurációs fájlokat.

Fontos megjegyezni, hogy a .run fájlok is tartalmazhatnak rosszindulatú kódot, ezért mindig célszerű ellenőrizni a fájl forrását, és víruskeresni, mielőtt futtatná.

Ezenkívül egyes .run fájlok futtatásához és telepítéséhez root jogosultság szükséges, ezért előfordulhat, hogy a "sudo" parancsot kell használnia a fájl emelt szintű jogosultságokkal történő futtatásához:

```bash
sudo ./filename.run
```

## Hogyan lehet megnyitni a RUN fájlt?

A .run fájl megnyitásához futtathatóvá kell tenni, amit a "chmod" paranccsal lehet megtenni:

```bash
chmod +x filename.run 
```

Miután a fájl végrehajthatóvá lett, futtathatja a következő beírásával:

```bash
./filename.run
```

A .run fájl futtatása nem ugyanaz, mint a szövegszerkesztőben való megnyitása. A .run fájl futtatása végrehajtja az utasításait, amelyek bármiek lehetnek a program telepítésétől a szkript futtatásáig. A .run fájl tartalmának megtekintéséhez meg kell nyitnia azt egy szövegszerkesztőben, például nano vagy vim:

```
nano filename.run
```
vagy
```
vim filename.run
```

## Hivatkozások
* [A .bin és .run fájlok végrehajtása Ubuntuban](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


