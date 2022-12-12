{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PDF/A",
  "description":"Další informace o formátu souborů PDF/A a rozhraních API, která mohou vytvářet a otevírat soubory PDF/A.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co je PDF/A? #

PDF/A je standardní formát ISO pro archivaci elektronických dokumentů ve formátu PDF. Jeho primárním důvodem vzniku bylo splnění požadavků dlouhodobé archivace. Norma zajišťuje otevírání archivovaných souborů i po dlouhé době tím, že ukládá určitá omezení na nedílné součásti dokumentu pro dosažení shody. Formát je nyní široce přijímán ve všech průmyslových odvětvích. Prohlížeče PDFA/A, jako je Adobe Acrobat Reader, zajišťují, že soubory uložené v tomto formátu lze otevřít i v budoucnu v souladu s informacemi sdílenými tímto standardem.

## PDF/A verze ##

PDF/A byl přijat jako norma ISO v říjnu 2005. Od té doby je neustále vylepšován a postupem času bylo vyvinuto několik dalších norem. Informace o standardech PDF/A publikovaných v průběhu času a jejich podrobnosti jsou následující:

* **PDF/A-1:** publikováno v říjnu 2005 jako ISO 19005-1 a je založeno na PDF 1.4
* **PDF/A-2:** publikováno v červnu 2011 jako ISO 19005-2 a je založeno na PDF 1.7 (ISO 32000-1:2008)
* **PDF/A-3:** publikováno v říjnu 2012 jako ISO 19005-3 a je založeno na PDF 1.7 (ISO 32000-1:2008)

## PDF/A-1 ##

Standard PDF/A-1 vycházel z původní verze PDF 1.4. Standard PDF/A-1 definuje dvě úrovně shody pro soubory PDF.

### PDF/A-1a ###

Je v souladu s úrovní A a splňuje všechny požadavky ve specifikacích normy PDF/A-1. PDF/A-1a zajišťuje, že text lze z dokumentu extrahovat. Rovněž zaručuje, že přirozený proces čtení integrovaného textového materiálu zůstane nedotčen. PDF/A ukládá požadavek na schopnost reprezentace textu na zmenšených obrazovkách restrukturalizací, která je známá jako „tagované PDF“. Jeho záměrem bylo zvýšit dostupnost vyhovujících souborů pro tělesně postižené uživatele tím, že umožní pomocný software.

### PDF/A-1b ###

PDF/A-1b je nižší úroveň shody a zabývá se vizuálním vzhledem elektronických dokumentů s ohledem na normu ISO 19005. Zajišťuje jednotnou reprodukci textu a dalšího obsahu na stránkách. Tato shoda úrovně B označuje minimální shodu, aby bylo zajištěno, že vykreslený vizuální vzhled vyhovujícího souboru bude dlouhodobě zachován.

## PDF/A-2 ##

PDF/A-2 byl vydán standardem ISO v červenci 2011 jako nový standard známý jako ISO 32001-1. Tento nový standard nejen těžil ze všech funkcí verzí PDF až do 1.7, ale byl také zaveden jako nový standard. PDF/A-2 zahrnovalo následující funkce jako součást tohoto nového standardu.

* PDF/A-2 se dodává s podporou [JPEG2000](/cs/image/jp2/), která je užitečná v případě skenovaných dokumentů.
* Podporuje vkládání kolekcí PDF/A, které lze použít k vytvoření kontejneru PDF s dalšími podobnými soubory
* Podporuje funkci průhlednosti souborů PDF jako celek ve srovnání s PDF/A-1, kde byla podporována částečně.
* PDF/A-2 poskytuje podporu pro volitelný obsah, který je užitečný pro mapové aplikace a technické výkresy. Tyto jsou také známé jako vrstvy, které lze zviditelnit nebo skrýt podle požadavků prohlížející osoby.
* Specifikuje požadavky na vlastní metadata XMP
* Přidá některé z novějších typů komentářů do seznamu zakázaných typů poznámek. Kromě toho byly do seznamu přijatelných položek přidány některé z novějších typů komentářů, jako jsou komentáře pro úpravy textu.

## PDF/A-3 ##

PDF/A-3 zahrnuje všechny požadavky na shodu úrovně 2 a umožňuje vkládání dalších formátů souborů (jako je XML, [CSV](/cs/spreadsheet/csv/), [CAD](/cs/cad/), [textový editor] (/cs/textový procesor/) , [tabulkový procesor](/cs/tabulkový procesor/) a další) do dokumentů vyhovujících PDF/A.

## Reference ##

* [PDF/A – z Wikipedie](https://en.wikipedia.org/wiki/PDF/A)
* [Bílá kniha: PDF/A – Základy](http://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

