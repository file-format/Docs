{
"date":"2023-07-06",
   "keywords":[
"KOČKA",
"Soubor CAT",
"CAT Windows",
"soubor",
"přípona souboru cat",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CAT - soubor katalogu Windows",
   "description":"Další informace o formátu CAT a rozhraních API, která mohou vytvářet a otevírat soubory CAT.",
"linktitle":"CAT",
   "menu":{
      "docs":{
         "identifier":"system-cat",
         "parent":"system"
}
},
"lastmod":"2023-07-06"
}

## Co je soubor CAT?

Katalogový soubor Windows, také známý jako soubor .cat, hraje v operačním systému Windows zásadní roli tím, že zajišťuje integritu a autentičnost různých souborů. V podstatě slouží jako digitálně podepsaný soubor, který obsahuje kryptografické hodnoty hash souborů, které katalogizuje, a také digitální podpis od důvěryhodné autority.

Primárním účelem souboru .cat je umožnit ověření systémových souborů, ovladačů nebo softwarových komponent během instalace nebo během provozu systému. Když instalujete ovladač nebo softwarový balíček, systém Windows zkontroluje digitální podpis odpovídajícího souboru .cat, aby potvrdil, že soubory, na které odkazuje, nebyly od doby jejich podpisu změněny nebo změněny. Pomocí souborů .cat může systém Windows ověřit pravost souborů a zjistit jakékoli neoprávněné úpravy. Toto bezpečnostní opatření pomáhá zabránit instalaci nebo spuštění potenciálně škodlivých nebo kompromitovaných souborů v systému Windows.

## Formát souboru CAT – Další informace

Zde jsou některé důležité informace o souborech katalogu systému Windows:

- **Ověření:** Katalogové soubory Windows se používají k ověření integrity a pravosti jiných souborů, jako jsou systémové soubory, ovladače nebo softwarové komponenty.
- **Digitální podpis:** Soubor .cat obsahuje digitální podpis od důvěryhodné autority. Tento podpis zajišťuje, že katalogový soubor a soubory, na které odkazuje, nebyly od doby jejich podpisu změněny.
- **Kryptografický hash:** Soubor .cat obsahuje kryptografické hodnoty hash souborů, které katalogizuje. Tyto hodnoty hash fungují jako jedinečný otisk pro každý soubor a používají se k detekci jakýchkoli úprav nebo manipulace.
- **Detekce manipulace:** Během instalace nebo provozu systému Windows kontroluje digitální podpis a kryptografické hodnoty hash v souboru .cat, aby se ujistil, že související soubory nebyly zmanipulovány nebo kompromitovány.
- **Prevence malwaru:** Použití souborů .cat pomáhá zabránit instalaci nebo spuštění potenciálně škodlivých nebo neautorizovaných souborů v systému Windows. Zvyšuje úroveň zabezpečení ověřením integrity a pravosti souborů před povolením jejich instalace nebo spuštění.
- **Systémová integrita:** Systém Windows spoléhá na soubory .cat, aby zachoval integritu svých systémových souborů a komponent. Pokud se zjistí, že některé soubory byly změněny nebo kompromitovány, systém Windows je může odmítnout nainstalovat nebo spustit, aby byla chráněna stabilita a bezpečnost operačního systému.
- **Nasazení a aktualizace:** Soubory .cat se běžně používají během procesu nasazení a aktualizace ovladačů, softwarových balíčků a aktualizací systému Windows. Zajišťují, že v systému Windows jsou nainstalovány nebo aktualizovány pouze autentické a nezměněné soubory.

**Poznámka:**

Soubory katalogu systému Windows (.cat) mohou pomoci potlačit vícenásobná vyskakovací okna dialogu důvěryhodnosti pro stahování nových softwarových komponent. Když je softwarová komponenta doprovázena souborem .cat podepsaným důvěryhodnou autoritou, ustanoví se, že komponenta pochází z důvěryhodného zdroje.

Jakmile uživatel zvolí „Vždy důvěřovat obsahu“ od distributora softwaru, budoucí stahování od stejného distributora, které využívá soubor .cat, bude považováno za důvěryhodné. V důsledku toho systém Windows pro tyto soubory nezobrazuje vyskakovací okno důvěryhodnosti, protože již byly označeny jako důvěryhodné na základě předchozího rozhodnutí uživatele.

Tato funkce zjednodušuje uživatelské prostředí snížením počtu vyskakovacích dialogů důvěryhodnosti, které se zobrazují pro soubory ze známého a důvěryhodného zdroje. Využitím důvěry vytvořené prostřednictvím souboru .cat může systém Windows zefektivnit proces instalace nebo spouštění softwarových komponent od konkrétního distributora v budoucnu.

## CAT Windows

CAT Windows může také znamenat příkaz "cat" v příkazovém řádku Windows (CMD), používá se k zobrazení obsahu textového souboru přímo v okně příkazového řádku. Nativní příkazový řádek Windows však neobsahuje vestavěný příkaz "cat" jako v systémech založených na Unixu.

Chcete-li dosáhnout podobné funkce ve Windows, můžete použít příkaz "type". Zde je příklad, jak použít příkaz "type" ve Windows CMD:

```
C:\>type filename.txt
```

Nahraďte "filename.txt" skutečnou cestou a názvem textového souboru, který chcete zobrazit. Příkaz vypíše obsah souboru přímo v okně příkazového řádku.

Případně, pokud používáte PowerShell, obsahuje alias „cat“ pro příkaz „Get-Content“. Zde je jeden příklad:

```
PS C:\>cat filename.txt
```

Znovu nahraďte "filename.txt" cestou a názvem textového souboru, který chcete zobrazit.

Upozorňujeme, že pokud pracujete s binárními soubory nebo netextovým obsahem, nemusí použití příkazu „type“ nebo „cat“ poskytnout smysluplné výsledky, protože jsou primárně určeny pro zobrazování textových souborů.

## Jaký je Windows ekvivalent příkazu cat pro Unix?

Příkaz "type" ve Windows je ekvivalentem příkazu "cat" v Unixu, jak je uvedeno výše.

## Jaký je formát souboru CAT?

Binární


