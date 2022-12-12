{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru AWK - soubor skriptu AWK",
  "description":"Další informace o formátu souboru AWK a rozhraních API, která mohou vytvářet a otevírat soubory AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Co je soubor AWK?

Soubor AWK je soubor skriptu vytvořený pro aplikaci pro zpracování textu **AWK**, která je dodávána s operačními systémy Unix a Linux. Obsahuje logické instrukce pro provádění akcí s textem nebo obsahem souboru, jako je porovnávání, nahrazování a tisk textu. To pomáhá generovat zprávy a formátovaný text ze vstupního souboru. Obslužný program awk je obvykle umístěn v /usr/bin/awk na většině distribucí Linux/unix.

## Jak vytvořit skript AWK?

Soubor AWK lze vytvořit nebo otevřít v libovolném textovém editoru na OS Linux/Unix. Nový soubor skriptu AWK lze vytvořit následovně.

```
$ vi script.awk
```

Tím se otevře soubor AWK v textovém editoru. Zadejte některá tvrzení do textového editoru následovně.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
První řádek tohoto textového obsahu je vysvětlen následovně.

* \#! – označovaný jako „Shebang“, který specifikuje interpreta pro instrukce ve skriptu
* /usr/bin/awk – je interpret
* -f – volba tlumočníka, používaná ke čtení programového souboru

## Jak spustit skript AWK?

Uložte soubor a udělejte skript spustitelným zadáním příkazu níže:
```
$ chmod +x script.awk
```

Skript lze poté spustit následovně.

```
$ ./script.awk
```

výsledkem je následující výstup.

```
Writing my first Awk executable script!
```

## reference ##

* [Psaní skriptů pomocí programovacího jazyka Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

