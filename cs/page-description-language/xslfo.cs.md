{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Objekty formátování XSL", "Soubor", "Rozšíření", "Formát souboru", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Další informace o formátu souborů XSLFO a rozhraních API, která mohou vytvářet a otevírat soubory XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor XSL-FO? ##

XSL-FO (XSL Formatting Objects) je výkonný stylový jazyk pro formátování dokumentů XML. Sémantika ohraničené formy papíru a tisku je vyjádřena pomocí XSL-FO, když jsou rozměry pevně dané. Na rozdíl od HTML, které představuje sémantiku neohraničené podoby okna prohlížeče s proměnnými rozměry. XML dokumenty formátované XSL-FO se většinou používají pro generování PDF souborů. XSL (Extensible Stylesheet Language) je sada technologií W3C s kompletními funkcemi určených k navrhování pro formátování a výměnu dokumentů XML a XSL-FO části tohoto jazyka. XSLT a XPath jsou také další části XSL.

Navrhuje se, aby XML dokumenty byly nejprve transformovány do XSL-FO, PDF je příkladem tohoto kritéria. V PDF se výsledky vykreslují pomocí XSLTfirst a poté XSL-FO formátovače. Tímto způsobem mohou být dokumenty XML formátovány náhodně. Ačkoli XSL-FO využívá výhody kaskádových stylů (CSS) a rozšiřuje je tam, kde je to nutné pro skutečný formát, obsahuje poskytování šablon stránek nazývaných předlohy stránek v terminologii XSL-FO. XSL-FO také poskytuje formátování pro poměrně sofistikované dokumenty a podporuje generování indexů.

## Historie a základní pojmy ##

V lednu 2012 byl naposledy aktualizován Pracovní návrh XSL-FO a v listopadu 2013 byla jeho Pracovní skupina uzavřena. Šablona stylů XSL specifikuje prezentaci třídy dokumentů XML tím, že popisuje, jak je instance třídy transformována do dokumentu XML, který používá slovník formátování. XSL-FO je integrovaný prezentační jazyk a nemá žádné sémantické značky, které se používají v HTML. Navíc tento jazyk ukládá všechna data dokumentu v sobě, na rozdíl od CSS, které mění výchozí nastavení externího dokumentu HTML nebo XML.

Obecným kritériem použití XSL-FO je, že uživatel píše dokument v jazyce XML spíše než ve FO. Poté dojde k transformaci XSLT. Tato XSLT transformace je zodpovědná za převod XML na XSL-FO. Jakmile je dokument XSL-FO vygenerován, je předán aplikaci zvané zpracovatel FO. Zpracovatelé FO jsou zodpovědní za přeměnu tohoto dokumentu na čitelný i tisknutelný dokument. Soubory PDF nebo PS jsou příklady nejběžnějšího výstupu XSL-FO. Ale to neznamená, že FO procesor může produkovat pouze tyto dva typy formátu jako výstup. Některé FO procesory mohou mít výstup v souborech RTF nebo se dokonce může objevit okno v uživatelském GUI, toto okno zobrazuje sekvenci stránek a jejich obsah.

Dokument XSL-FO se liší od PDF nebo PS v tom smyslu, že v konečném důsledku nedefinuje rozložení textu na různých stránkách. Možná stylizuje stránky a určuje místa pro zobrazení obsahu. Zpracovatel FO navíc uspořádá text v mezích určených dokumentem FO. Tato specifikace dokonce umožňuje různým FO procesorům chovat se podle výsledně vytvořených stránek. Příkladem takového chování je dělení slov, jen málo procesorů FO dokáže dělit slova, aby se ušetřilo místo při zalomení řádku, zatímco některé procesory tuto možnost nevyberou. Záleží na procesorech, aby zvolili různé algoritmy dělení slov, které odpovídají jejich požadavkům. Tyto algoritmy dělení slov mohou být velmi jednoduché nebo možná složitější. V některých situacích specifikace XSL-FO výslovně schvaluje procesory FO, což je určitý stupeň volby v kontextu rozvržení.

Tato variace mezi procesory FO generuje různé výsledky, o které se procesory často nezajímají. Protože obecným zaměřením XSL-FO je produkovat stránkované/tištěné dokumenty. Samotné dokumenty XSL-FO obvykle fungují jako prostředníci, jejich hlavní funkcí je generovat buď soubory PDF, nebo dokument, který lze vytisknout jako výstup k distribuci. V HTML/CSS nebo XSL-FO distribuce PDF jako konečný výsledek namísto zadávání formátovacího jazyka znamená, že příjemci zůstávají nedotčeni výslednou všestranností, která je způsobena rozdíly mezi interprety formátovacího jazyka. Na druhou stranu je evidentní, že neexistuje jednoduchý způsob, jak dokument splnit různé potřeby příjemců, např. variabilní velikost stránky nebo požadovanou velikost písma nebo přizpůsobení pro stránku nebo tisk.

## Formát souboru XSLFO ##

Dokumenty SL-FO jsou v podstatě dokumenty XML, ale neřídí se žádným schématem. Místo toho se dokumenty SL-FO řídí syntaxí definovanou ve specifikaci jejich vlastního jazyka. V každém dokumentu XSL-FO jsou vyžadovány dvě sekce:

1. Sekce, která určuje seznam rozvržení stránek se štítky.
1. Sekce se všemi podrobnostmi o datech dokumentu s označením, která určuje zobrazení obsahu na různých stránkách prostřednictvím různých rozvržení stránek.

Vlastnosti stránky jsou uvedeny v rozvrženích stránky, které mohou definovat organizaci textu tak, aby odpovídala konvencím pro konkrétní jazyk. Kromě toho velikost stránky, jejich okraje a sekvence stránek (které schvalují různé vlastnosti pro liché a sudé stránky) jsou také definovány rozvržením stránky.

Datová část dokumentu je rozdělena do řady toků, kde každý tok je připojen k rozvržení stránky. Toky uzavírají seznam bloků v nich. Tento seznam bloků může obsahovat vložené značkovací funkce nebo seznam textových dat nebo možná obojí současně. Okraje dokumentu mohou také zobrazovat čísla stránek nebo nadpisy kapitol. Funkčnost bloků i vložených prvků zůstává stejná jako v CSS, přesto se některá pravidla pro výplň a okraje mezi FO a CSS liší.

Směr orientace stránky je zcela určen pro rozšíření bloků a řádků, takže dokumenty FO fungují pod jazyky odlišnými od angličtiny. Jazyk specifikace FO používá pro popis směrů slova začátek a konec spíše než doleva a doprava. Základní značení obsahu XSL-FO a pravidla kaskádování jsou převzata z CSS. Jazyk XSL-FO souhlasí s následujícími specifikacemi.

## Více sloupců ##

Stránka může mít více sloupců a bloků a ve výchozím nastavení se může rozšiřovat z jednoho sloupce do druhého. Více stránek může mít různé šířky a počty sloupců. Všechny charakteristiky FO se řídí limity stránky s více sloupci.

### Seznamy ###

Seznam XSL-FO je založen na dvou sadách bloků uspořádaných lícem k čelisti. Koncepčně v seznamu blok vlevo označuje číslo, odrážku nebo řetězec textu, zatímco blok na pravé straně může fungovat podle očekávání. Číslování seznamů XSL-FO se obvykle provádí pomocí XSLT.

### Stoly ###

Tabulka FO je podobná tabulce HTML/CSS. Uživatel si může vybrat řádky dat, informace o stylu, barvu pozadí pro každou jednotlivou buňku. Pomocí odlišných informací o stylu má uživatel oprávnění vybrat první řádek jako řádek záhlaví tabulky. Procesor FO může být explicitně informován o specifikaci prostoru každého sloupce nebo automaticky přizpůsobit text do tabulky.

### Indexování ###

XSL-FO 1.1 má funkce, které pomáhají generovat index prostřednictvím odkazování na správně označené prvky.

### Výhody ###

* Vhodné pro publikování založené na obsahu
* Snadnost použití
* Nízké náklady

## Reference ##

* [Co je XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Objekty formátování XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

