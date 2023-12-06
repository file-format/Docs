{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 File - iOS SHSH Blob File Format",
  "description":"Další informace o tom, co je soubor SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Co je soubor SHSH2?

Soubor SHSH2, také známý jako SHSH blob nebo ECID SHSH, je digitální podpis používaný společností Apple k ověřování a ověřování aktualizací firmwaru pro zařízení iOS, jako jsou iPhony, iPady a iPody. Obsahuje jedinečný identifikátor zařízení, který je známý jako ECID (Exclusive Chip ID). Obsahuje také informace o verzi firmwaru nainstalovaného v zařízení.

## Formát souboru SHSH2 – Další informace

Soubory SHSH2 se ukládají na disk v binárním formátu souboru a podrobnosti o interní struktuře souboru tohoto formátu souboru nejsou veřejně dostupné.

Když je na zařízení Apple, jako je iPhone, iPad nebo Mac nainstalována nová verze iOS, vygeneruje se soubor SHSH2. Tento soubor SHSH2 je odeslán na servery Apple, které přečtou a ověří tento soubor digitálního podpisu. Na základě těchto informací server povolí nebo zabrání instalaci.

Totéž se stane, když je požadována aktualizace. Když uživatel požádá o aktualizaci nebo obnovení svého zařízení prostřednictvím iTunes nebo jiného softwaru, servery společnosti Apple zkontrolují, zda soubor SHSH2 odpovídá ECID zařízení a verzi firmwaru, než umožní aktualizaci pokračovat.

## Reference

* [SHSH Blob – z Wikipedie](https://en.wikipedia.org/wiki/SHSH_blob)
* [Spořič TSS](https://tsssaver.1conan.com/v2/)

