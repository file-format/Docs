{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "soubor", "přípona", "formát souboru", "Soubor pro výměnu dat", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souborů, abyste věděli, co je přípona souboru DIF a rozhraní API, která mohou vytvářet a otevírat soubory DIF.",
  "title" :"DIF - Data Interchange File Format",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor DIF?

DIF je zkratka pro Data Interchange Format, který se používá k importu/exportu tabulkových dat mezi různými aplikacemi. Patří mezi ně Microsoft Excel, OpenOffice Calc, StarCalc a mnoho dalších. Ukládá data obsažená v jedné tabulce, což je jediné omezení tohoto formátu souboru.

## Stručná historie formátu souboru DIF ##

Formát souboru DIF byl vyvinut společností Software Arts, Inc. na počátku 80. let. Specifikace formátu souboru pro DIF byly zahrnuty do VisiCalc, což byl první tabulkový procesor pro osobní počítače. Tyto specifikace byly chráněny autorským právem v roce 1981 a byly registrovanou ochrannou známkou společnosti Software Arts Products Corp.

## Formát souboru DIF ##

DIF ukládá obsah tabulky v textovém souboru ASCII, který umožňuje jeho prohlížení a úpravy pomocí textového editoru. Formát má své místo v seznamu formátů serializace dat pro své charakteristiky výměny dat. Soubor DIF se skládá ze 2 částí; záhlaví a data.

Vše v DIF je reprezentováno 2- nebo 3-řádkovým blokem. Záhlaví získají 3-řádkový blok; údaje, 2.

* Části záhlaví začínají textovým identifikátorem, který obsahuje velká písmena, pouze abecední znaky a má méně než 32 písmen. Následující řádek musí být dvojice čísel a třetí řádek musí být řetězec v uvozovkách.
* Datové bloky začínají dvojicí čísel a další řádek je řetězec v uvozovkách nebo klíčové slovo.

### Hodnoty ###

Hodnota zabírá dva řádky, na prvním je dvojice čísel a na druhém je řetězec nebo klíčové slovo. První číslo z dvojice označuje typ:

* −1 – typ direktivy, druhé číslo je ignorováno, následující řádek je jedním z těchto klíčových slov:
** BOT – začátek n-tice (začátek řádku)
** EOD – konec dat
* 0 – číselný typ, hodnota je druhé číslo, následující řádek je jedním z těchto klíčových slov:
** V – platné
** NA – není k dispozici
** ERROR – chyba
** TRUE – skutečná booleovská hodnota
** FALSE – falešná booleovská hodnota
* 1 – typ řetězce, druhé číslo je ignorováno, následující řádek je řetězec v uvozovkách

### DIF Header chunk ###

Část záhlaví souboru DIF se skládá z řádku identifikátoru následovaného dvěma řádky hodnoty. Číselné hodnoty v blocích záhlaví používají místo klíčových slov platnosti pouze prázdný řetězec. Podrobnosti o těchto částech záhlaví jsou následující.

* TABLE - za verzí následuje číselná hodnota, nepoužívaný druhý řádek hodnoty obsahuje komentář generátoru
* VEKTORY - následuje počet sloupců jako číselná hodnota
* TUPLES - následuje počet řádků jako číselná hodnota
* DATA - za fiktivní číselnou hodnotou 0 následují data pro tabulku, každému řádku předchází hodnota BOT, celá tabulka je ukončena hodnotou EOD

### Příklad DIF ###

Následující příklad ukazuje obsah jednoduchého listu a jeho ekvivalentní DIF reprezentaci.


|Jméno|Věk
---|---|
|Bob|34
|List|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Reference ##

* [ DIF – z Wikipedie](https://en.wikipedia.org/wiki/Data_Interchange_Format)

