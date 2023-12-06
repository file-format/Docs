{
"date":"2023-10-18",
   "keywords":[
"cpi",
"soubor cpi",
"informační soubor kódové stránky cpi",
"jak otevřít soubor cpi",
"soubor",
"přípona souboru cpi",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CPI - Informační soubor kódové stránky",
   "description":"Další informace o formátu souboru CPI Codepage Information a rozhraních API, která mohou vytvářet a otevírat soubory CPI.",
"linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
         "parent":"system"
}
},
"lastmod":"2023-10-18"
}

## Co je soubor CPI?

Soubor `.cpi` je v kontextu operačních systémů Microsoft Windows a DOS obvykle **"Informační soubor kódové stránky."** Tyto soubory obsahují informace o kódových stránkách používaných pro kódování textu a mapování znakových sad. Kódové stránky jsou nezbytné pro zobrazování a zpracování textu v různých jazycích a znakových sadách.

V kontextu Windows a DOS se kódové stránky používají k definování toho, jak jsou znaky reprezentovány a kódovány v různých jazycích a oblastech. Tyto kódové stránky určují, jak se znaky ukládají do paměti a zobrazují na obrazovce. Každá kódová stránka má jedinečný identifikátor a soubory `.cpi` ukládají informace o těchto kódových stránkách, včetně podrobností, jako je mapování znaků a informace o písmech.

Soubory `.cpi` se běžně nacházejí v systémových adresářích Windows nebo DOS a hrají klíčovou roli v tom, že umožňují operačnímu systému správně zobrazovat text pro různá národní prostředí a znakové sady. Pomáhají systému pochopit, jak interpretovat a vykreslovat znaky z různých jazyků a kódování.

## Informační soubory kódové stránky

Podívejme se blíže na informační soubory kódové stránky (.cpi) a na to, jak fungují v rámci systému MS-DOS a dřívějších verzí systému Microsoft Windows:

1. **Kódování znaků a kódové stránky**: Kódové stránky jsou kritickou součástí toho, jak je text kódován a zobrazen na počítači. Definují kódování znaků pro konkrétní jazyk nebo znakovou sadu. Každá kódová stránka přiřazuje znakům číselné hodnoty (kódové body), což umožňuje počítači je reprezentovat a zobrazovat. Například kódová stránka 437 se běžně používá ve Spojených státech a západní Evropě, zatímco kódová stránka 850 se používá pro kódování Latin-1.
    







2. **Inicializace systému**: Během inicializace systému (při spouštění počítače) by MS-DOS a starší verze Windows přečetly soubory `.cpi`, aby určily, které kódové stránky mají podporovat. Tyto informace byly zásadní pro vykreslování textu, zadávání z klávesnice a převod znakových sad.
    







3. **Podpora displeje a klávesnice**: Tyto soubory poskytují informace o tom, jak by se znaky měly zobrazovat na obrazovce a které znakové sady nebo kódové stránky by měly být podporovány pro zadávání z klávesnice. Různé kódové stránky definují různé znakové sady, takže tyto soubory pomáhají operačnímu systému vědět, jak správně zacházet s uživatelským vstupem a zobrazovat text.
    







4. **Lokalizace**: Soubory `.cpi` jsou nezbytné pro lokalizaci operačního systému. Umožňují systému přizpůsobit se různým jazykům, regionům a znakovým sadám, což umožňuje uživatelům na celém světě používat MS-DOS nebo Windows v preferovaných jazycích.
    







5. **Více souborů `.cpi`**: Na počítači s podporou více jazyků můžete najít několik souborů `.cpi` odpovídajících různým kódovým stránkám. Systém může mít například `437.cpi` pro Spojené státy, `850.cpi` pro Latin-1, `852.cpi` pro střední Evropu a tak dále. Načte se příslušný soubor na základě národního prostředí uživatele nebo vybrané kódové stránky.
    







6. **Informace o písmech**: Kromě mapování znaků mohou tyto soubory obsahovat informace o písmech, které určují, která písma se mají použít pro jednotlivé kódové stránky. To je důležité pro vykreslení textu ve vhodném stylu a velikosti.
    







7. **Starší systémy**: Soubory `.cpi` byly běžnější ve starších verzích MS-DOS a Windows. Moderní verze systému Windows (například Windows 10 a novější) obvykle používají pro kódování textu Unicode, který podporuje širokou škálu znaků a jazyků. Unicode zjednodušuje zpracování textu pro vícejazyčná prostředí a je standardem pro moderní software.

## Jak otevřít soubor CPI?

Otevření souboru .CPI (Code Page Information) není typickou akcí uživatele a tyto soubory obecně nejsou určeny k ručnímu otevírání. Jsou používány operačním systémem ke správě kódování textu a znakových sad ak jejich obsahu systém automaticky přistupuje a využívá jej.

Pokud však máte zájem o prohlížení obsahu souboru .CPI pro informační účely, můžete jej zkusit otevřít pomocí textového editoru nebo hexadecimálního prohlížeče. Zde je, jak se můžete pokusit otevřít soubor .CPI:

1. **Textový editor**: K otevření a zobrazení souboru .CPI můžete použít textový editor, jako je Poznámkový blok (v systému Windows) nebo jakýkoli editor prostého textu v jiných operačních systémech. Mějte na paměti, že obsah souborů .CPI není zamýšlen tak, aby byl čitelný pro člověka a můžete vidět řadu znaků, které je obtížné interpretovat.
    







2. **Hexadecimální prohlížeč**: K otevření a kontrole obsahu souboru .CPI v jeho surové binární podobě lze použít hexadecimální prohlížeč nebo hex editor. Hexadecimální editory poskytují podrobnější pohled na data souboru, což může být užitečné, pokud se snažíte porozumět jeho struktuře. Příklady takového softwaru zahrnují HxD, Hex Fiend (pro macOS) a 010 Editor.

## Jiné soubory CPI

Zde jsou další typy souborů, které používají příponu souboru **.cpi**.

**Video a systém**
- [CPI - Informace o videoklipu AVCHD](/cs/video/cpi/)
- [CPI - Informační soubor kódové stránky](/cs/system/cpi/)

## Reference
* [Kódová stránka](https://en.wikipedia.org/wiki/Code_page)

