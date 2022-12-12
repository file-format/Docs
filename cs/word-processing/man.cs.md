{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix Manual",
  "description":"Další informace o formátu souboru FODT a rozhraních API, která mohou vytvářet a otevírat soubory MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Co je soubor MAN?

Soubor s příponou .man znamená man page, což je uživatelská příručka pro programování Unixu ve formě softwarové dokumentace. Používá ho nástroj `Man`, který je součástí Unixu a který se používá k prohlížení dokumentace. Softwarová dokumentace obsahuje informace v oddílech a stránkách, které lze získat pomocí obslužného programu Man z příkazového terminálu zadáním příkazů. Vzhledem k tomu, že je k dispozici v počítači jako softwarová kopie dokumentace, nevyžaduje pro přístup k ní žádnou tištěnou kopii ani připojení k internetu.

## Unix Manual Man File Format – Další informace

Manuálové stránky jsou uloženy ve formátu prostého textu a lze je vytvořit a otevřít v libovolném textovém editoru pro prohlížení nebo úpravy. V UNIXu se informace z manuálových stránek získávají pomocí příkazů z terminálu, které obsahují odkaz na čísla oddílů a stránek z manuálu.

### Sekce a stránky

Unix man je systémový manuál, kde každý argument stránky příkazu odkazuje na název programu, nástroje nebo funkce. příkaz, je-li poskytnut s informacemi o sekci, vyhledá stránku v této konkrétní sekci. Výchozí chování je však vyhledat stránku ve všech sekcích a zobrazit první stránku bez ohledu na to, zda existuje ve více sekcích.

### Čísla oddílů

Následují informace o číslech sekcí příručky následované typy stránek, které obsahují.

|Číslo sekce|Typ stránek|
---|---|
|1|Spustitelné programy nebo příkazy shellu|
|2|Systémová volání (funkce poskytované jádrem)|
|3|Volání knihovny (funkce v rámci programových knihoven)|
|4|Speciální soubory (obvykle se nacházejí v /dev)|
|5|Formáty souborů a konvence, např. /etc/passwd|
|6|Hry|
|7|Různé (včetně makro balíčků a konvencí), např. man(7), groff(7)|
|8|Příkazy správy systému (obvykle pouze pro uživatele root)|
|9|Rutiny jádra [Nestandardní]|

## Příklad – Jak číst stránky MAN?

Zde je příklad, jak získat informace o příkazu MkDir pomocí příkazu Man.

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

## Reference

* [Technické specifikace OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — manuálová stránka Linuxu](https://man7.org/linux/man-pages/man1/man.1.html)

