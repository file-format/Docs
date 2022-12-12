{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK fájlformátum - AWK szkriptfájl",
  "description":"További információ az AWK fájlformátumról és az API-król, amelyek AWK fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Mi az AWK fájl?

Az AWK-fájl az **AWK** szövegfeldolgozó alkalmazás számára létrehozott szkriptfájl, amely Unix és Linux operációs rendszerekkel együtt érkezik. Logikai utasításokat tartalmaz a szöveggel vagy a fájl tartalmával kapcsolatos műveletek végrehajtására, például szöveg egyeztetésére, cseréjére és nyomtatására. Ez segít jelentéseket és formázott szöveget generálni a bemeneti fájlból. Az awk segédprogram általában a /usr/bin/awk könyvtárban található a legtöbb linux/unix disztribúción.

## Hogyan készítsünk AWK szkriptet?

Az AWK fájl bármely szövegszerkesztőben létrehozható vagy megnyitható Linux/Unix OS rendszeren. Új AWK szkriptfájlt az alábbiak szerint lehet létrehozni.

```
$ vi script.awk
```

Ezzel megnyílik az AWK fájl a szövegszerkesztőben. Írjon be néhány állítást a szövegszerkesztőbe az alábbiak szerint.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
A szövegtartalom első sorát a következőképpen magyarázzuk.

* \#! – „Shebang” néven hivatkozunk rá, amely értelmezőt ad meg a szkriptben lévő utasításokhoz
* /usr/bin/awk – a tolmács
* -f – értelmező opció, programfájl olvasására szolgál

## Hogyan kell végrehajtani az AWK szkriptet?

Mentse el a fájlt, és tegye futtathatóvá a szkriptet az alábbi parancs kiadásával:
```
$ chmod +x script.awk
```

A szkript ezután a következőképpen futtatható.

```
$ ./script.awk
```

ami a következő kimenetet eredményezi.

```
Writing my first Awk executable script!
```

## Hivatkozási szám

* [Szkriptek írása Awk programozási nyelv használatával](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

