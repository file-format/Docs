{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf soubor", "co je sdf soubor", "jak otevřít sdf soubor", "přípona", "soubor", "formát souboru sdf", "typ souboru databáze", "formát databázového souboru", "Soubory databáze" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů SDF a rozhraních API, která mohou vytvářet a otevírat soubory SDF.",
  "title" :"SDF - SQL Server Compact Database File",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Co je soubor SDF?
Soubor s příponou .sdf obsahuje databázi Microsoft SQL Server Compact (SQL CE), která je také známá jako kompaktní relační databáze; vyrobené společností Microsoft pro aplikace vytvořené pro mobilní zařízení a stolní počítače. Podporuje 32 i 64 bitový operační systém a kompletní obsah databáze je obsažen v jediném souboru SDF a může zabírat více než 4 GB místa na disku. Z bezpečnostních důvodů lze soubor .sdf zašifrovat 128bitovým šifrováním. Běhové prostředí SQL CE zajišťuje paralelní víceuživatelský přístup k souboru .sdf. Soubor SDF lze zkopírovat pomocí **QuickOnce** nebo jej lze jednoduše zkopírovat do cíle pro nasazení systému.

## Formát souboru SDF
Soubor SDF obsahuje databázi, která se obvykle nazývá kompaktní relační databáze. Soubor SDF obsahuje všechny informace související s databází a SQL Server Compact je lehký a bezplatný databázový stroj, který se používá ke správě souborů .sdf. Velikost souboru .sdf by neměla překročit limit 4 GB velikosti. Soubory SDF neukládají informace o uložených procedurách, triggerech nebo pohledech. Aplikace používající databázi SQL CE nemusí uvádět cestu k souboru SDF v připojovacím řetězci ADO.NET, místo toho ji lze uvést jako |DataDirectory|\název_databáze.sdf, definující datový adresář definovaný v manifestu sestavení pro aplikaci.
Konvence pojmenování .sdf je volitelná a k uložení souboru lze použít libovolnou příponu. Nastavení hesla pro soubor databáze je volitelný krok. Pro komprimaci nebo opravu databáze by měl být soubor uložen s možností **komprimovaná/opravená databáze**.

## Reference

* [SQL Server Compact – Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Používání SQL Server Compact pro webové aplikace ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


