{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH File - iPhone/iPod Touch SHSH Blob File Format",
  "description":"Další informace o tom, co je soubor SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Co je soubor SHSH?

Soubor SHSH, také známý jako Signature HaSH, je digitální podpis používaný společností Apple k ověřování a ověřování aktualizací firmwaru pro zařízení iOS, jako jsou iPhony, iPady a iPody.

## Rozdíl mezi formáty souborů SHSH a SHSH2

Stejně jako soubor SHSH2 obsahuje soubor SHSH jedinečný identifikátor zařízení nazvaný „ECID“ (Exclusive Chip ID) a také informace o verzi firmwaru nainstalovaného v zařízení. Soubory SHSH se však používaly ve starších verzích systému iOS (před iOS 10) a od té doby byly nahrazeny soubory SHSH2.

## Formát souboru SHSH – Další informace

Soubory SHSH se ukládají na disk v binárním formátu souboru. Podrobnosti o interní struktuře souboru tohoto formátu souboru nejsou veřejně dostupné.

Soubory SHSH jsou důležité pro uživatele, kteří chtějí downgradovat firmware svého zařízení na předchozí verzi, kterou již Apple nepodepisuje. Uložením souborů SHSH pro konkrétní verzi firmwaru, když je stále podepsán společností Apple, je uživatelé mohou později použít k obejití ověření podpisu společnosti Apple a nainstalovat tuto verzi firmwaru do svého zařízení. Tento proces je také známý jako „útěk z vězení“.

## Reference

* [SHSH Blob – z Wikipedie](https://en.wikipedia.org/wiki/SHSH_blob)
* [Spořič TSS](https://tsssaver.1conan.com/v2/)

