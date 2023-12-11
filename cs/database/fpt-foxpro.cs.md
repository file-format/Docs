{
"datum": "2023-06-12",
  "keywords": [
"fpt",
"fpt soubor",
"soubor foxpro fpt",
"FoxPro Table Memo",
"co je soubor fpt",
"jak otevřít soubor fpt",
"soubor",
"přípona souboru fpt",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru FPT - FoxPro Table Memo",
  "description":"Další informace o formátu FPT FoxPro a rozhraních API, která mohou vytvářet a otevírat soubory FPT.",
  "linktitle": "FPT FoxPro",
  "menu": {
    "docs": {
      "identifier": "database-fpt-foxpro",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Co je soubor FPT?

Soubor "FPT" je přípona souboru spojená se systémem správy databáze FoxPro. V FoxPro soubor FPT obsahuje pole typu memo přidružená k tabulce. Memo pole se používají k ukládání velkého množství textu nebo binárních dat, jako jsou dlouhé popisy, dokumenty nebo obrázky, které se nemusí vejít do běžného databázového pole.

Zde je návod, jak funguje struktura souborů FoxPro:

- **DBF (databázový soubor):** Toto je hlavní soubor, který obsahuje strukturovaná data v tabulkovém formátu, včetně běžných polí. Každý záznam odpovídá řádku v tabulce a každé pole v záznamu odpovídá sloupci.

- **FPT (Memo File):** Soubor FPT se používá k ukládání poznámkových polí spojených se záznamy v souboru DBF. Každé pole poznámky odpovídá záznamu v souboru DBF a soubor FPT ukládá skutečný obsah poznámky.

- **CDX (Index File):** Tyto soubory ukládají indexy, které zlepšují výkon vyhledávání a řazení dat v souboru DBF.

Pokud máte databázi FoxPro s poli typu memo, měli byste mít pro každou tabulku odpovídající soubory DBF, FPT a případně CDX. Soubor FPT obsahuje binární data a není určen k přímému otevření v textovém editoru. Místo toho je přístupný a spravovaný prostřednictvím aplikace FoxPro nebo jiných kompatibilních databázových nástrojů.

## Vztah s FoxPro

Soubor FPT je spojen s FoxPro, což je systém správy relačních databází (DBMS), který byl původně vyvinut společností Fox Software a později získaný společností Microsoft. Dodává se v různých verzích, přičemž Visual FoxPro (VFP) je jednou z nejznámějších. Visual FoxPro byl výkonný a oblíbený systém pro správu databází používaný pro vývoj desktopových a klient-server aplikací.

Mezi klíčové funkce Visual FoxPro patří:

- **Tabulární úložiště dat:** Umožňuje uživatelům vytvářet a spravovat strukturovaná data v tabulkách, s poli a záznamy podobnými jiným databázovým systémům.
- **Podpora pro pole typu Memo:** Visual FoxPro měl podporu pro pole typu Memo, která mohla ukládat velké množství textu nebo binárních dat.
- **Interaktivní vývojové prostředí:** Mělo vizuální vývojové prostředí, kde jste mohli navrhovat formuláře, sestavy a aplikace pomocí grafického rozhraní.
- **Podpora SQL:** Visual FoxPro podporoval SQL (Structured Query Language), který umožňoval dotazování a manipulaci s daty pomocí standardní syntaxe SQL.
- **Objektově orientované programování:** Visual FoxPro podporoval objektově orientované programování, což umožnilo vytvářet modulárnější a udržovatelnější aplikace.
- **Indexování a vyhledávání:** Poskytuje možnosti indexování pro rychlejší vyhledávání a třídění dat.
- **Nástroje pro vytváření sestav:** Visual FoxPro obsahoval nástroje pro vytváření a generování sestav na základě dat uložených v databázi.
- **Kompatibilita:** Umožňuje integraci s dalšími produkty a technologiemi společnosti Microsoft.

Upozorňujeme, že společnost Microsoft ukončila běžnou podporu pro Visual FoxPro v roce 2007 a rozšířená podpora skončila v roce 2015. To znamená, že i když stávající aplikace vyvinuté pomocí FoxPro mohou stále fungovat, neexistují žádné oficiální aktualizace nebo opravy zabezpečení poskytované společností Microsoft. Moderní trendy vývoje se navíc posunuly směrem k webovým a cloudovým aplikacím a objevily se novější systémy pro správu databází.

## Jak otevřít soubor FPT?

Programy, které otevírají soubory FPT, zahrnují

- Microsoft Visual FoxPro (placené)

## Jiné soubory FPT

- [FPT - Alpha Five Table Memo File](/cs/database/fpt-alphafive/)
- [FPT - FileMaker Pro Database Memo File](/cs/database/fpt/)

## Reference
* [Visual FoxPro](https://en.wikipedia.org/wiki/Visual_FoxPro)

