{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "soubor mht", "formát souboru mht", "typ souboru mht", "soubor", "typ", "co je soubor mht" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML formát souboru",
  "description" :"Další informace o formátu souborů MHT a rozhraních API pro vytváření a otevírání souborů MHT.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Co je soubor MHT?

Soubor s příponou .mht je formát archivačního souboru s povoleným MIME, který obsahuje různé typy dat do jednoho souboru. Může ukládat data jako text, obrázky, styly stránek ve formě souborů [CSS](/cs/web/css/), JavaScript a další zdroje jako vložené prostředky. Soubory MHT, které mají typ MIME message/rfc822, zapouzdřují veškerý obsah souboru HTML jako jeden archivní soubor pro uložení při archivaci na úložných zařízeních. Softwarové aplikace, jako je Microsoft Word, vám umožňují převést dokumenty WORD do formátu MHT exportem jako soubor MHT. Soubory MHT lze otevřít pomocí oblíbených prohlížečů, jako je Microsoft Internet Explore a Google Chrome.

## Formát souboru MHT

Stejně jako [MHTML](/cs/web/mhtml/) je MHT také zapouzdřením MIME agregovaných HTML dokumentů. Obsah dokumentu uvnitř dokumentu MHT, jako jsou vložené obrázky, šablony stylů, aplety atd., je kódován MIME tam, kde jsou propojeny s kořenovým zdrojem prostřednictvím URI. E-mailoví klienti, jako je Microsoft Outlook, ukládají e-maily (obvykle [EML](/cs/email/eml/)) ve formátu MHT. Úplné specifikace formátu souboru MHT jsou k dispozici v [RFC 822](https://tools.ietf.org/html/rfc822) a lze je použít pro vývoj softwarových aplikací, které mohou zpracovávat soubory MHT.

## Rozdíl mezi MHT a MHTML

Při ukládání online stránky je uživatel požádán, aby se rozhodl, jaký druh formátu souboru musí být online stránka uložena v nativním systému. Nejčastěji se uživatel zaměňuje mezi značkovacím jazykem a formáty souborů MHTML. Všimli si, že je problematické vidět, že formát souboru je mezi těmito formáty zdravější.

Když se uživatel rozhodne vyhnout se plýtvání online stránkou jako značkovacím jazykem, vytvoří se složka, která obsahuje více souborů pro různý obsah stránky, tj. zcela odlišné jednotky oblasti souborů vytvořené pro text, grafiku, applety atd. Na druhou stranu online stránka jako MHTML vytvoří jeden soubor pro celou online stránku. Všechny prvky stránky spolu s grafikou, odkazy a alternativními soubory jsou vložené do jednoho souboru.

Přirozeně je snadné pracovat se soubory MHT nebo MHTML, protože soubor, který lze chránit a sdílet jednoduše prostřednictvím e-mailu. Jednotka oblasti souborů značkovacího jazyka však pod šancí ztráty informací, protože ztráta nebo smazání byť jednoho souboru by mohla způsobit, že kompletní složka značkovacího jazyka nebude pro uživatele k ničemu.

## Reference

* [MHTML – Wikipedie](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

