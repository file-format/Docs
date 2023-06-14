{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ATOM File - Atom Syndication Format",
  "description" :"Zjistěte, co je soubor ATOM a rozhraní API, která mohou vytvářet a otevírat soubory ATOM.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Co je soubor ATOM?

Soubor ATOM je syndikační formát pro strukturu zdrojů Atom a vstupních dokumentů. Podobně jako soubory .RSS je formát souboru ATOM syndikační formát založený na XML, který je standardem pro publikování obsahu. Soubor ATOM se používá pro webové kanály, které softwarovým programům umožňují kontrolovat aktualizace publikované na webu. Obsahuje položky, které mohou být různého typu, jako jsou titulky, fulltextové články, úryvky nebo odkazy na obsah na webu.

Mezi aplikace, které mohou **otevřít soubory ATOM**, patří **Apple Safari**.

## Formát souboru ATOM – Další informace

Soubory ATOM jsou ukládány a publikovány v oblíbeném formátu XML, který je univerzálním formátem pro výměnu informací. Byl vyvinut jako alternativa k RSS s ohledem na omezení a nedostatky formátu souborů RSS.

### Typy dokumentů Atom

1. `Atom Entry Documents` – Jedná se o XML dokument, který se skládá z jediné položky informací, známé jako vstup, pro Atom feed. To má atom:entry prvek, který obsahuje řadu podřízených prvků. Obsah položky Atom může být prostý text, HTML, XHTML nebo jiný typ média IANA (Internet Assigned Numbers Authority).
1. „Dokumenty Atom Feed Documents“ – Jedná se o dokument XML, který poskytuje metadata o zdroji Atom a jeden nebo více záznamů pro zdroj. Když klient požádá o informace ze zdroje, server vygeneruje dokument zdroje, který obsahuje řadu položek Atom pro splnění požadavku.
1. `Atom Collection` – Jedná se o speciální druh dokumentu zdroje Atom, který obsahuje adresy URL položek Atom, které lze upravit.

## Reference

* [Formát syndikace Atom – RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Přehled Atom Feeds – IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom – Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))

