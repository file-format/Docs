{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI File - Asterisk Gateway Interface File Format",
  "description":"Zjistěte, co je formát souboru AGI s příklady a rozhraními API, která mohou vytvářet a otevírat soubory AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Co je soubor AGI?

Soubor AGI je soubor skriptu používaný open source telefonním systémem Asterisk. Obsahuje informace, které lze použít k automatizaci procesů a vytáčení Asterisk. Pomocí souborů skriptů AGI lze navázat spojení s relačními databázemi, jako je PostgreSQL nebo MySQL. Kromě toho lze skripty AGI použít také pro přístup k dalším externím zdrojům. Skripty AGI mohou převést kontrolu nad dialplanem na externí skript AGI, což umožňuje Asterisku provádět složité úkoly.

## Formát souboru AGI - Další informace

Soubory skriptů AGI se ukládají jako textové soubory a lze je otevřít v libovolném textovém editoru pro provádění změn.

### Standardní vzor komunikace AGI

Skript AGI načte proměnné a jejich hodnoty, které mu posílá Asterisk. Běžný vzhled těchto proměnných je následující.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Po těchto proměnných následuje prázdný řádek odeslaný Asterisk, což ukazuje, že skript AGI nyní může převzít kontrolu nad dialplanem.

### Programovací jazyk pro AGI Script Files

Skripty AGI lze obvykle psát v Perlu, [PHP](/cs/programming/php/), [C](/cs/programming/c/), Pascalu nebo Bourne Shell.

## Reference

* [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

