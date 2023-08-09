{
  "date" : "2019-12-09",
  "keywords" :[ "soubor 3mf", "formát souboru 3mf", "co je soubor 3mf", "soubor", "příklad 3mf", "přípona souboru 3mf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Další informace o formátu souboru 3MF a rozhraních API, která mohou otevírat a vytvářet soubory 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Co je soubor 3MF?

3MF, 3D Manufacturing Format, je používán aplikacemi k vykreslování 3D modelů objektů pro řadu dalších aplikací, platforem, služeb a tiskáren. Byl vytvořen tak, aby se vyhnul omezením a problémům v jiných 3D formátech souborů, jako je [STL](/cs/cad/stl/), pro práci s nejnovějšími verzemi 3D tiskáren. 3MF je relativně nový formát souborů, který byl vyvinut a publikován konsorciem 3MF. Bohatě stačí k úplnému popisu modelu, uchování interních informací, barev a dalších charakteristik, které jej činí rozšiřitelným pro podporu nových inovací v 3D tisku. Formát je rozšiřitelný, může být široce přijat a bez problémů s jinými široce používanými formáty souborů.

## Stručná historie formátu souboru 3MF

Stávající omezení v dostupných modelových popisných formátech souborů, jako je STL a další, vedou přední značky k tomu, aby se spojily a vytvořily rozšiřitelnější formát souborů pro 3D tisk. Důležitou úvahou bylo, jak by aplikace měly předávat modelová data 3D tiskárnám. Konsorcium 3MF tedy vzniklo, aby podpořilo nový formát 3D souborů nazvaný 3MF s cílem zajistit, aby byl dostatečně rozšiřitelný, aby vyhovoval potřebám 3D tisku. Součástí tohoto konsorcia bylo několik společností včetně Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP a dalších. Společnost Microsoft darovala svůj nedokončený formát 3D souborů jako výchozí bod pro další vývoj specifikace konsorcia 3MF ve spolupráci.

## Formát souboru 3MF - Další informace

3MF je datový formát založený na XML – lidsky čitelný komprimovaný XML – který obsahuje definice pro data související s 3D výrobou, včetně rozšiřitelnosti třetích stran pro vlastní data. Formát souboru 3MF byl navržen s ohledem na omezení a problémy, kterým čelí jiné formáty souborů 3D. To vedlo k formulaci formátu souboru 3MF, který je:

* **Kompletní:** Obsahuje všechny potřebné informace o modelu, materiálu a majetku v jediném archivu
* **Čitelné pro člověka:** Použití běžných struktur, jako je OPC, [ZIP](/cs/komprese/zip/) a XML pro usnadnění vývoje
* **Jednoduché:** Krátká a jasná specifikace, která usnadňuje vývoj a urychluje ověřování
* **Rozšiřitelné:** Využití jmenných prostorů XML umožňuje veřejná i soukromá rozšíření při zachování kompatibility
* **Jednoznačně:** Jasné testy jazyka a shody zajišťují, že soubor je vždy konzistentní od digitálního po fyzický
* **Zdarma:** Přístup a implementace specifikace 3MF je a vždy bude bez licenčních poplatků, patentů a licencí

Specifikace pro formát souboru 3MF jsou hostovány na [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) pro veřejný přístup a průběžné aktualizace. Aktuální publikovaná verze je 1.2.3, která popisuje sadu konvencí pro použití XML a dalších široce dostupných technologií k popisu obsahu a vzhledu jednoho nebo více 3D modelů. Vývojáři, kteří chtějí sestavit systémy pro zpracování formátů souborů 3MF, se mohou pro účely implementace odkázat na tyto specifikace.

## Specifikace formátu souboru 3MF

Formát souboru 3MF využívá pro svůj fyzický model specifikace Open Packaging ve formě archivu ZIP. Zahrnuje dobře definovanou sadu částí a vztahů, které plní konkrétní účel dokumentu. Díky tomu také formát odpovídá funkci balíčku včetně digitálních podpisů a miniatur.

### Dokument 3MF – přehled

Typický dokument 3MF vypadá následovně:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Užitečné zatížení zahrnuje úplnou sadu dílů potřebných pro zpracování dílu 3D modelu. Veškerý obsah, který má být použit k výrobě předmětu popsaného v 3D užitečné zátěži, MUSÍ být obsažen v dokumentu 3MF. Popis každé části dokumentu spolu s jejím stavem podle potřeby nebo možnosti je uveden v následující tabulce.


|**Jméno**|**Popis**|**Zdroj vztahu**|**Povinné/Volitelné**
--- | --- | --- | ---
|3D model|Obsahuje popis jednoho nebo více 3D objektů pro výrobu.|Balík|POŽADOVANÝ
|Základní vlastnosti|Část OPC, která obsahuje různé vlastnosti dokumentu.|Balík|VOLITELNÉ
|Původ digitálního podpisu|Část OPC, která je kořenem digitálních podpisů v balíčku.|Balík|VOLITELNÉ
|Digitální podpis|Části OPC, z nichž každá obsahuje digitální podpis.|Původ digitálního podpisu|VOLITELNÉ
|Certifikát digitálního podpisu|Části OPC, které obsahují certifikát digitálního podpisu.|Digitální podpis|VOLITELNÉ
|PrintTicket|Poskytuje nastavení pro použití při výstupu 3D objektu(ů) v části 3D modelu.|3D model|VOLITELNÉ
|Miniatura|Obsahuje malý obrázek JPEG nebo PNG, který představuje 3D objekty v balíčku nebo balíčku jako celku.|Balík|VOLITELNÉ
|3D textura|Obsahuje texturu použitou k aplikaci barvy na 3D objekt v části 3D modelu (k dispozici pro rozšíření)|3D model|VOLITELNÉ
|Vlastní díly|díly OPC, které jsou spojeny s metadaty|balíček|VOLITELNÉ

[Díly a vztahy](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D modely](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Materiálové zdroje](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) a [Funkce balíčku](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) části specifikací dokumentu poskytují podrobné informace o dokumentu 3MF.

## Reference ##

* [Specifikace formátu souboru 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF – z Wikipedie](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

