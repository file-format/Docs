{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell Script File",
  "description":"További információ az SH-fájlformátumról és az SH-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Mi az SH fájl?

Az .sh kiterjesztésű fájl egy parancsnyelvi parancsfájl, amely a Unix shell által futtatandó számítógépes programot tartalmazza. Egy sor parancsot tartalmazhat, amelyek egymás után futnak le olyan műveletek végrehajtására, mint a fájlfeldolgozás, a programok végrehajtása és más hasonló feladatok. Ezeket a parancssori felületről hajtja végre a felhasználó, vagy kötegesen hajtja végre több műveletet egyidejűleg. A szkriptfájlok megnyithatók olyan szövegszerkesztőkkel, mint a Notepad, Notepad++, Vim, Apple Terminal és más hasonló alkalmazások Windows, MacOS és Linux operációs rendszeren.

## SH fájlformátum

Az SH fájlok egyszerű szöveggel vannak írva, a meghatározott szintaxist követve. Ezek a szkriptfájlok támogatják:

* `Megjegyzések` - A megjegyzések # karakterrel kezdődnek, és a shell figyelmen kívül hagyja őket.
* `Parancsikonok` - Ezekkel lehet átnevezni egy parancsot a rövid és egyszerű végrehajtás érdekében.
* `Batch Jobs` - Számos parancs hajtható végre automatikusan, amelyeket egyébként manuálisan kellene megadni. Így nem kell várni, amíg a felhasználó elindítja a sorozat egyes szakaszait.
* `Általánosítás` - Egyszerű hurkokat használva sokkal több általánosítás érhető el az olyan műveleteknél, mint a képek átalakítása egyik állomásról a másikra.

## SH fájl példa

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Hogyan kell futtatni az SH fájlt?
Az SH fájlok általában Linuxon futnak, még Windows alatt is csatlakoznia kell egy Linux terminálhoz olyan szoftverek segítségével, mint a Putty az sh fájlok futtatásához. Az alábbiakban bemutatjuk az SH-fájl Linux-terminálon való futtatásának lépéseit.

1. Nyissa meg a Linux terminált, és lépjen abba a könyvtárba, ahol az SH fájl található.
2. A `chmod` paranccsal állítsa be a parancsfájl végrehajtási engedélyét (ha még nincs beállítva).
3. Futtassa a szkriptet a következők egyikével
1. `./fájlnév.sh`
2. `sh fájlnév.sh`
3. `bash script-name-here.sh`

## Hivatkozások

* [Bashscripting kezdőknek](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

