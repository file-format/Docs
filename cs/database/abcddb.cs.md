{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souboru ABCDDB a rozhraních API, která mohou vytvářet a otevírat soubory ABCDDB.",
  "title" : "Formát souboru ABCDDB – soubor databáze seznamu kontaktů Apple Address Book",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-cs",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Co je soubor ABCDDB?

Soubor s příponou **.ABCDDB** je zkratka pro Apple Address Book Contact List Database. Patří do aplikace **Adresář** také běžně známá jako **Kontakty**. Je to vestavěná aplikace a je součástí operačních systémů iOS a macOS. Aplikace Kontakty umožňuje uživatelům ukládat a organizovat informace související s jejich kontakty, včetně jednotlivců, firem a organizací. Tato aplikace umožňuje uživatelům sledovat podrobnosti, jako jsou jména, adresy, telefonní čísla a e-mailové adresy, a také kategorizovat své kontakty do skupin.

## Vztah s SQLite a typická cesta

Adresář společnosti Apple (také známý jako Kontakty) ukládá kontaktní informace jako vCard do složky metadat. **Soubor _ABCDDB_ je ve skutečnosti datový soubor _SQLite 3_**.

SQLite je populární systém pro správu databází, který je navržen tak, aby byl lehký a samostatný. Používá se v mnoha různých typech softwaru a zařízení. SQLite je typ RDBMS, což znamená, že ukládá data do tabulek, které spolu souvisí pomocí klíčů. Dokáže zpracovat řadu datových typů, včetně celých čísel, čísel s plovoucí desetinnou čárkou, řetězců a binárních dat. SQLite navíc podporuje transakce, které uživatelům umožňují provádět více databázových operací společně jako jednu jednotku práce.

Zde je obvykle uložen soubor s příponou ABCDDB

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Oprava poškozené databáze kontaktů

Než se o to pokusíte, nejprve si udělejte zálohu. Pak prosím přejděte na

`~/Library/Application Support/AddressBook`

V tomto adresáři najdete tři soubory včetně toho s příponou .abcddb

- `adresář-v22.abcddb`
- `adresář-v22.abcddb-wal`
- `adresář-v22.abcddb-shm`

Odstraňte všechny tyto soubory a znovu otevřete Kontakty, začne znovu fungovat.

## Obnovte databázi adresáře ze zálohy

Předpokládejme, že kontakty z databáze adresáře jsou uloženy v `addressbook-v22.abcddb`

- Nejprve zálohujte data adresáře a ukončete všechny aplikace.
- Přesuňte soubor databáze do podadresáře `~/Library/Application Support/AddressBook`
- Spusťte **Adresář.app**.

## Exportujte data souboru ABCDDB do aplikace Microsoft Access

Protože soubor je datový soubor SQLite 3, můžete data v souboru abcddb exportovat do Microsoft Access pomocí konektoru ODBC.

Konektor SQLite ODBC je softwarová knihovna a ovladač, který umožňuje aplikacím podporujícím rozhraní ODBC připojit se k databázi SQLite. Zahrnuje knihovnu, která definuje rozhraní ODBC, a ovladač, který toto rozhraní převádí na volání SQLite API. Chcete-li využít konektor SQLite ODBC, musíte jej nejprve nainstalovat a poté nastavit zdroj dat ODBC na vašem počítači. Po dokončení těchto kroků se každá aplikace vybavená podporou ODBC bude moci připojit ke zdroji dat a načíst data z databáze SQLite.

## Reference
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Databáze kontaktů pro Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Jak mohu otevřít nebo exportovat soubor abcddb ve Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

