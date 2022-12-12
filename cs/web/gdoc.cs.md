{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor GDOC – zástupce Dokumentů Google",
  "description":"Zjistěte, co je soubor GDOC a rozhraní API, která mohou vytvářet a otevírat soubory GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Co je soubor GDOC?

Soubor GDOC je soubor zástupce, který odkazuje na soubor umístěný na Disku Google, cloudové službě úložiště dokumentů. Když je na počítači nainstalován klient Disku Google a je v něm vytvořen dokument, disk vytvoří dokument v online cloudovém úložišti a zapíše [URL](/cs/web/url/) tohoto dokumentu do souboru GDOC v místním Googlu. Složka Disku. Když dvakrát kliknete na tento soubor zástupce, výchozí webový prohlížeč otevře dokument z umístění [URL](/cs/web/url/). Pokud se tento soubor zástupce přesune z této složky, odkaz na online dokument se přeruší.

## Formát souboru GDOC – Další informace

Soubor GDOC obsahuje zástupce online dokumentu napsaného ve formátu souboru [JSON](/cs/web/json/). Prohlížeč otevírající soubory GDOC přečte informace o adrese URL a otevře propojený dokument pro zobrazení za předpokladu, že je uživatel přihlášen k tomuto účtu Google, kde je dokument uložen. Soubory GDOC neobsahují obsah dokumentu.

### Příklad souboru GDOC

Soubor GDOC lze otevřít v textovém editoru a jeho obsah vypadá následovně.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Jak je vidět, obsah je formátován v JSON s adresou URL dokumentu a přidruženým ID dokumentu.

## Reference

* [Dokumenty Google neotevírají soubory gdoc ani docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=cs )

