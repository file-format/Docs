{
  "date" : "2019-10-11",
  "keywords" :[ "chm", "soubor chm", "formát souboru chm", "typ souboru chm", "soubor", "typ", "co je soubor chm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Kompilovaný formát souboru nápovědy HTML",
  "description" :"Zjistěte, co je soubor CHM a rozhraní API, která je mohou vytvářet a otevírat.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je to CHM soubor?

Formát souboru CHM představuje soubor nápovědy Microsoft **[HTML](/cs/web/html/)**, který se skládá z kolekce stránek HTML. Poskytuje rejstřík pro rychlý přístup k tématům a navigaci do různých částí dokumentu nápovědy. V souboru CHM lze vyhledávat obsah pomocí poskytnuté možnosti vyhledávání. CHM je proprietární formát souboru online nápovědy společnosti Microsoft, který se často používá pro dokumentaci softwaru. Kromě toho se používá v několika dalších aplikacích, jako jsou školicí příručky, interaktivní knihy a elektronické zpravodaje. Většina moderních vývojových prostředí Microsoft podporuje generování dokumentace CHM z informací dostupných v aplikaci.

Jedinečná schopnost formátu souboru CHM implementovat kombinovaný obsah a index jej odlišuje od jiných standardních stránek HTML. Vygenerovaný soubor CHM má relativně malou velikost, a proto jej lze snadno distribuovat se softwarovými balíčky. Nástroj pro tvorbu nápovědy HTML Help Workshop poskytuje snadno použitelný systém pro vytváření a správu projektů nápovědy a souvisejících souborů. Soubory CHM mohou obsahovat text, obrázky a hypertextové odkazy; zobrazitelné ve webovém prohlížeči; používá Windows a další programy jako řešení online nápovědy.

## Formát souboru CHM

Konečná podoba vygenerovaného CHM souboru závisí na tom, jak je systém nápovědy navržen a zda je určen pro aplikaci nebo webovou stránku. Soubor CHM podporuje kompresi dat s kompresí LZX pro generování komprimovaných souborů HTML. Má vestavěný vyhledávač pro rychlé vyhledávání obsahu spolu se schopností sloučit více souborů .CHM. Soubor CHM se skládá ze sady souborů HTML, propojeného obsahu a indexového souboru.

### Soubory HTML

Ať už vytváříte témata nápovědy pro distribuci pomocí programu nebo na webu, vámi vytvořené dokumenty jsou vytvářeny pomocí speciálního formátovacího jazyka známého jako HTML (Hypertext Markup Language). Soubory témat HTML mají příponu názvu souboru .htm nebo .html.

Ačkoli každé téma nápovědy nebo webová stránka, kterou vytvoříte, se jeví jako dokument s textem, grafikou nebo animovanými obrázky, soubory .htm jsou ve skutečnosti textové dokumenty, které mají speciální kódy formátování HTML. Tyto kódy, nazývané tagy, říkají prohlížeči, jak má zobrazit jednotlivé stránky. Pouze text, který se zobrazí v tématu nebo webové stránce, je ve skutečnosti v souboru HTM. Jakákoli grafika, zvuky, animované obrázky nebo jiné prvky, které se objeví, jsou samostatné soubory, na které odkazuje váš soubor HTML. Prohlížeč zkopíruje nebo stáhne grafiku, zvuky nebo jiné prvky, když vidí značky, které mu to říkají.

### Obsah (TOC)
Soubor obsahu nápovědy (.hhc) je soubor HTML, který obsahuje názvy témat vašeho obsahu. Když uživatel otevře obsah v kompilovaném souboru nápovědy (nebo na webové stránce) a klepne na název tématu, otevře se soubor HTML přidružený k tomuto názvu.

### Indexový soubor
Soubor indexu (.hhk) je soubor HTML, který obsahuje položky indexu (klíčová slova) pro váš index. Když uživatel otevře index v kompilovaném souboru nápovědy nebo na webové stránce a klepne na klíčové slovo, otevře se soubor HTML přidružený ke klíčovému slovu.

## Komponenty nápovědy HTML

Nápověda HTML se skládá z několika součástí. Patří mezi ně následující:

* `HTML Help Workshop`: nástroj pro tvorbu nápovědy se snadno použitelným grafickým rozhraním pro vytváření souborů projektu, souborů témat HTML, souborů obsahu, souborů indexů a všeho ostatního, co potřebujete k sestavení systému online nápovědy nebo webové stránky .
* „Ovládací prvek ActiveX nápovědy HTML“: malý modulární program používaný k vložení navigace nápovědy a funkcí sekundárního okna do souboru HTML.
* `Prohlížeč nápovědy HTML`: plně funkční a přizpůsobitelné okno se třemi panely, ve kterém se mohou zobrazovat témata online nápovědy.
* `Microsoft HTML Help Image Editor`: online grafický nástroj pro vytváření snímků obrazovky; a pro konverzi, úpravu a prohlížení obrazových souborů.
* „Java Applet nápovědy HTML“: malý program založený na Javě, který lze použít místo ovládacího prvku ActiveX k vložení navigace nápovědy do souboru HTML.
* `Spustitelný program nápovědy HTML`: program, který zobrazí a spustí nápovědu po klepnutí na kompilovaný soubor nápovědy.
* `Překladač nápovědy HTML`: program, který kompiluje projekt, obsah, rejstřík, téma a další soubory do zkompilovaného souboru nápovědy.
* `The HTML Help Authoring Guide`: online příručka navržená tak, aby pomohla autorům při používání nápovědy HTML k návrhu systému nápovědy. Příručka také obsahuje kompletní referenci HTML nápovědy pro vývojáře a referenci HTML tagů pro autory.

## Reference

* [Nápověda Microsoft HTML](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

