{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru TEX",
  "description":"Další informace o formátu souborů TEX a rozhraních API, která mohou vytvářet a otevírat soubory TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TEX? ##

**TeX** je jazyk, který se skládá z programovacích a také značkovacích funkcí, které se používají k sazbě dokumentů. Donald Knuth ze Stanfordské univerzity je tvůrcem tohoto nápaditého sázecího systému. Po celém světě je TeX nejlepší volbou autorů a vydavatelů pro vytváření vysoce kvalitních technických dokumentů. TeX odvádí vynikající práci při formátování složitých matematických výrazů. Ve spojení s vysoce kvalitním fotosázecím strojem TeX konkuruje výsledkům generovaným nejlepšími tradičními sázecími systémy. Proto je považován za nejklasičtější digitální typografické systémy.

Vstupní soubory TeX jsou založeny na kódu ASCII, což umožňuje sdílení rukopisů mezi autory, manažery vydavatelství a kritiky. TeX podporuje široká škála výpočetních prostředí, téměř každá moderní platforma a mnoho starších platforem. TeX je navíc svobodný software dostupný širokému spektru spotřebitelů. Mnoho instalací UNIX používá UNIX troff i TeX jako svůj formátovací systém pro různé účely. Další sázecí úlohy jsou prováděny ohromně ve formě LaTeXu, ConTeXtu a dalších balíčků maker.

## Stručná historie ##

TeX navrhl a napsal Donald Knuth v roce 1978. Guy Steele z Massachusetts Institute of Technology revidoval vstup/výstup TeXu tak, aby běžel pod nekompatibilním operačním systémem, jako je Timesharing System (ITS). První verze TeXu byla vyvinuta pod operačním systémem Stanford's WAITS v programovacím jazyce (SAIL) a testována pro provoz na PDP-10. Knuth představil myšlenku gramotného programování pro pokročilé verze. Literátní programování je způsob generování kompilovatelného zdrojového kódu a sazby (v TeXu) pro křížově propojenou dokumentaci pomocí původního souboru. Jazyk používaný k vývoji těchto pokročilých verzí TeXu se nazývá WEB, což je směs programů DEC PDP-10 Pascal pro zajištění přenositelnosti.

Revidovaná nová verze TeX publikovaná v roce 1982 a byla nazvána TeX82. Hlavní změnou je nahrazení původního algoritmu dělení slov nově napsaným algoritmem Frankem Liangem. Aby byla zajištěna přenositelnost mezi různými platformami, TeX82 namísto použití s pohyblivou řádovou čárkou používá aritmetiku s pevnou řádovou čárkou spolu se skutečným programovacím jazykem s kompletním Turingem. V roce 1989 byly vydány nové verze TeX a Metafont. Verze 3.0 TeXu tedy umožňuje 8bitové vstupy, což umožňuje 256 různých znaků v textu. Po verzi 3 jsou aktualizace označeny přidáním další číslice na konec desetinné čárky, např. aktuální verze TeXu je označena jako 3.14159265. Tato verze byla naposledy aktualizována 12-1-2014.

## TeXový vstup ##

Vstupní soubor do TEXu lze připravit pomocí textového editoru s použitím běžného textu. Na rozdíl od typického textového procesoru tento vstupní soubor nepovoluje žádné neviditelné řídicí znaky. Jeden soubor lze vložit do jiného souboru, který obsahuje definice maker a pomocné definice, které rozšiřují možnosti TeXu. Pokud je instalace TeXu dodávána s nějakými soubory maker, místní informace o TeXu demonstrují použití souborů maker. Standardní forma TeXu integruje kombinaci maker a dalších definic známých jako plain TEX.

Na základě přesné znalosti velikostí všech znaků a symbolů vypočítá optimální uspořádání písmen na řádku a řádků na stránku. V době zpracování dokumentu je vytvořen soubor .dvi, kde „dvi“ znamená „nezávislý na zařízení“. Pro tisk nebo náhled dokumentu s příponou dvi jsou vyžadovány programy ovladače zařízení. V dnešní době se generování dvi obchází běžně používaným pdf-TeXem. Při instalaci TeXu nejsou k dispozici žádné předchozí znalosti písem, takže k získání informací pro dokument se používají externí soubory písem, které jsou součástí lokálního prostředí TeXu.

## Systém sázení ##

Základním systémem TeX lze porozumět asi 300 primitivům (příkazům). Primitiva jsou nízkoúrovňové příkazy, proto je běžný uživatel používá přímo zřídka a většinu funkcí zajišťují formátové soubory. Tyto formátové soubory jsou předinstalované paměťové obrazy TeXu, po kterých následuje načtení velkých sbírek maker. Původní výchozí formát jazyka, tj. plain TeX, přidává asi 600 příkazů.

Zpětné lomítko seskupené se složenými závorkami označuje začátek příkazů TeXu. Vzhledem k tomu, že TeX je jazyk založený na makrech a tokenech, lze téměř všechny syntaktické vlastnosti TeXu měnit za běhu, včetně těch uživatelsky definovaných, kromě neexpandovatelných tokenů, které jsou pak spuštěny. Samotné rozšíření je prakticky bezproblémové. Některé příkazy musí následovat za argumenty, které pomáhají vysvětlit funkci příkazu. Například příkaz \vskip nařídí TEXu, aby přeskočil stránku dolů/nahoru, následovaný argumentem určujícím, kolik místa se má přeskočit.

## Verze ##

LaTeX je nejčastěji používaný formát, který původně vyvinul Leslie Lamport. LaTeX integruje různé styly dokumentů pro soubory, dopisy, knihy a snímky a nabízí odkazy a automatické číslování pro různé sekce a matematické výrazy. AMS-TeX je další populární formát vyvinutý Americkou matematickou společností.

AMS-TeX nabízí mnohem uživatelsky přívětivější příkazy, které mohou být předefinovány časopisy tak, aby odpovídaly jejich místnímu stylu. LaTeX může využít výhod AMS-TeXu pomocí „balíčků“ AMS, které se pak nazývají AMS-LaTeX. ConTeXt je další formát napsaný Hansem Hagenem používaný hlavně pro DTP.

Software TeX nabízí několik funkcí, které byly v době svého vzniku v jiných sázecích systémech nedostupné nebo méně kvalitní. Některé z inovativních funkcí tohoto jazyka jsou založeny na zajímavých algoritmech odvozených z tezí Knuthových studentů. Zatímco ostatní sázecí programy nyní do svých programů začleňují užitečné funkce TeXu.

## Reference ##

* [Systém sázení TeX](https://en.wikipedia.org/wiki/TeX)

