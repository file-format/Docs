{
  "date" : "2019-10-11",
  "keywords" :[ "soubor md", "formát souboru md", "co je soubor md", "soubor", "příklad md", "přípona souboru md", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown Language File",
  "description":"Další informace o formátu souboru MD a rozhraních API, která mohou vytvářet a otevírat soubory MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor MD?

Textové soubory vytvořené dialekty jazyka Markdown se ukládají s příponou **.md** nebo **.MARKDOWN**. Soubory MD se ukládají ve formátu prostého textu, který používá jazyk Markdown, který také obsahuje vložené textové symboly, které definují, jak lze formátovat text, jako jsou odsazení, formátování tabulek, písma a záhlaví. Soubory MD lze převést do HTML pomocí programu Markdown. Jazyk Markdown vydává John Gruber.

Soubory MD lze také kategorizovat jako vývojářské soubory, které většinou používá Markdown, pro převod textových souborů na verze HTML, aby uživatelé mohli vytvářet soubory, které se snadno čtou a zapisují. Níže jsou uvedeny aplikace, které mohou otevřít soubor .md:

* Microsoft Poznámkový blok
* Poznámkový blok 2
* Apple TextEdit
* Microsoft WordPad

Pozor, nepřejmenovávejte příponu souborů .md. Pokud ano, nezmění se typ souboru, protože jsou k dispozici speciální konverzní software pro změnu souboru z jednoho typu na druhý. Jak je uvedeno výše, soubory .MD jsou přípony souborů vytvořených v softwaru jazyka Markdown. **Markdown** je [odlehčený značkovací jazyk](https://en.wikipedia.org/wiki/Lightweight_markup_language) určený k jednomu účelu, k formátování textu na webu pomocí syntaxe formátování prostého textu. Aby bylo jasné, že Markdown není náhradou HTML, protože jeho syntaxe je velmi malá a obsahuje velmi malou podmnožinu HTML značek. Důvodem Markdownu je usnadnit čtení, psaní a úpravy prózy. Jinými slovy můžeme říci, že HTML je formát pro publikování, zatímco Markdown je formát pro psaní.

Markdown je nyní jedním z nejpopulárnějších značkovacích jazyků na světě. Při používání aplikace Microsoft Word se slova a fráze formátují kliknutím na tlačítka a změny jsou okamžitě viditelné. Ale Markdown takový není. Když je vytvořen soubor ve formátu Markdown, je k textu přidána syntaxe Markdown, která označuje, která slova a fráze mohou vypadat jinak. Například pro zobrazení nadpisu se před něj přidá znak čísla (např. # Nadpis jedna). Pro vytvoření tučné věty se před a za ní přidají dvě hvězdičky (např. **tento text je tučný**). Syntaxi Markdown lze po chvíli vidět v textu.

## Stručná historie

John Gruber a Aaron Swartz v roce 2004 vytvořili jazyk Markdown s myšlenkou umožnit lidem „psát pomocí snadno čitelného a zapisovatelného formátu prostého textu as možností převodu do XHTML nebo HTML. Cílem za jeho designem je čitelnost – jazyk je čitelný tak, jak je, aniž by vypadal, jako by byl označen nebo přidán s pokyny pro formátování, jako je tomu ve značkovacích jazycích, jako je RTF nebo HTML, kde jsou značky a pokyny pro formátování zřejmé. Základní inspirací je použití stávajících konvencí pro označování prostého textu v e-mailu.

Od té doby byl Markdown znovu implementován ostatními, stejně jako v [modulu] v Perlu (https://en.wikipedia.org/wiki/Modular_programming) dostupném na [CPAN](https://en.wikipedia.org/ wiki/CPAN) a v různých dalších programovacích jazycích. Je distribuován pod [licence ve stylu BSD](https://en.wikipedia.org/wiki/BSD_license) a je součástí nebo je dostupný jako plugin pro několik [systémů pro správu obsahu](https:// en.wikipedia.org/wiki/Content_management_system).

## Technické specifikace

Když je něco napsáno v Markdown, text se nejprve uloží do souboru ve formátu prostého textu s příponou .md nebo .markdown, poté se ke zpracování souboru Markdown použije aplikace markdown, jako je Dillinger, aby se text ve formátu Markdown převedl do HTML pro zobrazení na webu. prohlížeče. Aplikace Markdown používají //Markdown procesor// (také běžně označovaný jako „analyzátor“ nebo „implementace“) k převzetí textu ve formátu Markdown a jeho výstupu do formátu HTML. Vývojový diagram procesu je následující:

Stručně řečeno, jde o čtyřkrokový proces takto:

1. Nejprve vytvořte soubory Markdown pomocí textového editoru nebo aplikace Markdown s příponou .md nebo .markdown.
1. Soubor Markdown se poté otevře v aplikaci Markdown.
1. Aplikace Markdown se používá k převodu souboru Markdown na dokument HTML.
1. Soubor HTML se poté zobrazí ve webovém prohlížeči nebo se použije aplikace Markdown k jeho převedení do jiného formátu souboru, jako je PDF.

Markdown umožňuje rychle a snadno dělat poznámky, psát obsah pro webové stránky, vytvářet dokumenty připravené k tisku, publikovat knihy, vytvářet prezentace a vytvářet dokumenty.

Některé verze v markdown měly podstatný dopad na jiné verze natolik, že je často uvidíte citované jako součást jiných verzí. Např. knihovny zmiňují podporu CommonMark (GFM). Pojďme se na ně krátce podívat.

### GFM
Markdown je u vývojářů tak oblíbený, protože platforma pro sdílení open source Github přijala a rozšířila jazyk o verzi nazvanou Github Flavored Markup (GFM), která zahrnuje chráněné kódové bloky, URL aultlinking, přeškrtnutí, tabulky a vytváření úkolů.

### Společná značka
Vývojáři Markdown se nedávno pokusili standardizovat markdown, spojili se, aby vytvořili verzi, testy a dokumentaci pro jazyk, který je robustnější a nazývá se CommonMark. Tento formát je trochu nový a nepodporuje mnoho funkcí, ale brzy bude přidáno mnoho funkcí MultiMarkdown.

### Vícenásobné značení
Multi-Markdown přidal do jazyka různé funkce, které jsou podporovány jinými verzemi. Původně byl napsán v Perlu, ale později se přesunul do C. Podporuje chráněné kódové bloky, zvýrazňování syntaxe, tabulky, metadata, odkazy na fragmenty/křížové odkazy, poznámky pod čarou, přeškrtnutí, seznamy definic, matematiku.

## Reference

* [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

