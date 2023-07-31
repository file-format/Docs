{
  "date" : "2021-08-24",
  "keywords" :[ "soubor trc", "formát souboru trc", "co je soubor trc", "soubor", "příklad trc", "přípona souboru trc", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru TRC a rozhraních API, která mohou vytvářet a otevírat soubory TRC.",
  "title" :"TRC - SQL Server Trace File",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Co je soubor TRC?
Soubor s příponou .trc obsahuje výsledky trasování aktivity databáze serveru SQL společnosti Microsoft. Tyto soubory jsou vytvořeny softwarem SQL Server Profiler; obvykle součástí softwaru Microsoft SQL Server. Správci databáze mohou analyzovat posloupnost databázových příkazů a mohou zkontrolovat protokol trasování, pokud existuje podezření na nějaký druh chyb nebo varování. Tyto soubory jsou obvykle umístěny v typické složce LOG MSSQL v adresáři Program Files v operačním systému Windows.

## Formát souboru TRC
Formát souboru TRC používá SQL Server Profiler k automatickému generování nové stopy nedávno provedených příkazů na serveru MS SQL. SQL Server Profiler používá výchozí šablonu pro jakékoli nové trasování. Software však obsahuje několik předdefinovaných šablon pro monitorování určitých typů událostí. SQL Server Profiler lze také použít k vytvoření šablon, které definují třídy událostí a datové sloupce, které mají být zahrnuty do trasování.

### Předdefinované šablony
Zde je seznam některých předdefinovaných šablon zahrnutých v SQL Server Profiler:
- **SP_Counts**: Zachycuje chování provádění uložené procedury v průběhu času.
- **Standardní**: Obecný výchozí bod pro vytváření trasování.
- **TSQL**: Zachycuje všechny příkazy Transact-SQL, které klienti odesílají na SQL Server, a čas vydání.
- **TSQL_Duration**: Zachycuje všechny příkazy Transact-SQL odeslané na SQL Server klienty, dobu jejich provádění a seskupuje je podle doby trvání.
- **TSQL_Grouped**: Používá se ke zkoumání dotazů od konkrétního klienta nebo uživatele.
- **TSQL_Locks**: Slouží k odstraňování problémů se zablokováním, časovým limitem uzamčení a událostmi eskalace uzamčení.
- **TSQL_Replay**: Slouží k provádění iterativního ladění, jako je srovnávací testování.
- **TSQL_SPs**: Slouží k analýze kroků součástí uložených procedur.
- **Tuning**: Slouží k vytvoření výstupu trasování, který může Poradce pro ladění databázového stroje použít jako pracovní zátěž pro ladění databází.
### Korelujte trasování s daty protokolu výkonu systému Windows
SQL Server Profiler lze použít k otevření protokolu výkonu Microsoft Windows, k výběru čítačů pro korelaci s trasováním a zobrazení vybraných čítačů výkonu vedle trasování v GUI MS SQL Server Profiler. Chcete-li označit data protokolu výkonu, která korelují s vybranou událostí trasování, použijte svislý červený pruh v podokně dat sledování systému SQL Server Profiler.


## Reference ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

