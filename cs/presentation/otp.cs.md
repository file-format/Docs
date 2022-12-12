{
  "date" : "2021-01-21",
  "keywords" :[ "soubor otp", "formát souboru otp", "co je soubor otp", "soubor", "příklad otp", "přípona souboru otp", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument Presentation Template",
  "description":"Další informace o formátu souboru OTP a rozhraních API, která mohou vytvářet a otevírat soubory OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Co je soubor OTP?

Soubory s příponou .otp představují soubory prezentačních šablon vytvořených aplikacemi ve standardním formátu OASIS OpenDocument. Obsahem takového souboru jsou prezentační informace ve formě snímků s textem, obrázky, tvary, multimediálním obsahem, přechodovými efekty a dalšími prvky snímků. Tyto soubory šablon se používají k rychlému vytváření nových prezentací na základě informací o stylu uložených v samotné šabloně. Soubory OTP lze vytvářet a ukládat pomocí několika různých aplikací, jako je Impress, který je součástí sady OpenOffice a Microsoft PowerPoint. Formát souboru OTP je podobný souborům šablon Microsoft PowerPoint [.pot](/cs/presentation/pot/) a [.potx](/cs/presentation/potx/).

## Formát souboru OTP

Formát souboru OTP je založen na standardu OpenDocument, který podporuje reprezentaci dokumentu jako jeden dokument XML a také shromažďování několika dílčích dokumentů v jediném zazipovaném balíčku ve formátu [ZIP](/cs/compression/zip/). Obsah souboru je distribuován ve více souborech xml zabalených společně. Tyto soubory [XML](/cs/web/xml/) obsahují informace o stylu, obsahu, metainformacích a nastavení dokumentu, jak je uvedeno níže.

* `content.xml` – Obsah dokumentu a automatické styly použité v obsahu.
* `styles.xml` – Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
* `meta.xml` – Metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
* `settings.xml` – Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

## Reference

* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

