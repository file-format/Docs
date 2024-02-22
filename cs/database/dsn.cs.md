{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souboru DSN a rozhraních API, která mohou vytvářet a otevírat soubory DSN.",
  "title" : "Formát souboru DSN - Soubor názvu zdroje databáze",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-cs",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Co je soubor DSN?

DSN znamená Název zdroje dat a je to formát souboru používaný k ukládání informací o připojení k databázi. Soubory DSN se obvykle používají ve spojení s ODBC (Open Database Connectivity) a umožňují snadný přístup ke konkrétní databázi poskytnutím nezbytných informací pro připojení k ní, jako je název serveru, uživatelské jméno a heslo. Soubor je obvykle ve formátu prostého textu a lze jej vytvořit a upravit pomocí textového editoru. Lze jej použít na různých operačních systémech, jako jsou Windows, Linux a Mac.

## Jak vytvořit soubor DSN?

Způsob vytvoření souboru DSN se může lišit v závislosti na operačním systému a dostupných nástrojích. Následující kroky poskytují obecný přehled procesu vytváření souboru DSN v systému Windows.

1. Otevřete Správce zdrojů dat ODBC vyhledáním Zdroje dat ODBC v nabídce Start.
2. Vyberte kartu System DSN a klikněte na tlačítko Add.
3. Vyberte příslušný ovladač pro databázi, ke které se chcete připojit, a klikněte na Dokončit.
4. Vyplňte potřebné informace pro připojení k databázi, jako je název serveru, uživatelské jméno a heslo.
5. Klikněte na OK pro uložení souboru DSN.

Alternativně můžete soubor DSN vytvořit ručně vytvořením souboru ve formátu prostého textu s příponou .dsn a zadáním nezbytných informací o připojení ve formátu:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Cestu k tomuto souboru pak můžete použít jako DSN ve vašem kódu/skriptu pro připojení k databázi.

## Programy, které otevírají soubor DSN

Soubor DSN je soubor ve formátu prostého textu, který ukládá informace používané k připojení k databázi, jako je název serveru, uživatelské jméno a heslo. Obvykle se používá ve spojení s ODBC (Open Database Connectivity) pro zajištění snadného přístupu ke konkrétní databázi.

Chcete-li otevřít a zobrazit obsah souboru DSN, můžete použít jakýkoli textový editor, jako je Poznámkový blok, Sublime Text, Atom atd. Tyto programy vám umožní otevřít soubor DSN a zobrazit informace o připojení v něm uložené.

Chcete-li však použít soubor DSN pro připojení k databázi a provádět operace jako SELECT, INSERT, UPDATE, DELETE atd., program s podporou ODBC, jako je programovací jazyk jako Python, Java, C# nebo nástroj pro správu databází, jako je Microsoft Access , je vyžadováno SQL Server Management Studio. Tyto programy mohou použít informace v souboru DSN k připojení k databázi a provedení požadované operace.

## Reference

* [Co je DSN (název zdroje dat)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



