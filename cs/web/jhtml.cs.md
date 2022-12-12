{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml", "soubor jhtml", "formát souboru jhtml", "typ souboru jhtml", "soubor", "typ", "co je soubor jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Java HTML File",
  "description":"Další informace o formátu souborů JHTML a rozhraních API, která mohou vytvářet a otevírat soubory JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Co je soubor JHTML?

Soubor s příponou .jhtml je [HTML](/cs/web/html/) soubor s [Java](/cs/programming/java/) kódem, který se spustí na serveru, když klient požádá o tuto stránku v prohlížeči. Server zpracuje požadavky, provede funkce Java obsažené ve funkci a vrátí stránku do prohlížeče klienta. Objekty Java vložené do stránek JHTML běží na serveru pro zpracování požadavků na stránky tohoto typu. Soubory JHTML mohou také přistupovat k informacím z databáze pomocí připojení JDBC (Java [Database](/cs/database/) Connectivity). Soubory JHTML lze otevřít v libovolném textovém editoru a prohlížet ve webových prohlížečích, jako je Google Chrome, Firefox a Safari.

## Formát souboru JHTML

JHTML je patentovaná technologie společnosti ATG a lze ji vytvořit pomocí editoru dokumentů ATG (Art Technology Group) Dynamo Document Editor. Soubory JHTML se zapisují ve formátu prostého textu pomocí standardního kódu HTML a Java. Ty obsahují kromě proprietárních značek, které odkazují na objekty Java, standardní značky HTML. Když uživatel takovou stránku požaduje, HTTP server předá požadavek Java aplikačnímu serveru. Stránka JHTML je nejprve převedena na soubor .java a zkompilována tak, aby vygenerovala soubor [.class](/cs/programming/class/), který se spustí jako servlet. Tím se vygeneruje proud standardních dat HTTP a HTML, který se vrátí zpět do žádajícího prohlížeče a zobrazí se uživateli. To je užitečné pro spouštění dotazů souvisejících s databází na serveru a vrácení konečného nashromážděného výsledku do prohlížeče klienta.

## Reference

* [Globální struktura dokumentu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

