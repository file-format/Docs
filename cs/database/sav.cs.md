{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "přípona", "soubor sav", "formát souboru sav", "Typ souboru databáze", "Formát souboru databáze", "co je soubor sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru SAV a rozhraních API, která mohou vytvářet a otevírat soubory SAV.",
  "title" :"SAV - SPSS datový soubor",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Co je soubor SAV?
Soubor SAV je datový soubor vytvořený Statistickým balíčkem pro společenské vědy (SPSS), což je aplikace široce používaná výzkumníky trhu, zdravotními výzkumníky, průzkumnými společnostmi, vládou, výzkumnými pracovníky v oblasti vzdělávání, marketingovými organizacemi a těžaři dat pro statistickou analýzu. SAV uložený v proprietárním binárním formátu a skládá se z datové sady a také slovníku, který datovou sadu představuje, ukládá data v řádcích a sloupcích.

## Formát souboru SAV
Formát souboru SAV se stal relativně stabilním, ale nemůžeme ho označit za statický. V případě potřeby je volitelně k dispozici zpětná a dopředná kompatibilita, ale není správně udržována. Data v souboru SAV jsou rozdělena do následujících sekcí:

### Záhlaví souboru
Skládá se ze 176 bajtů. První 4 bajty označují řetězec **$FL2** nebo **$FL3** v kódování znaků použitém pro soubor. Poslední tři bajty představují, že data v souboru jsou komprimována pomocí **ZLIB**. Další 60bajtový řetězec začíná **@(#) SPSS DATA FILE** a také určuje operační systém a verzi SPSS, která soubor vytvořila. Záhlaví pak pokračuje šestimístnými poli obsahujícími počet proměnných na pozorování a číselný kód pro kompresi a končí znakovými údaji označujícími datum a čas vytvoření a štítkem souboru.
### Záznamy deskriptorů proměnných
Záznam obsahuje pevnou posloupnost polí, klasifikující typ a název proměnné spolu s informacemi o formátování používaných SPSS. Každý záznam proměnné může volitelně obsahovat označení proměnné o délce až 120 znaků a až tři specifikace chybějících hodnot.
### Hodnotové štítky
Štítky hodnot jsou volitelné a jsou uloženy v párech záznamů s celočíselnými štítky 3 a 4. První záznam, kterým je štítek 3, má sekvenci dvojic polí, přičemž každý pár obsahuje hodnotu a přidružený štítek hodnoty. Druhý záznam, kterým je tag 4, představuje, na které proměnné se sada hodnot/štítek vztahuje.
### Dokumenty
Jeden nebo více záznamů s celočíselným tagem 6. Volitelná dokumentace. obsahuje 80 řádků znaků.
### Záznamy rozšíření
Jeden nebo více záznamů s celočíselným tagem 7. Záznamy rozšíření poskytují informace, které lze bezpečně ignorovat, ale v mnoha situacích uchované umožňují u souborů zapsaných novějším softwarem zachovat zpětnou kompatibilitu. Záznamy rozšíření mají značky podtypu typu integer.
### Terminátor slovníku
Záznam pouze s celočíselnou značkou 999. Odděluje slovník od pozorování dat.
### Pozorování dat
Uvažuje se, že data jsou v pořadí pozorování, např. všechny hodnoty proměnných pro první pozorování, následované všemi hodnotami pro druhé pozorování atd. Formát datového záznamu se liší v závislosti na kompresním kódu v záznamu záhlaví souboru. Datovou část souboru .sav lze dekomprimovat:
- **kód 0**: komprimovaný bajtkódem
- **kód 1**: komprimováno pomocí komprese ZLIB
 







## Reference ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

