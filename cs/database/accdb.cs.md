{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru ACCDB a rozhraních API, která mohou vytvářet a otevírat soubory ACCDB.",
  "title" :"Formát souboru ACCDB - databázový soubor Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Co je soubor ACCDB?

Soubor s příponou .accdb je databázový soubor aplikace Microsoft Access 2007, který ukládá data uživatelů do tabulek. Podporuje ukládání vlastní formuláře, SQL dotazy a další data. Soubory ACCDB nahradily soubory [MDB](/cs/database/mdb/) poté, co Microsoft přešel na strukturu souborů založenou na XML. Soubory ACCDB lze stále převádět na MDB se starou kompatibilitou. ACCDB jsou však nyní široce používaným formátem databázových souborů aplikace Access. Microsoft také podporoval další funkce ve formátu ACCDB, jako je možnost ukládání příloh souborů, binární data a podpora vícehodnotových polí.

## Formát souboru ACCDB

Stejně jako MDB nejsou k dispozici žádné veřejné specifikace pro formát souboru ACCDB. Společnost Microsoft podporuje programový přístup k těmto souborům prostřednictvím standardu Open Database Connectivity (ODBC) a Visual Basic for Applications (VBA).

### Postřeh

Hexadecimální výpis jednoduchého souboru ACCDB naznačuje, že existují obecné podobnosti ve struktuře s nejnovějšími verzemi předchozí rodiny formátů MDB. Oba formáty souborů používají pevnou velikost stránky 4096 bajtů. Další podobností mezi ACCDB a MDB je forma magického čísla, která obsahuje řetězec „Standard ACE DB“ pro ACCDB. Verze nebo kód kompatibility je v obou formátech na stejném místě. Nástroje mdbtools | HACKING soubor uvádí "Offset 0x14 obsahuje Jet verzi této databáze" a neoficiální průvodce MDB souhlasí. Informace v těchto zdrojích v kombinaci se záznamem na Wikipedii pro [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) naznačují, že hodnota 0x02 označuje ACE 12 (Access 2007) a 0x03 označuje ACE 14 (Přístup 2010). Minimální databáze vytvořená v Accessu 2010 a podobná databáze vytvořená v Accessu 2016 však mají v tomto umístění 0x02. Minimální databáze vytvořená v Accessu 2016, ale definující sloupec s nově zavedeným datovým typem „large integer“, měla hodnotu 0x05. V souborech ACCDB se zdá, že tento indikátor odráží kompatibilitu souboru spíše než verzi ACE motoru použitého k jeho vytvoření.

## Reference

* [Access File Format](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Specifikace Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Jaký formát souboru Access mám použít?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=cs-cz&rs=cs-cz&ad=us)
