{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PDF/UA",
  "description":"Další informace o formátu souborů PDF/UA a rozhraních API, která mohou vytvářet a otevírat soubory PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co je soubor PDF/UA? #

PDF/UA byl publikován jako [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) v srpnu 2012 a je zdaleka první kompletní definicí sady požadavků na univerzálně přístupné dokumenty PDF. Pojem „univerzálně přístupný“ se vztahuje k pochopení, že informace obsažené v dokumentu [PDF](/cs/pdf/) by měly být stejně a nezávisle přístupné všem obecně a lidem se zdravotním postižením zvláště. Zavedení standardu PDF/UA lze považovat za významný krok pro vytváření nástrojů a aplikací za účelem vytváření a čtení obsahu PDF.

## Požadavky na formát souboru ##

PDF/UA má ve své podstatě určité určité požadavky, které fungují jako podstata tohoto standardu. V podstatě jsou založeny na tagování PDF, což znamená, že všechny dokumenty PDF/UA musí být správně tagovány. Vyžaduje také, aby značky byly sémanticky vhodné a v logickém pořadí. To zajišťuje, že koncový dokument vytvořený se specifikací PDF/UA je spolehlivější a přístupnější. To může přivést autory PDF k otázce, zda potřebují vědět vše o všech těchto požadavcích? Naštěstí tomu tak není, protože nástroje pro shodu PDF/UA přebírají odpovědnost za přidání a zachování dostupnosti PDF.

Požadavky na formát souboru pro PDF/UA jsou následující.

* Obsah je kategorizován jedním ze dvou způsobů: smysluplný obsah a artefakty, jako jsou dekorativní prvky stránky. Veškerý smysluplný obsah musí být označen a integrován do stromu struktury všech značek v dokumentu. Artefakty na druhou stranu stačí jako takové označit.
* Smysluplný obsah musí být označen tagy a spolu s ostatními tagy v dokumentu vytvořit kompletní strom struktury.
* Smysluplný obsah musí být označen příslušnými sémantickými značkami.
* Strom struktury vytvořený značkami dokumentu musí odrážet logické pořadí čtení dokumentu.
* Lze použít pouze standardní značky definované v PDF 1.7; jsou-li použity jiné značky, musí položka přiřazení role zaznamenat, kterou standardní značku každá z nich představuje.
* Informace nesmí být přenášeny pouze vizuálními prostředky (např. kontrast, barva nebo umístění na stránce).
* Není povoleno žádné blikání, blikání nebo blikající obsah, ať už jako efekty ovládané JavaScriptem, ani jako součást jakýchkoli videí vložených do PDF.
* Musí být uveden název dokumentu a dokument musí být nastaven tak, aby se název (spíše než název souboru) objevil v záhlaví okna.
* Jazyk veškerého obsahu musí být uveden a změny jazyka musí být jako takové výslovně označeny.

## Shoda PDF/UA ##

Standard PDF/UA definuje specifikace pro obsah, čtečky a asistenční technologie. Tyto tři aspekty jsou vzájemně propojeny na základě obsahu dokumentu. Požadavky na shodu pro každý z nich jsou uvedeny níže.

## Vyhovující soubory ##

Soubory vyhovující standardu PDF/UA by měly obsahovat funkce, které jsou platné podle [specifikace PDF 1.7](http://www.adobe.com/go/pdfreference). Nicméně funkce, které jsou zakázány konkrétně PDF/UA, by měly být vyloučeny.

## Konformní čtenáři ##

Čtenář, který je v souladu, se musí řídit pravidly stanovenými ve specifikacích PDF 1.7. Konkrétně by měl podporovat:

* všechny značky, atributy a hodnoty klíčů určené pro usnadnění. Měl by mít také schopnost zpracovávat a reprezentovat digitální podpisy, anotace a volitelný obsah.
* zpracovávat a reprezentovat digitální podpisy, anotace a volitelný obsah
* procházet dokument různými způsoby

## Vyhovující asistenční technologie ##

Pro podporu funkcí PDF/UA je vázána odpovídající asistenční technologie. Patří mezi ně například vlastnosti obsahu a čtečky a měly by umožňovat navigaci podle štítků stránek, struktury dokumentu nebo osnovy. Mělo by také umožnit uživateli přepsat výchozí přiblížení navigace.

## Reference ##

* [PDF/UA – z Wikipedie](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA v kostce](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

