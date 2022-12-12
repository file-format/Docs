{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Komprimovaný", "Soubor", "Přípona", "Formát souboru", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru LZO",
  "description":"Další informace o formátu souborů LZO a rozhraních API, která mohou vytvářet a otevírat soubory LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Co je soubor LZO? ##

Soubor s příponou .lzo je kombinován s funkcemi archivace souborů, které mohou zmenšit velikost všech souborů v komprimovaném souboru. Všechny komprimované soubory mohou obsahovat jeden nebo více souborů nebo dokonce skupiny pořadačů s několika soubory různých druhů a rozměrů. Velikost komprimovaného souboru je menší ve srovnání se společnou velikostí všech souborů a složek uložených v komprimovaném souboru LZO. Všechny komprimované soubory LZO jsou uloženy ve formátu LZO a jsou explicitně prováděny pomocí kompresních funkcí používaných softwarem pro kompresi a dekompresi souborů LZOP. Všechny specifikace komprese jsou sloučeny do tohoto programu pro kompresi a dekompresi souborů, který pochází z knihovny pro kompresi souborů Lempel-Ziv-Oberhume. Vyšší rychlost dekomprese a vyvinuté kompresní poměry jsou také kombinovány do těchto souborů LZO.

## Specifikace LZO ##

Markus Franz Xaver Johannes Oberhumer vyvinul původní algoritmus „lzop“, založený na dřívějších algoritmech Abrahama Lempela a Jacoba Ziva, v roce 1996. Tato knihovna implementuje řadu algoritmů s následujícími charakteristikami:

* Rychlejší komprese než DEFLATE
* Rychlá dekomprese
* Další vyrovnávací paměti, které jsou potřeba během komprese (velikost 8KB nebo 64KB, v závislosti na úrovni komprese)
* Zdrojové a cílové vyrovnávací paměti představují veškerou paměť potřebnou pro dekompresi
* Poskytuje kontrolu nad kompresním poměrem a rychlostí komprese

Jako blokový kompresní algoritmus LZO provádí překrývající se kompresi i místní dekompresi. Aby bylo dosaženo překrývající se komprese, musí se velikost bloku komprese i dekomprese shodovat. Algoritmus komprese LZO rozděluje vstupní data na shody (posuvný slovník) a literály, které se neshodují, což dává dobré výsledky s vysoce redundantními daty a přijatelné výsledky s nekomprimovatelnými daty, pouze zvyšuje nestlačitelná data o 1/64 původního velikost.

## Problémy s otevřením souboru LZO ##

Následuje několik problémů, které mohou způsobit špatné fungování formátu souboru LZO:
  


* Soubor může být poškozen. Chcete-li tento problém vyřešit, stáhněte soubor znovu nebo požádejte odesílatele o opětovné zaslání souboru
* Druhým důvodem je infikovaný soubor, v tomto případě soubor řádně prohledejte
* Nesprávné odkazy na soubor LZO
* Odstranění popisu LZO
* Nedostatek hardwarových zdrojů
* Zastaralé ovladače zařízení
  


## Reference ##

* [LZO – z Wikipedie](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

