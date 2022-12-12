{
  "date" : "2019-10-11",
  "keywords" :[ "soubor tiff", "formát souboru tiff", "co je soubor tiff", "soubor", "příklad tiff", "přípona souboru tiff", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Formát souboru obrázku",
  "description":"Další informace o formátu souboru TIFF a rozhraních API, která mohou vytvářet a otevírat soubory TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TIFF?

TIFF nebo TIF, Tagged Image File Format, představuje rastrové obrázky, které jsou určeny pro použití na různých zařízeních, která vyhovují tomuto standardu formátu souboru. Je schopen popsat dvouúrovňová, šedá, paletová a plnobarevná obrazová data v několika barevných prostorech. Podporuje ztrátová i bezeztrátová kompresní schémata pro výběr mezi prostorem a časem pro aplikace používající formát. Formát není závislý na počítači a je prostý omezení, jako je procesor, operační systém nebo systémy souborů.

## Stručná historie formátu souboru TIFF

Formát souboru TIFF byl původně vytvořen společností Aldus Corporation na podzim roku 1986, po sérii setkání s různými výrobci skenerů a vývojáři softwaru. Primárním účelem formátu souboru TIFF bylo poskytnout běžný formát souboru naskenovaného obrázku pro všechny dodavatele stolních skenerů. Počínaje podporou pouze binárního formátu obrázků se formát postupem času vyvinul k podpoře obrázků ve stupních šedi a barevných obrázků. Počáteční verze specifikací formátu souboru TIFF může být označena jako Reivision 3.0, protože existovaly dvě dřívější verze. V roce 1988 byla publikována hlavní revize 5.0, která přidala podporu pro paletové barevné obrázky a kompresi LZW. Revize 6.0 formátů souborů TIFF byla publikována v roce 1992 poté. V roce 1994 společnost Adobe Systems získala Aldus a specifikace jsou nyní k dispozici a spravuje je společnost Adobe Systems.

## Specifikace formátu souboru TIFF

Formát souboru TIFF je rozšiřitelný a prošel několika revizemi, které umožňují zahrnutí neomezeného množství soukromých nebo speciálních informací. Soubor TIFF začíná 8bajtovým záhlavím, kde bajty jsou čísla od 0 do N. Největší možný soubor TIFF má délku 2**32 bajtů. Soubor začíná 8bajtovým záhlavím souboru obrázku, který ukazuje přímo na soubor obrázku (IFD). IFD obsahuje informace o obrázku a také ukazatele na aktuální data obrázku.

### Záhlaví souboru TIFF

Záhlaví 8bajtového souboru TIFF obsahuje následující informace:

**Bytes 0-1:** Pořadí bajtů použité v souboru. Zákonné hodnoty jsou: „II“ (4949.H) „MM“ (4D4D.H).

Ve formátu „II“ je pořadí bajtů vždy od nejméně významného bajtu po nejvýznamnější bajt, pro 16bitová i 32bitová celá čísla. Toto se nazývá pořadí bajtů typu little-endian. Ve formátu „MM“ je pořadí bajtů vždy od nejvýznamnějšího po nejméně významný, pro 16bitová i 32bitová celá čísla. Toto se nazývá pořadí bajtů big-endian.

**Bajty 2–3:** Libovolné, ale pečlivě zvolené číslo (42), které dále identifikuje soubor jako soubor TIFF. Pořadí bajtů závisí na hodnotě bajtů 0–1.

**Bytes 4-7:** Posun (v bajtech) prvního IFD. Adresář může být na libovolném místě v souboru za záhlavím, ale musí začínat na hranici slova. Adresář obrazových souborů může zejména sledovat obrazová data, která popisuje. Čtenáři se musí řídit ukazateli, kam mohou vést. Termín bajtový offset se v tomto dokumentu vždy používá k označení umístění vzhledem k začátku souboru TIFF. První bajt souboru má offset 0.

### Adresář souborů s obrázky

IFD obsahuje informace o obrázku a také ukazatele na aktuální data obrázku. Skládá se z 2bajtového počtu položek v adresáři (tj. počtu polí), po kterém následuje sekvence 12bajtových položek v polích. , následovaný 4bajtovým offsetem dalšího IFD (nebo 0, pokud žádný). V souboru TIFF musí být alespoň 1 IFD a každý IFD musí mít alespoň jednu položku.

#### Vstup IFD

Každý 12bajtový záznam IFD je v následujícím formátu.


|Bajty|Popis
---|---|
|0-1|Značka, která identifikuje pole
|2-3|Typ pole
|4-7|Počet uvedeného typu
|8-11|Posun hodnoty, posun souboru (v bajtech) hodnoty pro pole. Očekává se, že hodnota bude začínat na hranici slova; odpovídající Posun hodnoty bude tedy sudé číslo. Tento offset souboru může ukazovat kdekoli v souboru, dokonce i za obrazovými daty

Pole TIFF je logická entita sestávající z tagu TIFF a jeho hodnoty. Tento logický koncept je implementován jako položka IFD plus skutečná hodnota, pokud se nevejde do části hodnota/posun, posledních 4 bajtů položky IFD. Pojmy pole TIFF a položka IFD jsou ve většině kontextů zaměnitelné.

### Základní TIFF ###

Baseline TIFF je jádrem TIFF, základů, které by měli všichni běžní vývojáři TIFF podporovat ve svých produktech. Shoda s formátem TIFF je podmíněna dodržováním požadavků Baseline TIFF. Tyto požadavky jsou dobře zdokumentovány v dokumentu specifikací 6.0.

#### Více obrázků na soubor ####

V souboru TIFF může být více než jedno IFD. Každý IFD definuje dílčí soubor. Jedním z potenciálních použití podsouborů je popis souvisejících obrázků, jako jsou stránky faxového přenosu. Čtečka Baseline TIFF nemusí číst žádné IFD kromě prvního.

#### Typy obrázků ####

Základní obrázek TIFF má následující typy:

**Dvouúrovňový:** Dvouúrovňový obrázek obsahuje dvě barvy – černou a bílou. TIFF umožňuje aplikaci zapisovat dvouúrovňová data ve formátu bílá je nula nebo černá je nula. Pole, které zaznamenává tyto informace, se nazývá **PhotometricInterpretation**.

* RGB plnobarevné

Informace o PhotometricInterpretation pro dvouúrovňové obrázky jsou následující:

Značka = 262 (106,H)
Typ = KRÁTKÁ
**Hodnoty**

|Hodnota|Popis|
---|---|
|0|Pro dvouúrovňové obrázky a obrázky ve stupních šedi: 0 je zobrazena jako bílá. Maximální hodnota je zobrazena jako černá. Toto je normální hodnota pro Compression#2|
|1|Černá je nula. Pro dvouúrovňové obrázky a obrázky ve stupních šedi: 0 je zobrazena jako černá. Maximální hodnota je zobrazena jako bílá. Pokud je tato hodnota zadána pro Compression#2, obraz by se měl zobrazit a vytisknout obráceně.|

**Stupně šedi:** Obrázky ve stupních šedi jsou zobecněním dvouúrovňových obrázků. Dvouúrovňové obrazy mohou ukládat pouze černobílá obrazová data, ale obrazy ve stupních šedi mohou také ukládat odstíny šedé. Chcete-li takové obrázky popsat, musíte přidat nebo změnit následující pole. Ostatní povinná pole jsou stejná jako u dvouúrovňových obrázků. Pro obrázky ve stupních šedi komprese # 1 nebo 32773 (PackBits). V Baseline TIFF mohou být obrázky ve stupních šedi uloženy buď jako nekomprimovaná data, nebo komprimované pomocí algoritmu PackBits.

Informace **BitsPerSample** pro obrázky ve stupních šedi jsou následující:

Značka = 258 (102,H)
Typ = KRÁTKÁ

Počet bitů na komponentu. Povolené hodnoty pro obrázky ve stupních šedi Baseline TIFF jsou 4 a 8, což umožňuje 16 nebo 256 různých odstínů šedi.

**Palette-Color:** Obrázky v paletě barev jsou podobné obrázkům ve stupních šedi. Stále mají jednu komponentu na pixel, ale hodnota komponenty se používá jako index do úplné vyhledávací tabulky RGB. Chcete-li takové obrázky popsat, musíte přidat nebo změnit následující pole. Ostatní povinná pole jsou stejná jako u obrázků ve stupních šedi.
Informace o fotometrické interpretaci pro obraz Palette-Color jsou následující:

Fotometrická interpretace = 3 (barva palety).
ColorMapTag = 320 (140,H)
Typ = KRÁTKÁ
N = 3 * (2 bity na vzorek)

Toto pole definuje barevnou mapu červená-zelená-modrá (často nazývaná vyhledávací tabulka) pro obrázky palet barev. V obrazu palety barev se hodnota pixelu používá k indexování do vyhledávací tabulky RGB. Například pixel palety barev s hodnotou 0 by se zobrazil podle 0. trojice červená, zelená, modrá. V barevné mapě TIFF jsou na prvním místě všechny hodnoty červené, poté hodnoty zelené a poté hodnoty modré. V ColorMap je černá reprezentována 0,0,0 a bílá je reprezentována 65535, 65535, 65535.

**RGB plné barvy:** V obrázku RGB se každý pixel skládá ze tří složek: červené, zelené a modré. Neexistuje žádná mapa barev. Chcete-li popsat obrázek RGB, musíte přidat nebo změnit následující pole a hodnoty. Ostatní povinná pole jsou stejná jako u obrázků v paletě barev.

BitsPerSample = 8,8,8. Každá složka má hloubku 8 bitů v základním obrázku TIFF RGB.

PhotometricInterpretation = 2 (RGB) a neexistuje žádná mapa barev.

Značka = 277 (115,H)
Typ = KRÁTKÁ
Počet komponent na pixel. Toto číslo je 3 pro obrázky RGB, pokud nejsou přítomny další vzorky.

## Reference ##

* [Formát souboru TIFF – Wikipedie](https://en.wikipedia.org/wiki/TIFF)

