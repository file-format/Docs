{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PS",
  "description":"Další informace o formátu souborů PS a rozhraních API, která mohou vytvářet a otevírat soubory PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor .PS? ##

PostScript (PS) je univerzální jazyk pro popis stránek používaný v oblasti stolního a elektronického publikování. Hlavním zaměřením PostScriptu (PS) je usnadnit dvourozměrný grafický design. Většina jazyků vyžaduje samostatnou fázi kompilace před spuštěním kódu, zatímco formát Post Script (PS) podporuje přímou interpretaci za běhu. Jeho raná verze definuje grafické tvary, různé vzhledy textu a modelované obrázky na tištěných nebo zobrazených stránkách podle pravidel zobrazovacího modelu Adobe. Program PS je schopen vzájemně komunikovat popis dokumentu mezi systémem kompozice a tisku, přičemž zařízení udržuje nezávislé a na vysoké úrovni. Navíc je tento program také schopen řídit vzhled textu a grafiky na displeji.

Popis PostScriptové stránky je možné vykreslit, zobrazit na tiskárně a jiném výstupním zařízení pomocí PostScriptového interpretu zařízení. Protože příkazy k tisku znaků, grafických tvarů a obrázků jsou vykonávány interpretem, pro toto konkrétní zařízení se popis vysoké úrovně PostScript převede do formátu rastrových dat nízké úrovně. Obecně platí, že různé aplikace, jako jsou ilustrátoři, systémy pro tvorbu dokumentů a počítačově podporovaný design (CAD), jsou automatizovány pro generování popisů stránek PostScript. Obecně musí programátoři psát PostScriptové programy v době vytváření nových aplikací. Programátor však může využít schopností jazyka PostScript, které nejsou dostupné v žádné aplikaci, napsáním programu PS pro tuto zvláštní situaci.

## Stručná historie ##

Koncept jazyka PostScript poprvé představil John Warnock. V roce 1966 pracoval na projektu New York Harbor. Snažil se vyvinout interpret pro velkou trojrozměrnou grafiku pro databázi tohoto projektu. Pro zpracování této grafiky navrhl John Warnock jazyk Design System. Mezitím Xerox PARC hledal standardní způsob definování obrázků stránek pro svou první laserovou tiskárnu. Ačkoli Bob Sproull a William Newman v letech 1975-76 vyvinuli formát Press (formát dat) pro řízení laserových tiskáren, pro větší flexibilitu byl zapotřebí jazyk. V roce 1978 se Warnock připojil k Martinu Newellovi v Xerox PARC a přepsal interpretační jazyk JaM, který se později rozrostl a rozšířil do jazyka Interpress. Warnock založil Adobe Systems v prosinci 1982 s Chuckem Geschkem, Dougem Brotzem, Edem Taftem a Billem Paxtonem. Začali pracovat na jednodušším jazyce zvaném PostScript podobný Interpressu, který byl komerčně uveden v roce 1984. Navštívil je Steve Jobs z Applu a poradil jim, aby upravili PostScript pro ovládání laserových tiskáren.

V březnu 1985 byla první tiskárnou se zabudovaným PostScriptovým interpretem Apple LaserWriter, který způsobil revoluci v DTP (DTP). Technická spolehlivost a široká dostupnost učinily PostScript jazykem volby pro stolní počítače a elektronické publikování. Během roku 1990 byl nezbytnou součástí laserových tiskáren interpret pro jazyk PostScript.

## Hlavní rysy ##

Schopnosti jazyka PostScript pro práci s interaktivní grafikou a popisem stránek mají následující vlastnosti:

**Tvary:** Libovolné povahy, mohou se skládat z přímých čar, křivek, čtverců a krychlových křivek, které mohou být samoprojížděné i rozpojené (v úsecích a otvorech).

**Operátoři malování:** umožňují obrys tvaru libovolné tloušťky, barvy, výplně nebo umožňují nakreslení tvaru jako výstřižek, aby bylo možné oříznout jakoukoli jinou grafiku.

**Barvy:** mají rozmanitost, jako jsou stupně šedi, RGB, CMYK a CIE. Speciální druhy barev jsou modelovány jako různé prvky: přímé barvy, mapování barev, dokonce i stínování a opakující se vzory.

**Text:** plně integrovaný s grafikou. Adobe imaging model navíc umožňuje, aby textové znaky byly zobrazeny jako grafické tvary, které může ovládat jakýkoli normální grafický operátor.

**Ukázkové obrázky**: extrahované z originálních zdrojů (naskenované fotografie) nebo mohou být vyrobeny synteticky. Jazyk PostScript nabízí různé prostředky pro regeneraci obrázků v jakémkoli rozlišení a podle různých barevných modelů na výstupním zařízení.

Univerzální programovací jazyk může využít grafických schopností jazyka PostScript vložením Ps do svého rámce. Primitivní datové typy, jako jsou čísla, znaky, pole a řetězce; řídicí primitiva, jako jsou smyčky, procedury a podmínky; a některé nekonvenční funkce, jako jsou slovníky, jsou specifikovány v jazyce. Tyto funkce umožňují programátorům psát příkazy pro vyvolání operací vyšší úrovně. Tyto operace na vysoké úrovni splňují potřeby komplexní aplikace. Taková praxe je kompaktnější a efektivnější než použití pevného souboru základních operací.

Programy napsané v PostScriptu lze vytvářet, komunikovat a interpretovat ve formě zdrojového textu ASCII. Celý jazyk lze definovat ve formě tisknutelných znaků a mezer. Tato reprezentace podporuje programátory k snadnému vytváření, manipulaci a porozumění jazyku. Navíc ukládání a přenos souborů mezi různými počítači a operačními systémy je stále pohodlný díky nezávislosti na stroji.

Binární zakódované formy jazyka jsou možné, když je programu zaručena plně transparentní komunikační cesta k překladači PostScript. Adobe doporučuje striktní soudržnost s ASCII reprezentací PS programů pro výměnu dokumentů nebo archivaci.

## Verze ##

PS(.ps) je přípona souboru pro PostScriptový dokument. UK National Archives kategorizuje pět chronologických verzí PostScriptového souboru, definovaných ve verzi DSC: verze 1.0, 2.0, 2.1, 3.0, 3.1. Každá verze definuje důležité strukturující komentáře. Encapsulated PostScript File (EPS) je speciální podtyp souboru PostScript, který používá jazyk k určení obdélníkové grafiky. Referenční příručka jazyka PostScript popisuje EPS takto: "Soubor EPS (Encapsulated PostScript) je PostScriptový program popisující maximálně jednu stránku ve formě, kterou lze importovat jinými aplikacemi a vložit ji do obsahujícího dokumentu." Soubor dokumentu PostScript v něm může zapouzdřit soubor EPS. Další použití PostScriptu je zmíněno jako Display PostScript (DPS). DPS generuje grafiku na obrazovce prostřednictvím grafického enginu, který využívá PostScriptový zobrazovací model a jazyk.

## Reference ##

* [Rodina formátů PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

