{
  "date" : "2021-06-29",
  "keywords" :[ "XAR", "soubor", "přípona", "formát souboru", "Soubor automatického obnovení Excel", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru XAR a rozhraních API, která mohou vytvářet a otevírat soubory XAR.",
  "title" :"XAR - Formát souboru automatického obnovení Microsoft Excel",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
      "identifier": "spreadsheet-xar",
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor XAR?

Soubor s příponou .xar je soubor Microsoft Excel Recvoery, který se generuje spolu s hlavními soubory tabulky Excel. Používá se jako soubor pro obnovu, pokud aplikace nefunguje správně nebo se neočekávaně zavře, což má za následek ztrátu dat hlavního souboru. Tyto soubory pro obnovení jsou kvůli rychlosti a jednoduchosti uloženy ve stejném původním formátu souboru. Excel navrhne původní formát a název souboru při opětovném otevření obnoveného souboru, který uloží do systémového registru pro obnovení.

## Formát souboru XAR

Soubory XAR jsou soubory obnovy uložené v binárním formátu na disk spolu s hlavním souborem aplikace Excel. Ty jsou uloženy jako skryté soubory na disku s libovolnými názvy, které odkazují na hlavní excelový soubor ze systémového registru. Všechny otevřené soubory se aktivně a pravidelně ukládají do výchozí přípony jako skryté soubory XAR a ukládají se na disky s názvy jako ~ar8EF9.xar.

## Jak obnovit soubor Excel ze souboru XAR?

Soubory XAR mohou ukládat všechny typy formátů souborů aplikace Excel, jako jsou XLS, XLSX a další. Pokud se váš soubor Excel Spreadsheet neočekávaně zavře, můžete otevřít Excel nebo poklepat na soubor a automaticky vás požádá o obnovení z uloženého souboru pro obnovení, který můžete uložit se stejným názvem souboru jako původní pro pozdější použití.

## Reference

* [Funkce Atuo Recover v Excelu](https://docs.microsoft.com/en-us/office/troubleshoot/excel/autorecover-functions-in-excel)
* [Nápověda komunity souborů XAR](https://answers.microsoft.com/en-us/msoffice/forum/msoffice_excel-mso_win10-mso_365hp/2016-excel-xar-files/5af5e10c-027a-4c24-a403-39e9c590ce8f)

