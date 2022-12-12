{
  "date" : "2019-10-11",
  "keywords" :[ "soubor aba", "formát souboru aba", "co je soubor aba", "soubor", "příklad aba", "přípona souboru aba", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText File Format",
  "description":"Další informace o formátu souboru ABA a rozhraních API, která mohou vytvářet a otevírat soubory ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Co je soubor ABA?

Soubor s příponou .aba je formát souboru Australské banky bankéřů (ABA) nebo [Cemtext](https://www.cemtexaba.com/), který používají banky pro dávkové transakce. Používá jej většina bank pro vedení finančních záznamů. Formát souboru ABA, známý také jako soubor přímého vstupu, byl přijat většinou australských bank jako výchozí formát pro dávkové transakce. Stále nebyl uznán jako standardní formát navzdory skutečnosti, že jej používají Bank of Queensland, NAB a Westpac. Soubory ABA lze otevřít pomocí libovolného textového editoru, jako je Notepad++.


## Formát souboru ABA

Soubor ABA používá formát ASCII k ukládání dat pro předávání nebo načítání do bankovních systémů. Formát byl zachován jednoduchý, aby bylo možné snadno integrovat do vlastního finančního systému společnosti pro zpracování dávek transakcí. Například ve mzdovém systému lze nahrát dávku transakcí ke zpracování v jednom přístupu. Specifikace formátu souboru ABA jsou k dispozici jako úplný přepis na webu [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) a lze na ně odkazovat pro vývojáře .

Soubor ABA se skládá z několika řádků, přičemž každý řádek je znám jako „záznam“. V souboru ABA jsou tři hlavní záznamy:

* Popisný záznam
* Detailní záznam
* Celkový záznam souboru

### Popisný záznam

"Popisný záznam" obsahuje informace, jako je pořadové číslo cívky, název finanční instituce uživatele, název souboru, který poskytuje použití, a další informace.

### Detailní záznam

Typ "Podrobný záznam" zahrnuje informace, jako je číslo banky/státu/pobočky, číslo účtu, který má být připsán/odepsán, indikátor, kód transakce, částka a další informace.

### Celkový záznam souboru

Typ "File Total Record" zahrnuje typ záznamu 7, BSB Format Filler, File (Uživatel) Čistá celková částka, Soubor (Uživatel) Kredit Celková částka, Soubor (Uživatel) Debet Celková částka a další informace.

### Kódy transakcí

Seznam platných kódů transakcí je následující. V souborech ABA se většinou používá kód "53 - Pay". Tyto kódy transakcí zahrnují debetní, kreditní a srážkové daně.

|Kód|Popis transakce|
---|---|
|13|Externě iniciované debetní položky|
|50|Externě iniciované kreditní položky s výjimkou těch, které nesou kódy transakcí|
|51|Bezpečnostní zájem australské vlády|
|52|Rodinný příspěvek|
|53|Zaplatit|
|54|Důchod|
|55|Přidělení|
|56|Dividenda|
|57|Debenture/Note Interest|


## Příklad souboru ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Reference

* [Cemtext ABA](https://www.cemtexaba.com/)

