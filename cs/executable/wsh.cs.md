{
  "date" : "2021-08-27",
  "keywords" :[ "soubor wsh", "formát souboru wsh", "co je soubor wsh", "soubor", "příklad wsh", "přípona souboru wsh", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů WSH a rozhraních API, která mohou vytvářet a otevírat soubory WSH.",
  "title" :"WSH - soubor skriptu Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Co je soubor WSH?
Soubor s příponou .wsh obsahuje vlastnosti a parametry pro určitý skript programovacího jazyka, jako je VB nebo VBS atd. Skutečná potřeba WSH je použít je pro přizpůsobení provádění určitých skriptů. Pro spuštění je vyžadován WScript nebo CScript a oba jsou součástí operačního systému Windows. Soubory WSH byly původně poskytovány ve Windows 95 na instalačních discích jako volitelná konfigurovatelná a instalovatelná součást pro Ovládací panely a poté jako výchozí součást Windows 98.

## Formát souboru WSH
WSH (Windows Script Host) lze použít pro různé účely, včetně administrace, přihlašovacích skriptů a obecné automatizace. WSH vytváří prostředí pro spouštění skriptů. vyvolá vhodný skriptovací stroj a přidělí sadu služeb a objektů, se kterými bude skript pracovat. Tyto skripty lze spouštět v režimu GUI, z objektu COM nebo z režimu příkazového řádku, což uživateli poskytuje flexibilitu pro interaktivní i neinteraktivní skripty.

### Příklady
Zde je velmi jednoduchý příklad, který ukazuje nějaký VBScript, který používá kořenový objekt WSH COM "WScript" k zobrazení zprávy s tlačítkem 'OK'. Když bude tento skript spuštěn, bude zavolán CScript nebo WScript engine a bude vytvořeno běhové prostředí.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Reference

* [Windows Script Host – od Wikipedie](https://en.wikipedia.org/wiki/Windows_Script_Host)



