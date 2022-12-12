{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "soubor", "přípona", "formát souboru", "Excel", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souboru, abyste věděli, co je soubor XLS a rozhraní API, která je mohou vytvořit a otevřít.",
  "title" :"Co je formát souboru XLS? Učte se od odborníků na formát souborů!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Co je soubor XLS?

Soubory s příponou XLS představují binární formát souboru Excel. Takové soubory lze vytvořit v aplikaci Microsoft Excel i v jiných podobných tabulkových programech, jako je OpenOffice Calc nebo Apple Numbers. Soubor uložený aplikací Excel je známý jako sešit, kde každý sešit může mít jeden nebo více listů. Data se ukládají a zobrazují uživatelům ve formátu tabulky v listu a mohou zahrnovat číselné hodnoty, textová data, vzorce, externí datová připojení, obrázky a grafy. Aplikace jako Microsoft Excel vám umožňují exportovat data sešitu do několika různých formátů včetně [PDF](/cs/pdf/), [CSV](/cs/tabulkový procesor/csv/), [XLSX](/cs/tabulkový procesor/xlsx/), [TXT](/cs/ word-processing/txt/), [HTML](/cs/web/html/), [XPS](/cs/page-description-language/xps/) a několik dalších. Formát souboru XLS byl s vydáním aplikace Microsoft Excel 2007 nahrazen otevřenějším a strukturovanějším formátem XLSX. Nejnovější verze stále poskytují podporu pro vytváření a čtení souborů XLS, ačkoli XLSX je nyní první volbou použití.

## Stručná historie

XLS byl vytvořen společností Microsoft pro použití s aplikací Microsoft Excel a je také známý jako Binary Interchange File Format (BIFF). Tento typ souboru byl poprvé představen tím, že byl součástí Excelu pro Windows v roce 1987. Specifikace formátu souboru XLS byly poprvé zveřejněny v červnu 2008 jako revize 1. Poté byly specifikace průběžně aktualizovány a byla k dispozici nejnovější revize je ze srpna 2018, která je označena jako revize 8.0. Stručná historie různých verzí formátu souboru XLS je následující:

* Verze 7.0 (vydaná s Office 95): Tato verze excelu byla nejrobustnější a rychlejší ze všech verzí a interní přepisy streamu byly aktualizovány na 32 bitů.
* Verze 8 (vydaná s Office 97): VBA byl představen jako standardní jazyk a do této verze byly poprvé začleněny odstraněné popisky přirozeného jazyka. Poprvé také představil kancelářského pomocníka na kancelářské sponky.
* Verze 9 (Vydáno s Office 2000): Ve verzi 9 došlo pouze k drobným změnám, kde kancelářský asistent kancelářské sponky mohl současně držet více objektů, což dříve nebylo možné.
* Verze 10 (vydaná s Office XP): Tato verze neobsahovala žádné výrazné vylepšení.
* Verze 11 (Vydáno s Office 2003): Hlavní aktualizací ve verzi 11, Excel 2003 bylo zavedení nových tabulek.

## Specifikace formátu souboru XLS ##

Data jsou uspořádána v souboru XLS jako binární proudy ve formě složeného souboru, jak je popsáno v [MS-CFB]. Data jsou uložena ve složeném souboru pomocí úložišť, proudů a dílčích proudů, které obsahují informace o obsahu a struktuře sešitu, včetně dat sešitu, jako jsou definice listů. Každý proud nebo dílčí proud obsahuje řadu binárních záznamů. Každý binární záznam obsahuje nula nebo více strukturovaných polí, která obsahují data sešitu. Tato část poskytuje stručný přehled struktury souborů XLS, ale pro podrobné specifikace formátu souboru je nutné nahlédnout do [Specifikace vytváření souborů XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) dokument společnosti Microsoft.

#### Stream a substream ####

Sešit je reprezentován proudem sešitu. Každý list v sešitu je reprezentován dílčími proudy. Kromě toho má dílčí proud tabulky grafů, dílčí proud listu maker nebo dílčí proud dialogového listu, který následuje po globálním dílčím proudu. Každý binární proud nebo dílčí proud, který obsahuje data sešitu, MUSÍ být zapsán jako řada binárních záznamů.

#### Záznam ####

Informace o funkcích v sešitu jsou uloženy jako záznam, který je posloupností bajtů s proměnnou délkou. Binární záznam se skládá z následujících tří složek:

**Typ záznamu:** Typ záznamu je dvoubajtové celé číslo bez znaménka, které určuje, jaký typ informace je specifikován záznamem a jak je uspořádána a strukturována struktura dat záznamu specifických pro tento záznam. Hodnoty typu záznamu MUSÍ být hodnotami z Výčtu záznamů (část 2.3) nebo záznam MUSÍ využívat architekturu budoucího záznamu (část 2.1.6).

**Velikost záznamu**: Velikost záznamu je dvoubajtové celé číslo bez znaménka, které určuje počet bajtů, které určuje celkovou velikost dat záznamu. Velikost záznamu MUSÍ být větší nebo rovna 0 a MUSÍ být menší nebo rovna 8224.

**Data záznamu:** Složka dat záznamu obsahuje pole, která odpovídají konkrétnímu typu záznamu a tvoří zbytek záznamu. Pořadí a struktura polí pro daný typ záznamu je specifikována v odpovídající sekci pro daný typ záznamu. Velikost složky dat záznamu MUSÍ být rovna velikosti záznamu. Pole v komponentě dat záznamu mohou obsahovat jednoduché hodnoty, pole hodnot, struktury několika polí, pole polí a pole struktur.

#### Tabulka buněk ####

Buňky jsou základní bloky sešitu, které ukládají obsah sešitu, jako je text, vzorce a číselná data. Buňky uchovávají záznam o uložených datech prostřednictvím datové struktury nazývané tabulka buněk. Samotná tabulka buněk je uložena v sekvenci záznamů, které odpovídají pravidlům CELLTABLE definovaným v dokumentu specifikací. Skládá se z řady řadových bloků, kde jsou řady uspořádány do řadových bloků. Každý blok řádků obsahuje řádky od prvního řádku obsahujícího data po poslední řádek obsahující data.

Formátování dat nebo řádků je uloženo v záznamu řádku pro každý blok řádku. Každá buňka, která obsahuje data nebo formátování jednotlivých buněk, je reprezentována záznamem. Formátování spojené s buňkou lze odvodit z formátování jednotlivých buněk, formátování řádků, formátování sloupců nebo výchozího formátu buňky. Pořadí priority pro formátování je formátování jednotlivých buněk s nejvyšší prioritou, následuje formátování řádků a poté formátování sloupců a poté výchozí formát buňky. Buňky, které neobsahují data a neobsahují individuální formátování, se neukládají.

#### Vzorce ####

Vzorec je posloupnost hodnot, odkazů na buňky, názvů, funkcí nebo operátorů v buňce, které dohromady vytvářejí novou hodnotu. Vzorce jsou uloženy v tokenizované reprezentaci známé jako „analyzované výrazy“. Analyzovaný výraz je za běhu převeden na textový vzorec pro zobrazení a úpravy uživatele. Vzorce buněk jsou určeny záznamem Vzorec. Vzorce pole jsou určeny záznamem Array. Sdílené vzorce jsou určeny záznamem ShrFmla.

#### Grafy ####

List s grafem určuje graf, grafiku, která zobrazuje data nebo vztahy mezi sadami dat ve vizuální podobě, a mezipaměť dat grafu, místní kopie dat, která se používají v datech grafu, chybí nebo pokud jsou odkazy na externí zdroje dat jsou nefunkční. Graf určuje jednu nebo dvě skupiny os, sadu os, proti kterým jsou vykreslena data grafu, a sadu řad, trendových linií a chybových pruhů určených v grafu. Každá skupina os určuje jednu až čtyři skupiny grafů, které určují typ vizualizace použité k zobrazení dat. Každá řada, spojnice trendu a chybový pruh určují skupinu grafů, ke které jsou přidruženy.

#### Metadata ####

Metadata jsou další data spojená s konkrétní buňkou nebo jejím obsahem. Metadata jsou zaznamenána v BIFF8 pouze pro účely budoucí rozšiřitelnosti.

#### kontingenční tabulky ####

Kontingenční tabulka je mechanismus pro shrnutí zdrojových dat, abyste získali přehled o distribuci těchto dat. V kontingenční tabulce se příslušné sloupce zdrojových dat stanou poli, která lze použít k sumarizaci dat. Když jsou zdrojová data kontingenční tabulky zdrojová data OLAP, hierarchie OLAP a některé další entity OLAP se stanou poli v kontingenční tabulce.
Kontingenční tabulka má dvě hlavní části, kontingenční mezipaměť a zobrazení kontingenční tabulky. Může existovat více zobrazení kontingenční tabulky založené na jedné kontingenční mezipaměti jiné než OLAP.

#### Styly ####

Tento přehled popisuje, jak jsou zadány informace o formátování a ochraně buněk v listu (1). Formátování buněk se skládá z několika sad vlastností:

* Vlastnosti písma (tučné, kurzíva, barva písma, velikost písma atd...)
* Vlastnosti výplně (barva popředí, barva pozadí, vzor, přechod atd...)
* Vlastnosti zarovnání (zarovnání vlevo, na střed, vpravo atd...)
* Vlastnosti ohraničení (levý, pravý, horní, spodní, tlustý nebo tenký, barva atd.)
* Vlastnosti formátování čísel (datum, čas, počet desetinných míst atd.)
* Vlastnosti ochrany (uzamčené, skryté atd.)

Tyto vlastnosti jako celek popisují způsob zobrazení a tisku konkrétní buňky.

## Reference ##

* [[MS-XLS] – struktura binárního formátu souboru Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] – Binární formát složeného souboru](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

