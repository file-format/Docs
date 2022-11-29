{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK-filformat - AWK-skriptfil",
  "description":"Läs mer om AWK-filformat och API:er som kan skapa och öppna AWK-filer.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Vad är en AWK fil?

En AWK-fil är en skriptfil skapad för textbehandlingsapplikationen **AWK** som levereras med Unix- och Linux-operativsystem. Den innehåller logiska instruktioner för att utföra åtgärder på text eller innehåll i en fil, som att matcha, ersätta och skriva ut text. Detta hjälper till att generera rapporter och formaterad text från inmatningsfilen. Verktyget awk finns vanligtvis i /usr/bin/awk på de flesta linux/unix-distributioner.

## Hur skapar man AWK-skript?

En AWK-fil kan skapas eller öppnas i valfri textredigerare på Linux/Unix OS. En ny AWK-skriptfil kan skapas enligt följande.

```
$ vi script.awk
```

Detta öppnar AWK-filen i textredigeraren. Skriv in några påståenden i textredigeraren enligt följande.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Den första raden i detta textinnehåll förklaras enligt följande.

* \#! – kallad "Shebang", som anger en tolk för instruktionerna i ett manus
* /usr/bin/awk – är tolken
* -f – tolkalternativ, används för att läsa en programfil

## Hur kör man AWK-skript?

Spara filen och gör skriptet körbart genom att utfärda kommandot nedan:
```
$ chmod +x script.awk
```

Skriptet kan sedan köras enligt följande.

```
$ ./script.awk
```

som resulterar i följande utdata.

```
Writing my first Awk executable script!
```

## Referens ##

* [Skriv skript med Awk Programming Language](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

