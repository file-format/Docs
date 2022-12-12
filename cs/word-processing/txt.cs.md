{
  "date" : "2019-10-11",
  "keywords" :[ "txt soubor", "formát souboru txt", "co je soubor txt", "soubor", "příklad txt", "přípona souboru txt", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - soubor textového dokumentu",
  "description":"Další informace o formátu souboru TXT a rozhraních API, která mohou vytvářet a otevírat soubory TXT.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TXT?

Soubor s příponou .TXT představuje textový dokument, který obsahuje prostý text ve formě řádků. Odstavce v textovém dokumentu jsou rozpoznány podle konce řádku a slouží k lepšímu uspořádání obsahu souboru. Standardní textový dokument lze otevřít v libovolném textovém editoru nebo aplikaci pro zpracování textu na různých operačních systémech. Veškerý text obsažený v takovém souboru je ve formátu čitelném pro člověka a je reprezentován sekvencí znaků.

Textové soubory mohou ukládat velké množství dat, protože velikost obsahu není nijak omezena. Textové editory otevírající tak velké soubory však musí být chytré, aby je mohly načítat a zobrazovat. Téměř všechny operační systémy jsou dodávány s textovými editory, které umožňují vytvářet a upravovat textové soubory. Například operační systém Windows je pro tento účel dodáván s programem Poznámkový blok a Wordpad. Podobně MacOS přichází s TextEdit pro vytváření a úpravy textových dokumentů. Na internetu jsou však k dispozici i další bezplatné textové editory, které vám poskytují možnost pracovat s textovými dokumenty, jako je Notepad++, který je z hlediska funkčnosti mnohem pokročilejší.

## Specifikace formátu souboru ##

Formát textového souboru nemá žádné speciální specifikace formátu souboru. Textové soubory mají typ MIME "text/plain" a mají malé nebo žádné formátování. To umožňuje textovým editorům otevřít takové soubory bez dalších požadavků. Výchozí znaková sada textových souborů je ASCII, která se používá pro vytváření a zobrazování obsahu textových souborů. Znaky jsou kódovány pomocí znakové sady ASCII, ale to omezuje použití znaků, jako je znak libry, dolaru a eura, které nelze zapsat pomocí znakové sady ASCII. Textové soubory lze tedy ukládat i ve formátu Unicode, přičemž nejčastěji se používá UTF-8.

### Formát textového souboru Windows ###

Textové soubory v OS Windows se skládají z několika řádků, kde každý řádek je tvořen posloupností znaků. Každý řádek předpokládaný uživatelem je definován kombinací dvou znaků, tj. návrat vozíku (CR) a posun řádku (LF). Textové soubory Windows mohou být v kódování ANSI, OEM, Unicode nebo UTF-8. Kódování UTF-16 pomáhá uložit informace v textovém souboru, který vyžaduje dva bajty pro reprezentaci. Takové soubory obvykle začínají značkou Byte Order Mark (BOM), která sděluje endianness obsahu souboru. Je třeba poznamenat, že jiné aplikace v operačním systému Windows mohou ukládat informace ve formátu textového souboru, ale s různými příponami souborů, které představují text specifický pro aplikaci. Například programovací jazyky obvykle ukládají kód do textového souboru, ale s vlastními příponami.

### Unixový formát textového souboru ###

Všechny tyto systémy upřesňují textový soubor jako soubor, jehož znaky jsou uspořádány do nula nebo více řádků. Každý řádek je posloupnost nula nebo více znaků, které nejsou novým řádkem, a znak konce nového řádku, obvykle LF.

## Reference ##

* [Formát souboru TXT](https://en.wikipedia.org/wiki/Text_file)

