{
"date":"2023-01-04",
   "keywords":[
"cs",
"cs soubor",
"cs cleo vlastní skript",
"jak otevřít soubor cs",
"soubor",
"přípona souboru cs",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CS - vlastní skript CLEO",
   "description":"Další informace o formátu CS CLEO Custom Script a rozhraních API, která mohou vytvářet a otevírat soubory CS.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo",
         "parent":"game"
}
},
"lastmod":"2023-01-04"
}

## Co je soubor CS?

Soubor .CS v kontextu CLEO (zkratka pro CLEO Library) obvykle odkazuje na soubor vlastního skriptu používaný v sérii videoher Grand Theft Auto (GTA). CLEO je populární modelovací rámec, který umožňuje hráčům vytvářet a přidávat vlastní skripty do her GTA, které jim umožňují upravovat hru, přidávat nové funkce a zlepšovat celkový herní zážitek.

## Přehled souboru CS

Zde je základní přehled toho, co může soubor .cs v CLEO obsahovat:

1. **Kód skriptu**: Soubor .cs obsahuje kód skriptu napsaný ve skriptovacím jazyce CLEO. Tento skriptovací jazyk je specifický pro CLEO a používá se k definování chování vlastních skriptů ve hře. Kód lze napsat pomocí textového editoru a obvykle se řídí specifickou syntaxí.
    









2. **Úpravy**: Skripty CLEO mohou provádět různé úpravy hry, jako je změna chování objektů ve hře, vytváření vlastních misí, přidávání nových vozidel, zbraní a další. Možnosti jsou široké a závisí na kreativitě a programátorských schopnostech autora scénáře.
    









3. **Spouštěče**: Skripty CLEO často obsahují spouštěče, které určují, kdy a jak se má vlastní skript spustit. Tyto spouštěče mohou být založeny na událostech ve hře, akcích hráčů nebo specifických podmínkách.
    









4. **Proměnné a funkce**: Skripty CLEO mohou používat proměnné k ukládání a manipulaci s daty, stejně jako funkce k zapouzdření a opětovnému použití kódu. Tyto proměnné a funkce se používají k řízení chování skriptu.

## Příklad souboru CS

Zde je jednoduchý příklad skriptu CLEO .cs, který mění počasí ve hře:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## Knihovna CLEO

**CLEO Library**, často označovaná jednoduše jako „CLEO“, je populární a výkonná moddingová struktura pro sérii videoher Grand Theft Auto (GTA). Umožňuje hráčům a modderům vytvářet a přidávat do her GTA vlastní skripty, které jim umožňují upravovat hru, přidávat nové funkce a zlepšovat celkový herní zážitek. CLEO je zvláště dobře známý pro svou flexibilitu a snadné použití v komunitě GTA modding.

Zde jsou některé klíčové funkce a aspekty knihovny CLEO:

1. **Skriptovací jazyk**: CLEO představuje svůj skriptovací jazyk, který je specifický pro modding framework. Skriptovací jazyk je navržen tak, aby byl relativně snadno srozumitelný a pracoval s tím, aby byl přístupný začínajícím i zkušeným modderům.
    









2. **Vlastní skripty**: Pomocí CLEO můžete vytvářet vlastní skripty, které mohou provádět širokou škálu funkcí v herním světě. Tyto skripty mohou měnit chování ve hře, přidávat nové mise, představovat nová vozidla nebo zbraně, měnit herní fyziku a mnoho dalšího.
    









3. **Spouštěče a události**: Skripty CLEO mohou být spouštěny různými událostmi ve hře, akcemi hráčů nebo specifickými podmínkami. To umožňuje modderům vytvářet dynamický a interaktivní obsah ve hře.
    









4. **Podpora pro více verzí GTA**: CLEO má verze přizpůsobené různým hrám GTA, včetně GTA III, GTA Vice City, GTA San Andreas, GTA IV a dalších. To znamená, že moddeři mohou vytvářet a sdílet své vlastní skripty pro různé tituly GTA.

## Formáty souborů používané knihovnou CLEO

V moddingu CLEO pro hry Grand Theft Auto (GTA) se k vytváření a instalaci modů běžně používá několik formátů souborů. Tyto formáty souborů slouží k různým účelům od obsahu skutečných skriptů po ukládání dalších zdrojů, jako jsou textury, modely nebo zvuk. Zde jsou některé z klíčových formátů souborů používaných v moddingu CLEO:

1. **.cs (Custom Script)**: Soubory CLEO .cs jsou soubory vlastních skriptů napsané ve skriptovacím jazyce CLEO. Tyto soubory obsahují kód, který definuje chování a funkčnost mod. Soubory .cs jsou jádrem moddingu CLEO a jsou spouštěny hrou za účelem implementace vlastních funkcí.
    









2. **.csa (Custom Script Archive)**: Soubory .csa jsou archivy, které mohou ukládat více souborů skriptů .cs. Často se používají ke sbalení souvisejících skriptů pro snadnější instalaci a správu.
    









3. **.fxt (textové soubory)**: Soubory .fxt jsou textové soubory, které lze použít k lokalizaci nebo poskytování překladů textu pro mody CLEO. Obsahují textové řetězce, které lze zobrazit ve hře a zpřístupňují tak hráče v různých jazycích.
    









4. **[.bmp](/cs/image/bmp/), [.png](/cs/image/png/), [.jpg](/cs/image/jpeg/) (formáty obrázků)**: Tyto formáty obrázků jsou slouží k ukládání textur a obrázků pro mody. Lze je použít pro vlastní vzhledy, textury vozidel, prvky HUD a další. V závislosti na hře mohou být preferovány různé formáty obrázků.

## Jak otevřít soubor CS?

Chcete-li otevřít a zobrazit obsah souboru CLEO .cs (Custom Script), můžete použít textový editor nebo editor kódu dle vlastního výběru. Mezi běžné možnosti patří:

- **Poznámkový blok**: Jednoduchý textový editor, který je dodáván s předinstalovaným systémem Windows.
- **Poznámkový blok++**: Textový editor s více funkcemi určený pro kódování a skriptování.
- **Visual Studio Code**: Populární, bezplatný a vysoce rozšiřitelný editor kódu.
- **Sublime Text**: Další editor kódu známý svou rychlostí a všestranností.
- **Atom**: Editor kódu s otevřeným zdrojovým kódem vyvinutý společností GitHub.

## Další soubory CS

Zde jsou další typy souborů, které používají příponu souboru **.cs**.

**Datové soubory a hra**
- [CS - ColorSchemer Studio Color Scheme](/cs/data/cs-colorschemer/)
- [CS - Vlastní skript CLEO](/cs/game/cs-cleo/)

**Programování**
- [CS - CSharp Code File](/cs/programming/cs/)

## Reference
* [Knihovna CLEO](https://cleo.li/)

