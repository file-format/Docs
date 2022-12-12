{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "soubor", "přípona", "formát", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů JT a rozhraních API, která mohou vytvářet a otevírat soubory JT.",
  "title" :"JT - formát souboru Jupiter Tessellation",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor JT?

**JT** (Jupiter Tessellation) je účinný, průmyslově zaměřený a flexibilní formát 3D dat standardizovaný ISO vyvinutý společností Siemens PLM Software. Domény mechanického CAD v letectví, automobilovém průmyslu a těžkém vybavení používají JT jako svůj nejvýznamnější formát 3D vizualizace.

Formát JT je graf scény, který podporuje atributy a uzly, které jsou specifické pro CAD. K ukládání fazetových dat (trojúhelníků) se používají sofistikované kompresní techniky. Tento formát je strukturován tak, aby podporoval vizuální atributy, produktové a výrobní informace (PMI) a metadata. Existuje dobrá podpora pro asynchronní streamování obsahu. V těžkém strojírenství používají profesionálové soubor JT ve svých CAD řešeních a softwarových programech pro správu životního cyklu produktu (PLM) ke zkoumání geometrie komplikovaného zboží.

Protože JT podporuje téměř všechny důležité 3D CAD formáty, jeho sestava se může vypořádat s různými kombinacemi, které jsou známé jako "multi-CAD". Tato multi-CAD sestava je vždy dobře spravována a aktualizována, protože synchronizace mezi nativními soubory popisu produktu CAD s jejich přidruženými soubory JT probíhá automaticky. Soubory JT jsou původně lehké, takže se považují za vhodné pro internetovou spolupráci. Společnosti spolupracují prostřednictvím odesílání 3D vizualizací přes média mnohem snadněji ve srovnání s „těžkými“ původními soubory CAD. Soubory JT navíc zajišťují mnoho funkcí zabezpečení, díky nimž je sdílení duševního vlastnictví bezpečnější.

## Stručná historie formátu souborů JT

Engineering Animation, Inc. a Hewlett Packard byli původními návrháři JT, kteří tento formát vyvinuli jako sadu nástrojů Direct Model. Po akvizici EAI společností UGS Corp. se JT stal součástí sady UGS. Počátkem roku 2007 společnost UGS oznámila JT jako svůj hlavní 3D formát. Ve stejném roce Siemens AG koupil UGS a stal se Siemens PLM Software. Siemens používá JT jako společný formát interoperability a formát pro archivaci dat. V roce 2009 přijala ISO specifikaci JT k publikaci jako veřejně dostupnou specifikaci ISO (PAS). V polovině roku 2010 společnost ProSTEP iViP oznámila, že na průmyslové úrovni lze JT a STEP AP 242 XML používat společně k dosažení maximálních výhod v datech. výměnné scénáře. V roce 2012 byl JT oficiálně deklarován jako ISO standardizovaný (ISO 14306:2012 (ISO JT V1)) 3D vizualizační formát.

## Formát souboru JT ##

Všechny objekty ve formátu JT jsou reprezentovány prostřednictvím identifikátoru objektu a odkazy mezi objekty jsou zpracovávány pomocí identifikátoru odkazovaného objektu. Integrita těchto referencí na objekty může být udržována pomocí roztažení/swizzling ukazatelů.

Soubor JT je uspořádán jako řada bloků a blok záhlaví je vždy prvním blokem dat v souboru. Po bloku záhlaví bezprostředně následuje řada datových segmentů a segment TOC. Jeden datový segment (6 LSG Segment) má referenční soubor JT, který vždy existuje. Segment TOC obsahuje informace o umístění všech ostatních datových segmentů daného souboru.

{{< figure src="../JT-1.png" alt="Formát souboru JT" >}}

### Záhlaví souboru ###

Záhlaví souboru je prvním blokem v datové hierarchii souboru JT. Informace o verzi a informace o umístění obsahu jsou uzavřeny v záhlaví, což usnadňuje zavaděčům čtení souborů. Obsah záhlaví souboru je uspořádán následovně.

### Segment TOC ###

Segment TOC musí existovat v souboru a obsahovat informace o identifikaci a umístění všech ostatních datových segmentů. Skutečné umístění segmentu TOC je určeno polem TOC Offset v záhlaví souboru. Každý jednotlivě adresovatelný datový segment je reprezentován záznamem TOC v segmentu TOC.

### Datový segment ###

Soubor JT definuje všechna uložená data v rámci datového segmentu. Některé datové segmenty mohou komprimovat všechny datové bajty informací, které zůstaly v segmentu. Datové segmenty mají následující strukturu:

![alt text](../JT-2.png "JT Data Segment")

Následující tabulka popisuje různé typy segmentů dat:

|Jméno|Popis
---|---|
|LSG segment|Zahrnuje kolekci objektů propojených prostřednictvím směrovaných odkazů do formy LSG (struktura směrovaného acyklického grafu)
|Segment LOD tvaru|obsahuje definující data pro geometrické tvary (např. vrcholy, normály, mnohoúhelníky atd.)
|JT B-Rep Segment|Má prvek pro data reprezentující přesnou geometrickou hranici pro jednotlivou část ve formátu JT B-Rep.
|XT B-Rep segment|Obsahující prvek pro data, která reprezentují přesnou geometrickou hranici pro jednotlivou část ve formátu reprezentace hranice
|Segment drátěného modelu|Data představují přesný 3D drátový model pro konkrétní část, který je definován prvkem obsaženým v tomto segmentu.
|Segment metadat|Umožňuje ukládat metadata v různých adresovatelných segmentech.
|JT ULP segment|Obsahující prvek pro data reprezentující polopřesnou geometrickou hranici pro jednotlivou část ve formátu JT ULP.
|JT LWPA segment|Obsahuje element definující analytická data pro konkrétní součást. LWPA uzavře kolekci analytických povrchů do definice b-rep součásti.

## Komprese ##

Požadavky na přenos a ukládání 3D modelů jsou náročnější, takže soubory JT mohou využít komprimace. Datový model JT může být složen z různých souborů pomocí různých kompresních technik, ale proces komprese je pro uživatele dat JT transparentní.

JT Open Toolkit (jako standard) a pokročilá komprese jsou zatím dvě kompresní techniky používané soubory JT. JT Open Toolkit využívá snadný, bezeztrátový kompresní algoritmus, zatímco pokročilá komprese využívá jemnější, doménově specifickou kompresní techniku, která vede ke ztrátové geometrické kompresi. Klientské aplikace preferují pokročilou kompresi spíše než standardní kompresi, protože pokročilá komprese poskytuje poměrně vysoké kompresní poměry. Zpětná kompatibilita s běžnými aplikacemi pro prohlížení souborů JT je zachována prostřednictvím standardní komprese. Kompresní formulář musí být kompatibilní s verzí formátu souboru JT, kterou lze vidět, když se soubor JT otevře pomocí textového editoru, a musí být uzavřen v informacích záhlaví ASCII.

## Reference ##

* [Referenční informace o formátu souboru JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (formát vizualizace)](https://en.wikipedia.org/wiki/JT_(formát_vizualizace)#Data_model)

