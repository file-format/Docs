{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "rozšíření", "soubor", "formát", "systém", "soubor TMP", "dokumenty TMP", "soubory TMP", "Dočasný soubor", "aplikace", "programy" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - dočasný formát souboru",
  "description":"Další informace o formátu souboru TMP a rozhraních API, která mohou vytvářet a otevírat soubory TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Co je soubor TMP? ##

Soubor TMP označuje dočasnou zálohu, úložiště nebo jiný souborový systém vygenerovaný softwarovým programem. Občas je vytvořen jako neviditelný soubor a je často zničen při ukončení programu. Soubory TMP lze také použít k dočasnému uložení informací při vytváření nového souboru.

## Formát souboru TMP ##

Soubor TMP se obvykle skládá z nezpracovaných dat, která se používají jako fáze procesu převodu materiálu z jednoho stylu do druhého. Microsoft Word a Apple Safari jsou dvě aplikace, které mohou vytvářet a používat formát souboru TMP.

Vygenerované dokumenty TMP by měly být teoreticky automaticky odstraněny při zavření programu nebo vypnutí stroje. V praxi tomu tak vždy není. Výsledkem je, že při procházení dokumentů vašeho programu můžete narazit na přechodné soubory, které systém ani žádný jiný software aktivně nepoužívá.

### Pomocná paměť ###

Virtuální paměť se používá v operačních systémech, ale programy, které využívají velké objemy informací, mohou potřebovat vytvořit dočasné dokumenty.

### Meziprocesová komunikace ###

Většina operačních systémů poskytuje primitiva pro předávání dat mezi programy, jako jsou roury, sokety nebo hlavní paměť, ale nejjednodušší metodou je přenést soubory do dočasného souboru a informovat přijímající aplikaci o umístění dočasného souboru.


## Technická specifikace ##

Získání charakteristických názvů dočasných dokumentů obvykle zajišťují operační systémy a softwarové programy.
Dočasné soubory lze bezpečně generovat na systémech POSIX pomocí funkcí knihovny mkstemp nebo tmpfile. Některé systémy zahrnují předchozí aplikaci POSIX (od té doby) mktemp. Tyto soubory se obvykle nacházejí v běžném dočasném adresáři na platformách Unix v /TMP nebo %TEMP% (je specifické pro přihlášení) na počítačích se systémem Windows.

Když se program zastaví nebo se dokument zavře, přechodný soubor vygenerovaný pomocí tmpfile se automaticky odstraní. GetTempFileName (Windows) nebo tmpnam (POSIX) lze použít k vytvoření dočasného názvu souboru, který bude trvat déle než program, který jej vytvořil.

## reference ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
