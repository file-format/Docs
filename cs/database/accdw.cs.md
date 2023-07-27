{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů ACCDW a rozhraních API, která mohou vytvářet a otevírat soubory ACCDW.",
  "title" :"ACCDW - Microsoft Access Database Link File",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## Co je soubor ACCDW?

Soubor s příponou .accdw je odkazový soubor vytvořený pomocí Microsoft Access a obsahuje informace o odkazu ke stažení databázového souboru Accessu, tj. [ACCDB](/cs/database/accdb/) ze serveru SharePoint. To umožňuje uživatelům sdílet databázové soubory, které jsou hostovány vzdáleně. Otevřením souboru ACCDW se stáhne propojený soubor ACCDB jako místní kopie do počítače uživatele. Stažený soubor se uloží do výchozího umístění pro stahování a lze k němu přistupovat tak, že do něj přejdete. Obvykle se tyto soubory stahují a ukládají pod názvem "SiteServer.accdb", který odkazuje na databáze klientů.

## Formát souboru ACCDW – Další informace

Soubor ACCDW je soubor XML, který poskytuje odkaz na web SharePoint, kde jsou hostovány služby Access Services. Je to pouze zkratka a ke spuštění vyžaduje připojení k internetu. V případě online se SharePoint ukládá do místní mezipaměti, aby bylo možné jej později přepnout do režimu offline.

## Reference

* [Stažený soubor .accdw](https://learn.microsoft.com/en-us/shows/)
* [Specifikace Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Stahování souboru .accdw](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file?forum=sharepointgeneralprevious)
* [Jaký formát souboru Access mám použít?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=cs-cz&rs=cs-cz&ad=us)

