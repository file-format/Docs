{
"date":"2023-11-09",
   "keywords":[
"zoo",
"zoo soubor",
"komprimovaný soubor zoo",
"jak otevřít soubor zoo",
"soubor",
"přípona souboru zoo",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Soubor ZOO - Co je soubor .zoo a jak jej otevřít?",
   "description":"Další informace o formátu komprimovaných souborů ZOO a rozhraních API, která mohou vytvářet a otevírat soubory ZOO.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Co je soubor ZOO?

Soubor `.zoo` je formát archivu, který se používá ke kompresi a ukládání souborů a adresářů; je podobný jiným formátům archivů, jako jsou `.zip`, `.tar` a `.rar`. Formát `.zoo` byl populární v počátcích počítačů, ale v posledních letech se stal méně obvyklým. Původně byl vyvinut **Rahul Dhesi** a byl používán především na systémech Unix a DOS.

Soubor `.zoo` obvykle obsahuje jeden nebo více souborů a adresářů, které byly zkomprimovány a archivovány do jednoho souboru. Soubory `.zoo` můžete vytvářet a extrahovat pomocí různých softwarových nástrojů, které tento formát podporují.

Archivy ZOO mají jedinečnou funkci, která jim umožňuje ukládat více verzí stejného souboru za předpokladu, že každá verze byla změněna k jinému datu. To znamená, že uživatelé ZOO mohou ukládat a přistupovat k předchozím iteracím souboru přímo z archivu ZOO. Tato funkce umožňuje uživatelům vrátit se k dřívější verzi souboru nebo porovnat starší verzi s novější a nabízí pohodlný způsob správy revizí a změn souborů v průběhu času.

## Běžné operace se soubory ZOO

Zde jsou některé běžné operace spojené se soubory `.zoo`:

1. **Vytvoření souboru `.zoo`:** K vytvoření souboru `.zoo` můžete použít nástroj příkazového řádku, jako je "zoo". Například následující příkaz vytvoří archiv `.zoo` z adresáře:
    








`zoo a -c archiv.adresář zoo/`
    








V tomto příkazu "a" znamená "add", "-c" určuje kompresi a "archive.zoo" je název výstupního archivu.
    








2. **Extrakce souborů ze souboru `.zoo`:** Chcete-li extrahovat obsah archivu `.zoo`, můžete použít tento příkaz:
    








`zoo a archiv.zoo`
    








Tento příkaz rozbalí soubory ze souboru `archive.zoo`.
    








3. **Výpis obsahu souboru `.zoo`:** Obsah archivu `.zoo` můžete vypsat, aniž byste jej extrahovali pomocí možnosti „l“:
    








    








`zoo l archiv.zoo`

## Jak otevřít soubor ZOO?

Mezi programy, které otevírají soubory ZOO, patří

- **zoo** (zdarma) pro (Windows, Linux)

## Reference
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
