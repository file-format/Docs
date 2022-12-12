{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM File - Handheld Device Markup Language File",
  "description":"Další informace o formátu souborů HDM a rozhraních API, která mohou vytvářet a otevírat soubory HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Co je soubor HDM?

Soubor HDM je soubor webové stránky v jazyce značkování, který je vytvořen v jazyce HDML (handheld Device Markup Language). Obsahuje značkovací značky podobné jazyku [HTML](/cs/web/html/), ale je navržen pro kapesní elektronická zařízení, jako jsou smartphony a PDA. [Specifikace formátu souboru HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) byly předloženy W3C ke standardizaci, ale nemohly se stát standardem. HDM je založen na specifikacích formátu souboru [HDML](/cs/web/hdml/), které jsou k dispozici na webu W3.

## Formát souboru HDM – Další informace

Soubor HDM se skládá ze značek, které se vykreslují na vizuálně navržený web na kapesních zařízeních. Soubory HDM se zkopírují do zařízení pomocí protokolu HDTP (Handheld Device Transport Protocol) namísto protokolu HTTP, který se používá pro stránky HTML.

## Prvky souboru HDML

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

