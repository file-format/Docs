{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "základy" ],
  "description":"Portable Document Format (PDF) je standardní reprezentace dokumentů nezávislá na softwaru, hardwaru a OS. Mezi standardy PDF patří PDF/A, PDF/E, PDF/UA, PDF/VT a PDF/X.",
  "title" :"Formát souboru PDF - Co je soubor PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) je typ dokumentu vytvořený společností Adobe již v 90. letech minulého století. Účelem tohoto formátu souboru bylo zavést standard pro reprezentaci dokumentů a dalších referenčních materiálů ve formátu, který je nezávislý na aplikačním softwaru, hardwaru i operačním systému. Formát souboru PDF má plnou schopnost obsahovat informace jako text, obrázky, hypertextové odkazy, pole formuláře, multimédia, digitální podpisy, přílohy, metadata, geoprostorové prvky a 3D objekty, které se mohou stát součástí zdrojového dokumentu.

Ve většině případů jsou existující dokumenty převedeny do PDF, nikoli vytvoření nového PDF od začátku. To však neznamená, že neexistuje žádný software pro vytváření nebo manipulaci se soubory PDF.

**(Musíte se podělit o něco o formátu PDF? Své poznatky můžete zveřejnit v sekci [Zprávy o formátu PDF](https://news.fileformat.com/t/PDF).)**

## Formát souboru PDF - Stručná historie

Rychlý přehled časové osy o vytváření souboru PDF z hlediska časové osy je následující:

**1993** – Společnost Adobe Systems zpřístupnila specifikace PDF zdarma

**2008** – PDF byl vydán jako otevřený standard 1. července 2008 a byl publikován Mezinárodní organizací pro standardizaci jako **ISO 32000-1:2008**.

**2008** – Společnost Adobe zveřejnila veřejnou patentovou licenci na formát ISO 32000-1 bez licenčních poplatků pro všechny patenty vlastněné společností Adobe, které jsou nezbytné k vytvoření, použití, prodeji a distribuci implementací vyhovujících formátu PDF.

První verze PDF označená jako PDF 1.0, která později prošla revizemi až do PDF 1.7. PDF 1.7, které se stalo ISO 32000-1, zahrnuje některé nestandardizované proprietární technologie, stejně jako Adobe XML Forms Architecture (XFA) a rozšíření JavaScriptu pro Acrobat. Bylo to 28. července 2017, kdy byl publikován PDF 2.0, známý jako ISO 32000-2:2017, který neobsahuje žádné nestandardizované technologie.

## Specifikace formátu souboru PDF

Soubor PDF je sada bajtů, které lze seskupit do tokenů podle pravidel syntaxe definovaných specifikacemi PDF. Jednou nebo více tokenů je zkombinováno za účelem vytvoření syntaktických entit vyšší úrovně, především objektů, což jsou základní datové hodnoty, ze kterých je sestaven dokument PDF.

### Struktura souborů souborů PDF

Obsah souboru PDF je uvnitř souboru uspořádán v následujícím pořadí.

|Záhlaví
|Tělo
|Křížová referenční tabulka
| Trailer

#### Záhlaví souboru PDF ####

Bez ohledu na verzi PDF začíná soubor PDF záhlavím obsahujícím jedinečný identifikátor pro PDF a verzi formátu, jako je %PDF-1.x, kde x je v rozsahu 1-7.

#### Tělo souboru ####

Tělo souboru PDF se skládá ze sekvence nepřímých objektů představujících obsah dokumentu. Objekty, jak je popsáno výše, představují součásti dokumentu, jako jsou fonty, stránky a ukázkové obrázky. Počínaje PDF 1.5 může tělo obsahovat také proudy objektů, z nichž každý obsahuje sekvenci nepřímých objektů.

#### Tabulka křížových odkazů ####

Tabulka křížových odkazů obsahuje informace, které povolují náhodný přístup k nepřímým objektům v souboru, takže není třeba číst celý soubor, aby bylo možné najít jakýkoli konkrétní objekt. Tabulka musí obsahovat jednořádkový záznam pro každý nepřímý objekt, uvádějící bajtový offset tohoto objektu v těle souboru. (Počínaje PDF 1.5 mohou být některé nebo všechny informace o křížových odkazech alternativně obsaženy v proudech křížových odkazů.

#### Souborová upoutávka ####

Upoutávka souboru PDF umožňuje odpovídajícímu čtenáři rychle najít tabulku křížových odkazů a určité speciální objekty. Vyhovující čtenáři by měli číst soubor PDF od jeho konce. Poslední řádek souboru bude obsahovat pouze značku konce souboru, %%EOF. Dva předchozí řádky musí obsahovat, jeden na řádek a v daném pořadí, klíčové slovo startxref a bajtový offset v dekódovaném proudu od začátku souboru po začátek klíčového slova xref v poslední sekci křížového odkazu.

### Objekty PDF ###

Soubor PDF obsahuje několik různých typů objektů, které jsou následujících typů

* Booleovské hodnoty – představují podmíněnou hodnotu true nebo false
* Čísla - Integer a Real hodnoty
* Řetězce - obsahuje znaky v závorkách
* Jména – začněte znakem vpřed /, např. /ASomewhatLongerName má za následek ASomewhatLongerName
* Pole – PDF podporuje jednorozměrná pole. Pole vyšších rozměrů lze konstruovat pomocí polí jako vnořených prvků
* Slovníky - kolekce objektů jako párů klíč-hodnota. Může mít nulové položky.
* Proudy - představuje posloupnost bajtů, která může mít také neomezenou délku
* Objekt Null - představuje hodnotu null

Mohou existovat další další objekty, jako jsou komentáře, které jsou uvozeny znakem % a mohou obsahovat 8bitové znaky.

### Nepřímé objekty ###

Jakýkoli objekt v souboru PDF může být označen jako nepřímý objekt. Nepřímým objektům je přidělen jedinečný identifikátor objektu, pomocí kterého se na něj mohou ostatní objekty odkazovat. Křížové odkazy na ně jsou udržovány v indexové tabulce a označeny klíčovým slovem xref, které následuje za hlavním tělem a udává bajtový offset každého nepřímého objektu od začátku souboru.

### Lineární a nelineární rozvržení PDF ###

Rozvržení PDF jsou kategorizována jako Llnear a nelineární v závislosti na cílových aplikacích a dalších faktorech.

Nelineární – Nelineární soubory PDF využívají méně místa na disku ve srovnání s lineárními soubory PDF. Stránky PDF dokumentu jsou v souboru PDF rozptýleny, a proto jsou nelineární soubory ve srovnání s lineárními soubory pomalejší.

Lineární PDF – Cílení na online prohlížeče PDF, lineární PDF soubory jsou konstruovány tak, že jsou zapisovány na disk lineárním způsobem. To nevyžaduje pluginy prohlížeče, aby se celý dokument před zobrazením načetl jako první.

### Přehled objektů ###

Jak již bylo zmíněno, tělo PDF je kolekce objektů zmíněných výše. PDF je z velké části založen na PostScriptu bez ovládacích funkcí programovacích jazyků, jako jsou příkazy if a loop. Příkazy vydané Postscriptovým kódem pro generování grafického obsahu jsou shromažďovány a tokenizovány navíc k jakýmkoli souborům, grafikám nebo fontům uvedeným v dokumentu. Veškerý tento obsah je shromážděn do jednoho souboru, což má za následek složený výstup PostScript.

#### Text ####

Text v PDF je reprezentován textovými prvky, které jsou ve skutečnosti zobrazeny s glyfy z písem. Glyf je grafický tvar a podléhá všem grafickým úpravám, jako je transformace souřadnic. Vzhledem k důležitosti textu ve většině popisů stránek poskytuje PDF funkce vyšší úrovně pro pohodlný a efektivní popis, výběr a vykreslení glyfů.

#### Grafika ####

Grafické operátory používané v tocích obsahu PDF popisují vzhled stránek, které mají být reprodukovány na rastrovém výstupním zařízení. Zařízení jsou určena pro tiskařské i zobrazovací aplikace. Grafičtí operátoři tvoří šest hlavních skupin:

* Operátoři grafického stavu manipulují s datovou strukturou zvanou grafický stav, což je globální rámec, ve kterém provádějí ostatní grafické operátory. Grafický stav zahrnuje aktuální transformační matici (CTM), která mapuje souřadnice uživatelského prostoru používané v toku obsahu PDF na souřadnice výstupního zařízení. Zahrnuje také aktuální barvu, aktuální ořezovou cestu a mnoho dalších parametrů, které jsou implicitními operandy operátorů malování.
* Operátoři konstrukce cest určují cesty, které definují tvary, trajektorie čar a oblasti různých druhů. Zahrnují operátory pro začátek nové cesty, přidání segmentů čáry a křivek k ní a její uzavření.
* Operátoři malování cest vyplní cestu barvou, namalují podél ní tah nebo ji použijí jako ořezovou hranici.
* Ostatní operátoři malování malují určité samopopisující grafické objekty. Patří mezi ně vzorkované obrázky, geometricky definované stínování a celé toky obsahu, které zase obsahují sekvence grafických operátorů.
* Textové operátory vybírají a zobrazují znakové glyfy z písem (popisy typů písma pro reprezentaci textových znaků). Protože PDF zachází s glyfy jako s obecnými grafickými tvary, mnoho textových operátorů lze seskupit s operátory stavu grafiky nebo malování. Datové struktury a mechanismy pro práci s popisy glyfů a písem jsou však dostatečně specializované.
* Operátoři označeného obsahu spojují logické informace vyšší úrovně s objekty v toku obsahu. Tyto informace neovlivňují vykreslený vzhled obsahu; je to užitečné pro aplikace, které používají PDF pro výměnu dokumentů.

## Reference ##

* [Formát souboru PDF: Základní struktura](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF – Wikipedie](https://en.wikipedia.org/wiki/PDF)
* [PDF Reference – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

