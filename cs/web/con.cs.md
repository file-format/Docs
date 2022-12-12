{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor CON - Formát zdrojového souboru aplikace Concept",
  "description" :"Zjistěte, co je soubor CON a rozhraní API, která mohou vytvářet a otevírat soubory CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Co je soubor CON?

Soubor CON je soubor zdrojového kódu pro aplikaci vyvinutou pro **Concept Application Server**. Používá se pro psaní aplikací pro výměnu dat mezi serverem a uživatelem. Soubory CON hostované na serveru jsou přístupné pomocí webového prohlížeče za předpokladu, že je na straně uživatele nainstalován Concept Client. Concept Application Server je webový server s malým programovacím jazykem, který může mít podmnožinu databázového stroje [SQL](/cs/database/sql/) (TinDB).

Soubory CON lze otevřít/spustit pomocí RadGs Concept Application Server.

## Formát souboru CON – Další informace

Soubory CON jsou umístěny na serveru a lze k nim přistupovat pomocí webového prohlížeče na počítači uživatele. Koncept [adresy URL](/cs/web/url/) se liší od běžných adres URL HTTP a začínají řetězcem **koncept://**.

### Příklad URL souboru CON

K souboru CON hostovanému na Concept Application Server lze přistupovat prostřednictvím webového prohlížeče pomocí adres URL, jako jsou:

```
concept://domain.server.com/web_application/main.con.
```
## Reference

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

