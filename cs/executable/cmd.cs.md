{
  "date" : "2021-07-12",
  "keywords" :[ "soubor cmd", "co je soubor cmd", "soubor", "příklad cmd", "přípona souboru cmd", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru CMD a rozhraních API, která mohou vytvářet a otevírat soubory CMD.",
  "title" :"CMD - Windows Command File Format",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Co je soubor CMD?
Soubor CMD se skládá ze skriptu obsahujícího jeden nebo více příkazů ve formě prostého textu, které se spouštějí za účelem provádění různých úloh. Je podobný souboru [BAT](/cs/executable/bat/), který se také obecně používá k uložení dávky spustitelných příkazů. Soubory CMD jsou široce používány v operačním systému Microsoft Windows. Tyto soubory byly zavedeny téměř v 90. letech, ale stále se používají v nejnovějším operačním systému Windows. Tyto soubory jsou obecně zapsány pro provedení více než jednoho příkazu v sekvenci.

## Formát souboru CMD
CMD je formát souboru používaný spustitelnými programy ve stylu CP/M. Obecně je srovnatelný s [COM](/cs/executable/com/) v CP/M-80 a [EXE](/cs/executable/exe/) v DOSu. Soubor CMD obsahuje 1 až 8 skupin kódu nebo dat a 128bajtové záhlaví. Každá skupina může mít velikost až 1 MB. Soubory CMD mohou také obsahovat informace o přemístění a rozšíření rezidentního systému (RSX) v pozdějších verzích. CMD je nováček ve srovnání se souborem [BAT](/cs/executable/bat/); používané pro MS-DOS před vydáním Windows V MS-DOS. Ačkoli i dnes můžete ukládat soubory s příponou .bat, mnoho lidí používá k ukládání svých spustitelných skriptů příponu .cmd.

### Specifikace formátu CMD

Začátek hlavičky obsahuje seznam skupin přítomných v souboru spolu s jejich typy. Každý typ lze použít maximálně jednou. Jedná se o tyto typy:

- Kód
- Data
- Extra
- Zásobník
- uživatel 1
- uživatel 2
- uživatel 3
- uživatel 4
- Sdílený kód

Podobně jako Program Segment Prefix v DOSu je prvních 256 bajtů datové skupiny nula. Budou vyplněny CP/M-86 s nulovou stránkou. Pokud neexistuje žádná datová skupina, použije se místo ní prvních 256 bajtů kódové skupiny.
## Příklad souboru CMD
Následuje příklad skriptu CMD pro zobrazení systémových informací.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Reference

* [Jak napsat skript CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [soubor CMD (CP/M) – z Wikipedie](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

