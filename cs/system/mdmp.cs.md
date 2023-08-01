{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP File - Windows Minidump File Format",
  "description":"Další informace o formátu souboru MDMP a rozhraních API, která mohou vytvářet a otevírat soubory MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Co je soubor MDMP?

Soubor MDMP je výpis paměti aplikace v systému Microsoft Windows, který se vytvoří, když se aplikace neobvykle zavře nebo zhroutí. Obsahuje informace a výpisy dat, které lze použít k odladění příčiny selhání. Soubory MDMP jsou použitelné v aplikacích vytvořených jakoukoli platformou, jako je Java, C++, .NET a další. Kromě MDMP,

Aplikace, které mohou otevírat soubory MDMP, zahrnují Microsoft Visual Studio Debugger.

## Formát souboru MDMP

Soubory MDMP se ukládají jako binární soubory na disk a lze je otevřít pomocí ladicího programu Microsoft Visual Studio. Obsahuje následující informace, které vám pomohou identifikovat důvod selhání.

* Podrobnosti o zprávě Stop, její parametry a další data
* Seznam načtených ovladačů
* Kontext procesoru (PRCB) pro procesor, který přestal fungovat
* Informace o procesu a kontext jádra (EPROCESS) pro proces, který se zastavil
* Zpracovat informace a kontext jádra (ETHREAD) pro vlákno, které se zastavilo
* Zásobník volání v režimu jádra pro vlákno, které se zastavilo

Tyto informace pomáhají zjistit, co se stalo, vyřešit problém a zabránit jeho opakování.

### Analyzujte minidump

K vytvoření souboru výpisu paměti vyžaduje systém Windows stránkovací soubor na spouštěcím svazku. Stránkovací soubor je vytvořen na spouštěcím svazku a měl by mít velikost alespoň 2 megabajty (MB). Soubor výpisu se vytvoří při zhroucení aplikace. V případě druhého problému se vytvoří druhý malý soubor s výpisem paměti, zatímco předchozí zůstane zachován. Název souboru výpisu je odlišný, aby nedošlo k přepsání.

Systém Windows uchovává seznam všech souborů s výpisem stavu paměti ve složce %SystemRoot%\Minidump. Soubory MDMP můžete analyzovat jejich spuštěním v Visual Studio Debugger, jak je uvedeno v níže uvedených krocích.

## Jak otevřu soubor MDMP ve Visual Studiu?

Následující kroky lze použít k otevření souboru MDMP v sadě Visual Studio.

* V sadě Visual Studio z nabídky Soubor zvolte Otevřít | Výpis stavu systému .
* Přejděte na soubor výpisu, který chcete otevřít.
* Vyberte Otevřít.

## Odkaz

* [Jak číst soubor s malým výpisem paměti, který je vytvořen systémem Windows, pokud dojde k selhání](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

