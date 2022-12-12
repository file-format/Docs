{
  "date" : "2020-03-16",
  "keywords" :[ "Soubor DXF", "Formát souboru", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru DXF a rozhraních API, která mohou vytvářet a otevírat soubory DXF.",
  "title" :"Formát souboru DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DXF?

DXF, Drawing Interchange Format nebo Drawing Exchange Format, je reprezentace tagovaných dat výkresového souboru AutoCADu. Každý prvek v souboru má předponu celé číslo nazývané kód skupiny. Tento skupinový kód ve skutečnosti představuje prvek, který následuje, a označuje význam datového prvku pro daný typ objektu. DXF umožňuje reprezentovat téměř všechny uživatelem specifikované informace ve výkresovém souboru.

Formát souboru DXF byl vyvinut společností Autodesk jako formát datového souboru CAD pro datovou interoperabilitu mezi AutoCADem a dalšími aplikacemi. Data lze tedy importovat z jiných formátů do DXF do AutoCADu podle specifikací interoperability formátu souboru DXF.

## Stručná historie ##


Historie formátu souborů DXF sahá až do roku 1982, kdy byl představen jako součást AutoCADu 1.0. Počáteční verze AutoCADu podporují pouze formát souboru ASCII DXF. S vydáním 10 AutoCADu (a vyšším) v roce 1988 byla v AutoCADu zavedena podpora jak pro ASCII, tak i pro binární formát souborů DXF. V dřívějších fázích Autodesk nesdílel žádné specifikace formátu souborů a díky tomu nebylo snadné importovat soubory DXF. Autodesk však nyní publikuje specifikace DXF a je k dispozici široké veřejnosti.

## Specifikace formátu souboru ##

Formát souboru DXF používá k uspořádání obsahu do sekcí skupinový kód a páry hodnot. Každá sekce se skládá ze záznamů, kde každý záznam se skládá ze skupinového kódu a datové položky. Každý kód skupiny a hodnota jsou v souboru DXF na samostatném řádku. Každá sekce začíná skupinovým kódem 0 následovaným řetězcem SECTION. Následuje kód skupiny 2 a řetězec označující název sekce (například SECTION1). Každá sekce se skládá ze skupinových kódů a hodnot, které definují její prvky. Část končí 0 následovanou řetězcem ENDSEC.

Formát souboru DXF bere v úvahu objekty odlišné od entit. Objekty zde nemají žádnou grafickou reprezentaci, ale entity ji mají. Záznamy v DXF jsou tedy označovány jako grafické objekty, zatímco objekty jsou označovány jako negrafické objekty. Sekce BLOCK a ENTITIES souboru DXF obsahují entity a použití skupinových kódů v těchto dvou částech je totožné. Konec entity je označen další skupinou 0, která začíná další entitou nebo označuje konec sekce.

### Struktura souboru ###

Sekce v souboru DXF jsou uspořádány v následujícím pořadí:

|Oddíl|Základní popis
---|---|
|Záhlaví|Tato část obsahuje obecné informace o výkresu. Je to jako funkce Nastavení v telefonu, která obsahuje různé proměnné spojené s výkresem a jeho přidružené hodnoty. Například sekce Záhlaví definuje, kterou verzi AutoCADu soubor DXF používá (proměnná $ACADVER) nebo jednotku použitou k měření úhlů v souboru (proměnná $AUNITS)
|Třídy|Sekce CLASSES obsahuje informace pro třídy definované aplikací, jejichž instance se objevují v sekcích databáze BLOCKS, ENTITIES a OBJECTS.
|Tabulky|Tato část obsahuje definice pro několik různých tabulek, z nichž každá obsahuje řadu různých položek symbolů. Například [typ řádku](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- Tabulka 847B-5BBE36EC6FDF-htm.html) (LTYPE) definuje vzor čárek, teček, textu a symbolů v souboru DXF a způsob jejich změny. Zde je úplný seznam tabulek v této sekci:<ul><li> Tabulka ID aplikace (APPID).</li><li> Tabulka záznamu bloku (BLOCK_RECORD).</li><li> Tabulka Dimension Style (DIMSTYPE).</li><li> Tabulka vrstev (LAYER).</li><li> Tabulka typů čar (LTYPE).</li><li> Tabulka stylu textu (STYLE).</li><li> Tabulka uživatelského souřadnicového systému (UCS).</li><li> Zobrazit (VIEW) tabulku</li><li> Tabulka konfigurace výřezu (VPORT).</li></ul>
|Bloky|Tato část obsahuje grafické objekty a entity výkresu, které tvoří odkaz na každý blok ve výkresu.
|Entity|Tato část obsahuje aktuální objektová data a grafické entity výkresu. To může zahrnovat nezpracovaná data – například entita kruhu je definována svou tloušťkou, středovým bodem, svým poloměrem a směrem vysunutí.
|Objekty|Zde najdete negrafické části výkresu. Jsou zde uloženy například slovníky AutoCADu.

## Reference ##

* [Specifikace souboru DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF z Wikipedie](https://en.wikipedia.org/wiki/AutoCAD_DXF)

