{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDE File - Co je soubor MDE a jak jej otevřít?",
  "description":"Přečtěte si o formátu souboru MDE a rozhraních API, která mohou vytvářet a otevírat soubory MDE.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-cs-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

## Co je soubor MDE?

Soubor .MDE je zkompilovaná verze databáze Accessu (MDB nebo Accdb). Když zkompilujete databázi Accessu do souboru .MDE, již ji nelze upravovat pomocí standardních návrhových nástrojů Accessu. Primárním účelem vytvoření souboru .MDE je distribuce databázové aplikace bez odhalení původního zdrojového kódu.

## Formát souboru MDE

Soubor MDE se vytvoří kompilací kódu VBA, formulářů, sestav a dalších objektů. Výsledkem je vytvoření binárního formátu souboru MDE. Výsledný soubor .MDE lze distribuovat uživatelům, kteří mohou aplikaci spustit, ale nemohou upravit návrh nebo zobrazit původní kód. Soubor MDE je ve skutečnosti zkompilovaná verze [.MDA souboru](/database/mda/). Distribuce souborů .MDE může pomoci chránit duševní vlastnictví tím, že uživatelům zabrání v přístupu nebo úpravě zdrojového kódu. Může také zvýšit výkon při kompilaci a optimalizaci kódu.

## Reference

* [Specifikace přístupu](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Neoficiální průvodce MDB] (http://jabakobob.net/mdb/)