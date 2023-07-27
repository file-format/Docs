{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Specifikace papíru XML", "Soubor", "Rozšíření", "Formát souboru", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Formát souboru rozvržení stránky",
  "description":"Další informace o formátu souboru XPS a rozhraních API, která mohou vytvářet a otevírat soubory XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor XPS? ##

Soubor XPS představuje soubory rozvržení stránky, které jsou založeny na specifikacích papíru XML vytvořených společností Microsoft. Byl vyvinut jako náhrada formátu souboru EMF a je podobný formátu souboru [PDF](/cs/pdf/), ale používá XML v rozložení, vzhledu a informacích o tisku dokumentu. Ve skutečnosti je oprávněnější říci, že XPS je pokus o PDF, ale z mnoha důvodů nemohl získat dostatečnou popularitu, jakou vlastní PDF. Společnost Microsoft poskytuje ve výchozím nastavení XPS Document Writer od systému Windows 7 pro vytváření souborů XPS. Soubory XPS lze generovat výběrem "Microsoft XPS Document Writer" jako tiskárny při tisku dokumentu.

Prohlížeče XPS jsou integrovány jako součást Windows Vista, Windows 7, Windows 8 a Internet Explorer 6 nebo novější. Soubory XPS se po vygenerování stanou pouze pro čtení. To zvyšuje důvěru uživatele v přijaté dokumenty odeslané jako XPS pro pravost dokumentu. Dokument XPS může obsahovat jednu nebo více stránek převedených z původního dokumentu.

## Stručná historie ##

Microsoft předložil specifikaci XPS společnosti Ecma International. V červnu 2007 byl zřízen technický výbor Ecma 46 (TC46), jehož úkolem bylo vytvořit standard založený na specifikacích papíru OpenXPS. Společnost Ecma International schválila standard Ecma (ECMA-388) [Specifikace XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) v červnu 2009 na 97. valném shromáždění.

## Formát souboru XPS ##

Formát XPS se skládá ze značek XML, které definují složení dokumentu a vizuální vzhled každé stránky spolu s pravidly vykreslování pro zobrazení nebo tisk dokumentu. Uchovává všechny informace, aby bylo možné znovu vytvořit dokument v jakémkoli systému, což jej činí nezávislým na zdrojích dostupných v tomto systému. Formát je v podstatě archiv ZIP a pokud příponu souboru přejmenujete na ZIP, uvidíte základní soubory, které obsahují data dokumentu. Mezi tyto dokumenty patří:

* Soubory stránek dokumentu (.fpage) – Obsahuje obsah dokumentu a nastavení formátu dokumentu. Každá stránka v dokumentu XPS má jeden soubor FPAGE.
* soubor nastavení dokumentu (.fdoc) - Ukládá nastavení obsažená v archivu XPS.
* soubory fragmentů dokumentu (.frag) – Definuje nastavení pro aktuální soubor XPS a každá stránka v dokumentu má svůj vlastní soubor .frag.

{{< figure src="../XPS-1.png" alt="Formát souboru XPS" >}}

Tyto soubory uchovávají obsah dokumentu takovým způsobem, že pokud například někdo nemá na svém počítači nainstalována stejná písma, prohlížeč XPS tato původní písma přesto vykreslí. To znamená zahrnutí souboru značek XML pro každý:

* Stránka
* Text
* Vložená písma
* Rastrové obrázky
* 2D vektorová grafika
* Správa digitálních práv

Formát dokumentu XPS obsahuje dobře definovanou sadu částí a vztahů, z nichž každá plní v dokumentu určitý účel. Formát také rozšiřuje funkce balíčku, včetně digitálních podpisů, miniatur a prokládání.

Typický dokument XPS vypadá následovně a lze jej analyzovat ve světle formátu souboru XPS [specifikace](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Formát souboru XPS" >}}


## Reference ##

* [Specifikace formátu souboru XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS – z Wikipedie](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

