{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Metasoubor počítačové grafiky", "Soubor", "Rozšíření", "Formát souboru", "Vektorová grafika", "Deskriptor metasouboru"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru CGM",
  "description":"Další informace o formátu souborů CGM a rozhraních API, která mohou vytvářet a otevírat soubory CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor CGM? ##

Computer Graphics Metafile (CGM) je bezplatný, na platformě nezávislý, mezinárodní standardní formát metasouboru pro ukládání a výměnu vektorové grafiky (2D), rastrové grafiky a textu. CGM používá objektově orientovaný přístup a mnoho funkčních ustanovení pro produkci obrazu. CGM používá tyto objektově orientované charakteristiky pro přetvoření grafických prvků k vykreslení obrazu. Metasoubor obsahuje nezbytné informace, které definují další soubory. V CGM obsahuje textový zdrojový soubor všechny grafické prvky, které lze později zkompilovat do binárního souboru. CGM je v podstatě způsob, jak usnadnit výměnu 2D grafických dat, nezávisle na jakékoli konkrétní platformě nebo zařízení.

Formát CGM poskytuje různé prvky pro provádění funkcí a označující objekty pro úpravu geometrických primitiv a grafických informací. Ačkoli CGM byl nahrazen jinými formáty pro zobrazení grafiky na webových stránkách, protože není dostatečně podporován webovými stránkami, je stále velmi populární mezi průmyslovými, leteckými a jinými technickými aplikacemi. Ačkoli World Wide Web Consortium vyvinulo WebCGM, alternativní přístup pro použití CGM na webu. Primární implementace CGM byla ilustrací sekvence základních operací grafického systému jádra (GKS). V profesionálních návrzích se příliš neujal, ale do značné míry byl nahrazen jinými formáty, jako jsou DXF a SVG.

## Dějiny ##

CGM se ukázalo být mezinárodním standardem v roce 1987 (ISO 8632-1987) a byl také přijat jako národní standard ve Spojeném království společností BSI a v USA organizací ANSI. Po řadě úprav v roce 1991 byl v roce 1992 vydán revidovaný standard CGM (ISO 8632:1992). V roce 2001 World Wide Web Consortium vyvinulo WebCGM s vylepšenými možnostmi použití s webovými stránkami. V roce 2007 byla vydána druhá verze WebCGM a třetí verze byla vydána v roce 2010 s rozšířenými funkcemi.

## Formát souboru CGM ##

Metasoubory počítačové grafiky jsou v podstatě databází pro grafické informace a poskytují prostředky pro zachycení, uložení a přenos grafických dat. V důsledku toho musí existovat komponenta grafického systému pro vytváření databáze současně s prováděním aplikace ve formátu metasouboru. Ve většině případů je touto součástí generátor metasouborů. Vedle toho je potřeba další komponenta, která dokáže načítat, interpretovat a vykreslovat grafická data v metasouboru. Tato potřeba je splněna přítomností interpretu metasouborů. Následující obrázek znázorňuje pracovní prostředí grafického metasouboru.

Vztah CGM s ostatními součástmi typického grafického systému je znázorněn na obrázku výše. Z obrázku je také patrné, že funkčnost metasouboru není závislá na konečném výstupu zařízení.

Obecně existují dvě kategorie metasouborů: **zachycení sekce** a **zachycení obrázku**. Primární funkcí metasouboru pro zachycení obrázku je zachycení vícenásobných definic obrázků nezávislých na zařízení. Zatímco metasoubory zachycení relace používají systémové rozhraní k zachycení výstupního dialogu v grafickém systému. CGM patří do kategorie statických metasouborů pro zachycení obrázků. CGM poskytuje dobře organizované uspořádání komponent s dvouúrovňovou strukturou.

1. Deskriptor metasouboru
1. Soubor logicky nezávislých obrázků

Každý obrázek je sbírka deskriptorů obrázku a tělo obrázku včetně definice obrázku. deskriptor metasouboru definuje popisné informace, které se stejně vztahují na všechny obrázky daného metasouboru. Tyto informace pomáhají interpretu správně analyzovat metasoubor a rozpoznat prostředky, které jsou nutné pro správné vykreslení obrázku. Ačkoli deskriptor obrázku také obsahuje popisnou informaci, dokáže rozpoznat pouze obrázek, ve kterém se deskriptor nachází. V tomto formátu souboru je každá definice obrázku samostatná a logicky suverénní. Jsou nezávislé na všech ostatních definicích obrázků v souboru. Ihned po interpretaci metadeskriptoru lze obrázky přistupovat a interpretovat je náhodně. Změna stavu předchozích obrázků nemá žádný vliv na jejich nástupce. Tato nezávislost na obrázku je dalším významným rysem CGM. CGM se skládá z prostoru souřadnic, což jsou 2D kartézské souřadnice nazývané souřadnice virtuálních zařízení a lze je reprezentovat pomocí čísla nebo přesnosti představující rozsah a granularitu. CGM specifikuje jak přímý výběr barev, tak výběr na základě indexu. V prvním případě se specifikátor barev skládá z trojice RGB, zatímco později specifikátor barev označuje index do tabulky barev.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
