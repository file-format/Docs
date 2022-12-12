{
  "date" : "2019-10-11",
  "keywords" :[ "soubor emf", "formát souboru emf", "co je soubor emf", "soubor", "příklad emf", "přípona souboru emf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Enhanced Metafile Format",
  "description":"Další informace o formátu souborů EMF a rozhraních API, která mohou vytvářet a otevírat soubory EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor EMF?

**Enhanced metafile format (EMF)** ukládá grafické obrázky nezávisle na zařízení. Metasoubory EMF se skládají ze záznamů s proměnnou délkou v chronologickém pořadí, které mohou vykreslit uložený obraz po analýze na libovolném výstupním zařízení. Tyto záznamy s proměnnou délkou mohou být definice uzavřených objektů, příkazy pro kreslení a grafické vlastnosti, které jsou důležité pro přesné vykreslení obrazu. Když zařízení otevře metasoubor EMF pomocí vlastního grafického prostředí, proporce, rozměry, barvy a další grafické vlastnosti původního obrázku zůstanou stejné bez ohledu na platformu otevíracího zařízení.

## Stručná historie ##

V roce 1990 Microsoft navrhl obrazový formát souboru Windows Metafile ([WMF](/cs/image/wmf/)) pro Microsoft Windows. Metasoubory Windows jsou 16bitový formát, který může obsahovat některé bitmapové komponenty. WMF se může skládat z vektorové grafiky a je určen k tomu, aby byl přenosný mezi různými aplikacemi. V roce 1993 Win32/GDI ohlásil Enhanced Metafile (EMF), novější verzi se zvýšenou flexibilitou a škálovatelností. EMF se také používá jako příkazy grafického jazyka pro spouštění ovladačů tiskárny. Společnost Microsoft nyní doporučuje rozšířený formát metasouboru (EMF) oproti formátu Windows (WMF). Když byl představen Windows XP, byla vydána verze Enhanced Metafile Format Plus (EMF+). Tato novější verze si najde cestu serializací volání GDI+ API, stejně jako volání WMF/EMF do GDI. Existuje gzip komprimovaná verze EMF známá jako EMZ.

## Formát metasouboru EMF ##

Níže jsou uvedeny základní prvky vylepšeného formátu metasouboru:

* EMR_HEADER (verze, velikost, rozlišení obrázku při vytvoření)
* Tabulka pro objekty GDI
* Rezervovaná paleta (volitelné)
* Záznamy metasouborů uspořádané do struktury pole (nastavení vlastností, definované objekty, kreslicí příkazy)
* Záznam EMR_EOF (poslední záznam v metasouboru EMF)

## Verze EMF ##
* **Originál**: Původní verze specifikuje záznam nezbytný k zachování původního obrazu a zachování jeho nezávislosti na zařízení. Navíc podporuje záznam obsahující grafické objekty a příkazy pro kreslení.
* **Verze 1**: Druhá verze EMF zlepšila flexibilitu a nezávislost na zařízení přidáním záznamu pro formát pixelů a zřízení pro použití příkazu OpenGL.
* **Verze 2**: Třetí verze zvýšila přesnost přidáním metrického systému pro měření povrchových vzdáleností zařízení, takže záznam je škálovatelnější.

## Enhanced Metafile Records ##

Záznamy metasouborů jsou uspořádány ve formě pole. Tyto záznamy mají strukturu ENHMETARECORD a variabilní délku. ENHMETARECORD specifikuje data, která definují funkce GDI pro vytvoření obrázku pomocí rozšířeného formátu metasouboru. Struktura **ENHMETAHEADER** je vždy prvním záznamem v tomto formátu. Tato hlavička EMF obsahuje následující informace.

Každý záznam rozšířeného metasouboru má na začátku dva členy EMR (poskytuje základní strukturu). První člen rozpoznává funkci GDI (parametry se používají v záznamu), která určuje typ záznamu a je známá jako iType. Druhý člen nSize definuje velikost každého záznamu. Zbývající parametry (pokud existují) a další údaje uspořádané bezprostředně pod nSize. Bezprostředně za záhlavím může být volitelný textový popis. V tomto textovém popisu je zaznamenáno jméno fotografie a autor. Paleta, jejíž přítomnost je volitelná, určuje barvy použité při vytváření rozšířeného metasouboru. Další záznamy slouží k určení funkce GDI, která je nezbytná při vytváření obrázků.

V každém metasouboru by měl být přítomen alespoň jeden záznam EMF. Informace o procházení z jednoho záznamu do druhého závisí na záznamech EMF, takže tyto záznamy musí být uspořádány vedle sebe. U jakéhokoli daného záznamu v metasouboru kromě EOF_record definuje délka tohoto konkrétního záznamu pro přesun na další záznam.

## Vylepšené vytváření metasouborů ##

Funkce **CreateEnhMetaFile** se používá k vytvoření vylepšeného metasouboru. Argumenty této funkce se používají k rozměrům a ukládání obrázku na disk/paměť. Dále tato funkce vyžaduje rozměr zařízení, na kterém se obrázek objevil jako první (referenční zařízení) a kontext referenčního zařízení (DC). Takže argumenty pro zpracování tohoto DC musí poskytnout při volání funkce **CreateEnhMetaFile**. Syntaxe funkce je následující:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** rukojeť k referenčnímu zařízení.

**lptoFilename:** Ukazatel na název souboru.

**lprc:** Ukazatel na oválnou strukturu určuje rozměry obrázku v mm.

**lpDesc:** ukazatel na řetězec pro název obrázku a název aplikace, která obrázek vytvořila.

## Vylepšené operace s metasoubory ##

Následují úlohy, které lze provést pomocí popisovače vylepšeného metasouboru.

* Zobrazení a úprava uloženého obrázku.
* Vytvářejte vylepšené kopie metasouborů.
* Získejte kopii hlavičky EMF, volitelný popis a binární verzi vylepšeného metasouboru
* Shrnutí barev v paletě.

## Grafické objekty ##

V operacích kreslení a malování lze grafické objekty vytvářet záznamy o vytváření objektů a lze je uložit pro další použití. Záznam `EMR_SELECTOBJECT` může tyto grafické objekty načíst pomocí kontextu přehrávacího zařízení. Pera, palety, štětce, barevné prostory, písma a základní objekty jsou některé opakovaně použitelné typy objektů.

## Byte řazení ##

Formát Little-endian se používá k ukládání dat v záznamech metasouborů.

## Verze ##

Formát souboru EMF byl dvakrát revidován. Změněné verze jsou původní, rozšíření 1 a rozšíření 2. Rozšířené verze mají ustanovení pro záznamy OpenGL a volitelný deskriptor pro interní formát pixelů. Pro zobrazené rozměry je přidána možnost měření v mililitrech.

## Reference ##

* [Enhanced-Format Metafiles | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Vylepšený formát a specifikace metasouborů](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

