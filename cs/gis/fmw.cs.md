{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "FMW File - FME Workbench File Format",
  "description":"Přečtěte si o formátu souborů FMW a rozhraních API, která mohou vytvářet a otevírat soubory FMW.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-cs",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Co je soubor FMW?

Soubor FMW je soubor projektu vytvořený pomocí softwaru FME Workbench (dodává se jako součást sady FME Desktop), který se používá pro transformaci prostorových dat. Obsahuje uživatelsky definovaná nastavení používaná pro manipulaci s prostorovými daty, jako jsou sady vstupních dat, vlastnosti překladu, projekce a nastavení výstupu. Nastavení manipulace s prostorovými daty jsou uložena jako vizuální rozvržení a lze je snadno upravit a znovu uložit.

Soubory FMW můžete otevřít pomocí [Safe Software FME Desktop](https://fme.safe.com/platform/).

## Formát souboru FMW – Další informace

Soubory FMW se ukládají na disk jako binární soubory a lze je číst pouze pomocí softwaru FME Desktop. Software také umí číst data z řady formátů relačních databází a podporuje také řadu datových formátů.

### Stručná fakta FMW

|Fakt|Hodnota|
---|---|
|Čtenář/zapisovatel|Čtečka|
|Úroveň licence|Základ|
|Závislosti|Žádné|
|Typ datové sady|Soubor|
|Typ funkce|Pevné|
|Typické přípony souborů|.fmw|
|Podpora automatického překladu|Ano|
|Uživatelem definované atributy|Ne|
|Podpora souřadnicového systému|Ne|
|Obecná podpora barev|Ne|
|Prostorový index|Ne|
|Vyžadováno schéma|Ne|
|Podpora transakcí|Ne|
|Atribut typu geometrie|Žádný|
|Podpora kódování|Ne|

### Podpora geometrie FMW

|Geometrie|Podporováno?|
---|---|
|agregát|ne|
|kruhy|ne|
|kruhový oblouk|ne|
|kobliha mnohoúhelník|ne|
|eliptický oblouk|ne|
|elipsy|ne|
|řádek|ne|
|žádný|ano|
|bod|ne|
|polygon|ne|
|rastr|ne|
|pevné|ne|
|povrch|ne|
|text|ne|
|z hodnoty|ne|


## Reference

* [Safe Software FME Desktop](https://fme.safe.com/platform/)
* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
