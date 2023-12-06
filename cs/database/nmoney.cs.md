{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů NMONEY a rozhraních API, která mohou vytvářet a otevírat soubory NMONEY.",
  "title" :"Soubor NMONEY - Formát souboru účtu Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Co je soubor NMONEY?

Soubor NMONEY je soubor databáze úložiště finančních dat, který obsahuje záznamy o finančních transakcích. Byl vyvinut společností Nickvision a byl použit v softwaru Nickvision Denaro, což je osobní finanční softwarová aplikace. Data uložená v souboru NOMONEY zahrnují informace o kreditních a debetních transakcích na účtu.

Soubory NOMONEY lze otevřít pomocí aplikace [Github](https://github.com/NickvisionApps/Denaro).

## O softwaru Denaro

Denaro původně vyvinula [Nickvision](https://nickvision.org/) jako produkt, který byl později převeden na softwarovou aplikaci s otevřeným zdrojovým kódem hostovanou na [Github](https://github.com/NickvisionApps/Denaro) . Od té doby byla aplikace upravena a aktualizována pouze na Github. Aplikace je vyvinuta v C# v uživatelském rozhraní Windows s Windows App SDK (WinUI 3 jako v současnosti).

### Funkce nabízené společností Denaro

* Spravujte více účtů současně s nejoblíbenějším a nejznámějším rozhraním karet
* Filtrujte transakce podle typu, skupiny nebo data
* Opakujte transakce, jako jsou účty, ke kterým dochází každý měsíc
* Převod peněz z jednoho účtu na druhý
* Exportujte data z účtu jako soubor CSV a importujte soubor CSV, OFX nebo QIF pro přidání transakcí do účtu

## Formát souboru Denaro – Další informace

Soubory Denaro se ukládají na disk v binárním formátu souboru. Finanční data jsou uložena jako databázový soubor ve formátu **.SQLITE3**. SQLITE je odlehčený databázový soubor SQL vytvořený pomocí softwaru SQLite. Poskytuje samostatný databázový stroj, který je schopen poskytovat plně funkční a vysoce spolehlivou databázi. Databázové soubory SQLite lze použít ke sdílení bohatého obsahu mezi systémy jednoduchou výměnou těchto souborů po síti. SQLite vazby existují pro programovací jazyky jako C, [C#](/cs/programming/cs/), [C++](/cs/programming/cpp/), [Java](/cs/programming/java/), [PHP](/cs/programming/ php/) a mnoho dalších.

## Reference

* [Nickvision](https://nickvision.org/)
* [NIckVision – Github](https://github.com/NickvisionApps/Denaro)

