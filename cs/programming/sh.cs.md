{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell Script File",
  "description":"Další informace o formátu souboru SH a rozhraních API, která mohou vytvářet a otevírat soubory SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Co je soubor SH?

Soubor s příponou .sh je soubor příkazů skriptovacího jazyka, který obsahuje počítačový program, který má být spuštěn unixovým shellem. Může obsahovat řadu příkazů, které se spouštějí sekvenčně a provádějí operace, jako je zpracování souborů, provádění programů a další podobné úkoly. Ty jsou spouštěny z rozhraní příkazového řádku uživatelem nebo v dávce, aby bylo možné provádět více operací současně. Soubory skriptů lze otevřít v textových editorech, jako je Notepad, Notepad++, Vim, Apple Terminal a další podobné aplikace v OS Windows, MacOS a Linux.

## Formát souboru SH

Soubory SH jsou psány jako prostý text podle definované syntaxe. Tyto soubory skriptů podporují:

* `Komentáře` - Komentáře začínají znakem # a shell je ignoruje.
* `Zkratky` - Lze je použít k přejmenování příkazu pro krátké a snadné provedení.
* `Dávkové úlohy` - Několik příkazů může být provedeno automaticky, které by jinak bylo nutné zadat ručně. To odstraňuje potřebu čekat, až uživatel spustí každou fázi sekvence.
* `Zobecnění` - Pomocí jednoduchých smyček lze dosáhnout mnohem většího zobecnění operací, jako je převod obrázků z jednoho formátu do druhého.

## Příklad souboru SH

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
## Jak spustit soubor SH?
Soubory SH obvykle běží na Linuxu, dokonce i ve Windows se musíte ke spuštění souborů sh připojit k terminálu Linux pomocí softwaru, jako je Putty. Níže jsou uvedeny kroky ke spuštění souboru SH na terminálu Linux.

1. Otevřete terminál Linux a přejděte do adresáře, kde je umístěn soubor SH.
2. Pomocí příkazu `chmod` nastavte oprávnění ke spuštění vašeho skriptu (pokud již není nastaveno).
3. Spusťte skript jedním z následujících způsobů
1. `./název_souboru.sh`
2. `sh název_souboru.sh`
3. `bash script-name-here.sh`

## Reference

* [Bashscripting pro začátečníky](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

