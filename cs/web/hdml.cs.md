{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor značkovacího jazyka ručního zařízení",
  "description":"Další informace o formátu souborů HDML a rozhraních API, která mohou vytvářet a otevírat soubory HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Co je soubor HDML?

Soubor s příponou .hdml (Handheld Device Markup Language) je značkovací jazyk pro vytváření webových stránek pro přenosná elektronická zařízení, jako jsou kapesní počítače, chytré telefony a zařízení pro zobrazování informací. HDML je prý rozšířením jazyka [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML je podobný HTML, ale pro bezdrátová a kapesní zařízení, která mají malé displeje, jako jsou PDA, mobilní telefony a tak dále. To bylo nahrazeno WML, pro které se choval jako důležitý vliv.

## Formát souboru HDML – Další informace

HDML je značkovací jazyk pro kapesní zařízení, který je založen na značkovacích značkách podobných HTML. HDML byl předložen W3C ke standardizaci, ale nikdy se nestal standardem. Jeho specifikace formátu souboru jsou však k dispozici na [webové stránce W3] (https://www.w3.org/TR/NOTE-Submission-HDML-spec.html). [Syntaxe jazyka HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) je k dispozici pro vývojáře a lze ji použít pro vývoj ukázkových aplikací.

## prvky HDML

Následuje seznam prvků, které poskytují run-time prostředí pro HDML a jsou označovány jako uživatelský agent.

|Prvek|Popis|
---|---|
|Karty|Toto je základní stavební blok HDML a zobrazuje a umožňuje uživateli pracovat s kartami informací. |
|Balíčky|HDML karty jsou seskupeny do balíčků. Balíček HDML je podobný HTML stránce v tom, že je identifikován URL [RFC1738] a je to jednotka obsahu požadovaná ze serveru a uložená do mezipaměti uživatelským agentem.|
|Akce|Akce mohou být typu PREV, SOFT1-SOFT8 a HELP. Ty jsou abstraktní a jsou podporovány v uživatelském rozhraní způsobem specifickým pro uživatelského agenta.|
|Aktivity|Činnost je jako skupina souvisejících karet, které plní jednu logickou funkci. Ty mohou zahrnovat jednu nebo více palub. Navigační a stavový model HDML je strukturován podle činností.|
|Navigace založená na historii|User agent udržuje historii karet zobrazených uživateli. Každá karta, ke které se přistupuje, je přidána do historie karet. Uživatelský agent umožňuje uživateli snadno přejít zpět na předchozí kartu v historii.|

## Reference

* [HDML – Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Specifikace HDML – školy W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

