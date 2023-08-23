{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "rozšíření", "soubor", "formát", "Comic Books", "Comic Books File Format", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru CBC a rozhraních API, která mohou vytvářet a otevírat soubory CBC.",
  "title" :"CBC - Comic Book Collection File Format",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Co je soubor CBC?

Soubor s příponou .cbc je komprimovanou sbírkou souborů komiksů pro elektronické knihy a obsahuje soubory [CBZ](/cs/ebook/cbz/) a [CBR](/cs/ebook/cbr/). Používá jej [Calibre](https://calibre-ebook.com/), aplikace pro převod elektronických knih, což je multiplatformní open-source správce elektronických knih a umožňuje vám spravovat vaše elektronické knihy a převádět je do různých formátů. . Soubor CBC obsahuje soubor .txt, comics.txt, který uvádí další soubory, které jsou součástí archivu. Online je k dispozici několik aplikací, které dokážou převést soubory CBC na [AZW3](/cs/ebook/azw3/), [EPUB](/cs/ebook/epub/), [FB2](/cs/ebook/fb2/), [MOBI](/cs/ebook/ mobi/), [TXT](/cs/word-processing/txt/), [PDF](/cs/pdf/) a další oblíbené formáty souborů.

## Formát souboru CBC

Soubory CBC jsou komprimované archivy, které obsahují CBZ, CBR a textový soubor pro výpis obsahu. Textový soubor, comics.txt, je kódován UTF8 a obsahuje seznam souborů CBC, které mají čtenáři použít k uspořádání svých sbírek. Soubor CBC má obvykle několik atributů, které umožňují organizaci této sbírky, jako je Comic, Category, Publisher, Series, Edition a Artist.

Obsah ukázkového souboru CBC je uveden následovně:

* comics.txt – Textový soubor, který obsahuje seznam souborů CBR a CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Soubor(y) CBZ

kde soubor comics.txt uvádí obsah takto:

* 1.cbz: První kapitola
* 2.cbz: Druhá kapitola
* 3.cbz: Třetí kapitola

Čtenáři zpracují soubor comics.txt a vygenerují obsah na základě poskytnutých dat.

## Reference

* [Calibre](https://calibre-ebook.com/)

