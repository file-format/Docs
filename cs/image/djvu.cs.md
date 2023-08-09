{
  "date" : "2019-10-11",
  "keywords" :[ "soubor djvu", "formát souboru djvu", "co je soubor djvu", "soubor", "příklad djvu", "přípona souboru djvu", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru DJVU",
  "description":"Další informace o formátu souborů DJVU a rozhraních API, která mohou vytvářet a otevírat soubory DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DJVU?

DjVu, vyslovováno jako „déjà vu“, je formát grafického souboru určený pro naskenované dokumenty a knihy, zejména ty, které obsahují kombinaci textu, kreseb, obrázků a fotografií. Byl vyvinut společností AT&T Labs. Využívá různé techniky, jako je separace obrazových vrstev textu a obrázků na pozadí, progresivní načítání, aritmetické kódování a ztrátová komprese pro bitonální obrázky. Protože soubor DJVU může obsahovat komprimované, ale vysoce kvalitní barevné obrázky, fotografie, text a kresby a lze jej uložit na méně místa, používá se na webu jako e-knihy, manuály, noviny, staré dokumenty atd.

DjVu může být hodnocena jako lepší alternativa k [PDF](/cs/pdf/). Přípony souborů přidružené k DjVu jsou .DJVU nebo .DJV. DjVu může dosáhnout kompresních poměrů asi 5–10 lepších než stávající metody, jako je [JPEG](/cs/image/jpeg/) & [GIF](/cs/image/gif/) pro barevné dokumenty a 3–8krát lepší než [TIFF]( /image/tiff/) v černobílých dokumentech. Naskenované dokumenty s rozlišením 300 DPI s plnobarevnou velikostí až 25 MB lze komprimovat na 30 až 100 KB. Podobně lze černobílé dokumenty komprimovat až na 5 až 30 kB. Průměrná velikost HTML stránky může být až 50 KB, takže tyto dokumenty lze bez problému nahrát na net.

## Stručná historie ##

Technologie DjVu byla vyvinuta v laboratořích AT&T [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner a Paul G od roku 1996 do roku 2001. Formát souboru DjVu prošel různými revizemi, z nichž poslední pochází z roku 2005.


|Verze|Datum vydání|Poznámky
---|---|---|
|1–19|1996–1999|Toto jsou vývojové verze.
|20|Duben 1999|Jedna stránka byla změněna na vícestránkový formát.
|23|Červenec 2002|Část CID
|24|únor 2003|LTAnno kus
|21|Září 1999|Formát nepřímého úložiště nahrazen. Byla přidána vrstva textového vyhledávání.
|22|Duben 2001|Orientace stránky, barva JB2
|25|Květen 2003|Díl NAVM. Byla přidána podpora pro záložky DjVu.
|26|Duben 2005|Textové/řádkové anotace

## Formát souboru DjVu ##

Dokumenty DjVu jsou soubory IFF85. Struktura poskytuje hierarchii kontejnerů, které obsahují informace v souboru DjVu. Tyto nádoby se také nazývají „Chunks“. Typ bloku a ID bloku popisují, jak se blok používá. Následuje 4bajtová hlavička následovaná strukturou IFF. První čtyři bajty souboru DjVu jsou 0x41 0x54 0x26 0x54. Tato část pojednává o různých druzích dokumentů DjVu a odpovídajících částech, ze kterých se skládají.


|ID bloku|Použití
---|---|
|FORM|Složený blok obsahující první čtyři datové bajty bloku FORM, které jsou sekundárním identifikátorem.
|FORM:DJVM|Vícestránkový dokument DjVu. Složený blok, který obsahuje blok DIRM.
|FORM:DJVU|Jednostránkový dokument DjVu. Složený kus, který obsahuje části, které tvoří stránku v dokumentu djvu.
|FORM:DJVI|„sdílený“ soubor DjVu, který je součástí části INCL. Sdílené anotace a slovník tvarů.
|FORM:THUM|Složený blok, který obsahuje bloky TH44, což jsou vložené miniatury.
|DIRM|Informace o názvu stránky pro vícestránkové dokumenty.
|NAVM|Informace o záložce
|ANTa, ANTz|Anotace včetně počátečního nastavení zobrazení a překrývajících se hypertextových odkazů, textových polí atd.
|TXTa, TXTz|Unicode Text a informace o rozvržení.
|Djbz|Tabulka sdílených tvarů.
|Sjbz|BZZ komprimovaná bitonální data JB2 použitá k uložení masky.
|FG44|IW44 data použitá k uložení popředí
|BG44|Data IW44 použitá k uložení pozadí
|TH44|data IW44 používaná k ukládání vložených miniatur
K odstranění vodoznaku jsou vyžadována data |WMRM|JB2
|FGbz|Barevná data JB2. Poskytuje barvu pro každý (blit nebo tvar?) v odpovídajícím bloku Sjbz.
|INFO|Informace o stránce a DjVu
|INCL|ID zahrnutého bloku FORM:DJVI.
|BGjp|Zakódované pozadí JPEG
|FGjp|JPEG kódované popředí
|Smmr|Kódovaná maska G4

### DJVU komprese

Jeden obrázek je rozdělen do mnoha různých obrázků a poté je každý obrázek komprimován samostatně. Pro vytvoření souboru DjVu je obrázek nejprve rozdělen na tři obrázky, pozadí, popředí a obrázek masky. Obrázky na pozadí a popředí jsou obvykle barevné obrázky s nižším rozlišením; ale obraz masky je obraz s vyšším rozlišením a obvykle je tam uložen text. Po oddělení jsou obrazy popředí a pozadí komprimovány pomocí kompresního algoritmu IW44 založeného na vlnkách, zatímco obraz masky je komprimován pomocí jiné metody zvané JB2.

Metoda kódování JB2 eliminuje velkou část redundance v textovém obrázku tím, že identifikuje identické tvary na stránce, jako je více výskytů znaku v určitém písmu. JB2 nejprve zakóduje bitmapu každého jedinečného tvaru využitím redundance mezi podobnými tvary. Poté kóduje umístění, ve kterých se jednotlivé tvary na stránce objevují. JB2 i IW44 spoléhají na nový typ adaptivního binárního aritmetického kodéru nazývaného ZP-kodér, který vytlačí veškerou zbývající redundanci v rámci několika procent Shannonova limitu. ZP-kodér je adaptivní a rychlejší než jiné přibližné binární aritmetické kodéry.

## Reference ##

* [DjVu – Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Formát souboru DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

