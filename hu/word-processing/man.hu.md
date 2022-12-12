{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix kézikönyv",
  "description":"További információ a FODT fájlformátumról és az API-król, amelyek MAN fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Mi az a MAN fájl?

A .man kiterjesztésű fájl a man oldal rövidítése, amely egy Unix programozási felhasználói kézikönyv szoftverdokumentációs formában. A Unix-ban található "Man" segédprogram használja, amely a dokumentáció megtekintésére szolgál. A szoftver dokumentációja olyan szakaszokban és oldalakon tartalmaz információkat, amelyek a Man segédprogrammal a parancsterminálból parancsok kiadásával visszakereshetők. Mivel a számítógépen a dokumentáció puha másolataként elérhető, nincs szükség nyomtatott példányra vagy internetkapcsolatra a hozzáféréshez.

## Unix Manual Man File Format - További információ

A kézikönyvoldalak egyszerű szöveges formátumban vannak tárolva, és bármilyen szövegszerkesztőben létrehozhatók és megnyithatók megtekintés vagy szerkesztés céljából. A UNIX rendszerben a Man oldalak információit a terminálból kiadott parancsok segítségével lehet lekérni, amelyek hivatkozást tartalmaznak a kézikönyv szakaszaira és oldalszámaira.

### Szakaszok és oldalak

A Unix man a rendszer kézikönyve, ahol a parancs minden oldalargumentuma egy program, segédprogram vagy függvény nevére utal. a parancs, ha rendelkezik szakaszinformációkkal, megkeresi az adott szakaszban lévő oldalt. Az alapértelmezett viselkedés azonban az, hogy minden szakaszban megkeresi az oldalt, és megjeleníti az első oldalt, függetlenül attól, hogy több szakaszban is létezik-e.

### Szakaszszámok

Az alábbiakban a kézikönyv szakaszszámaira vonatkozó információk találhatók, majd a bennük található oldalak típusai.

|Szakaszszám|Oldaltípus|
---|---|
|1|Futtatható programok vagy shell-parancsok|
|2|Rendszerhívások (a kernel által biztosított funkciók)|
|3|Könyvtárhívások (a programkönyvtárakon belüli funkciók)|
|4|Speciális fájlok (általában a /dev könyvtárban találhatók)|
|5|Fájlformátumok és konvenciók, pl. /etc/passwd|
|6|Játékok|
|7|Egyéb (makrócsomagokat és egyezményeket is beleértve), pl. man(7), groff(7)|
|8|Rendszeradminisztrációs parancsok (általában csak a root számára)|
|9|Kernel-rutinok [Nem szabványos]|

## Példa – Hogyan olvassunk MAN oldalakat?

Íme egy példa arra, hogyan lehet lekérni az MkDir paranccsal kapcsolatos információkat a Man paranccsal.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Hivatkozások

* [OpenDocument műszaki specifikációi – a Wikipedia által](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) – Linux kézikönyv oldal](https://man7.org/linux/man-pages/man1/man.1.html)

