{
  "date" : "2019-10-11",
  "keywords" :[ "soubor png", "formát souboru png", "co je soubor png", "soubor", "příklad png", "přípona souboru png", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PNG - soubor rastrového obrázku",
  "description":"Další informace o formátu souboru PNG a rozhraních API, která mohou vytvářet a otevírat soubory PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PNG?

Soubor **PNG** (Portable Network Graphics) je formát rastrového obrázku, který používá bezztrátovou kompresi. Tento formát souboru byl vytvořen jako náhrada formátu Graphics Interchange Format ([GIF](/cs/image/gif/)) a nemá žádná omezení autorských práv. Formát souboru PNG však animace nepodporuje. Formát souboru PNG podporuje bezeztrátovou kompresi obrázků, díky čemuž je mezi uživateli oblíbený. S postupem času se PNG vyvinul jako jeden z široce používaných formátů souborů obrázků.

## Stručná historie formátu souboru PNG

Hlavním důvodem pro vytvoření formátu souboru PNG byl patentovaný kompresní algoritmus Lempel-Ziv-Welch používaný ve formátu GIF. To spolu s dalšími omezeními GIF vyvolalo potřebu nahradit formát souboru [**GIF**](/cs/image/gif/). První návrh a název pro formát souboru PNG přišel v lednu 1995. Klíčové události týkající se formátů souborů PNG jsou uvedeny níže:

* Říjen 1996: Specifikace PNG verze 1.0 byly vydány a později se objevily jako [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Totéž se stalo doporučením W3C v říjnu 1996.
Prosinec 1998: Byla vydána verze 1.1 s některými malými změnami a přidáním tří nových kusů.
* Srpen 1999: Byla vydána verze 1.2 s přidáním jednoho kousku navíc.
Listopad 2003: PNG se stal mezinárodním standardem (ISO/IEC 15948:2003). Tato verze PNG se od verze 1.2 liší jen mírně a nepřidává žádné nové kousky.
* Březen 2004: ISO/IEC 15948:2004

## Funkční srovnání GIF a PNG

Formát souboru PNG byl navržen tak, aby byl jednoduchý a přenosný, právně nezatížený, zaměnitelný, flexibilní a robustní. V následující tabulce jsou uvedeny funkce GIF, které jsou kromě nových funkcí zděděny formátem souboru PNG.

|Funkce|GIF|PNG|
---|---|---|
|Indexové barevné obrázky až 256 barev|Ano|Ano|
|Podpora streamování|Ano|Ano|
|Transparentnost|Ano|Ano|
|Doplňkové informace|Ano|Ano|
|Nezávislost na hardwaru a platformě|Ano|Ano|
|Efektivní|Ano|Ano|
|Truecolor obrázky až 48 bitů na pixel|Ne|Ano|
|Obrázky ve stupních šedi až 16 bitů na pixel|Ne|Ano|
|Úplný alfa kanál (obecné masky průhlednosti)|Ne|Ano|
|Informace o gama obrazu|Ne|Ano|
|Spolehlivost|Ne|Ano|
|Rychlejší úvodní prezentace|Ne|Ano|

## Struktura souboru PNG

Téměř všechny operační systémy podporují otevírání souborů PNG. Například prohlížeč Microsoft Windows má schopnost otevírat soubory PNG, protože OS má standardně podporu dostupnou jako součást instalace. Soubor PNG se skládá z `podpisu` PNG následovaného řadou //dílů//.

### Záhlaví souboru PNG

Prvních osm bajtů souboru PNG vždy obsahuje následující (desítkové) hodnoty:

{{{137 80 78 71 13 10 26 10 }}}

Tento podpis označuje, že zbytek souboru obsahuje jeden obrázek PNG, skládající se z řady částí začínajících částí IHDR a končící částí IEND.

### Kousky ###

Každý kus se skládá ze čtyř částí:

**Length:** 4bajtové celé číslo bez znaménka udávající počet bajtů v datovém poli bloku. Délka počítá pouze datové pole, ne sama sebe, kód typu bloku nebo CRC. Nula je platná délka. Ačkoli by kodéry a dekodéry měly délku považovat za bez znaménka, její hodnota nesmí přesáhnout 231 bajtů.

**Typ bloku:** 4bajtový kód typu bloku. Pro usnadnění popisu a zkoumání souborů PNG jsou typové kódy omezeny na to, že se skládají z velkých a malých písmen ASCII (AZ a az, nebo 65-90 a 97-122 desítkové). Kodéry a dekodéry však musí s kódy zacházet jako s pevnými binárními hodnotami, nikoli se znakovými řetězci. Například by nebylo správné reprezentovat typový kód IDAT ekvivalenty EBCDIC těchto písmen. Další konvence pojmenování pro typy bloků jsou popsány v další části.

**Chunk Data:** Datové bajty odpovídající typu bloku, pokud existují. Toto pole může mít nulovou délku.

**CRC:** 4bajtový CRC (Cyclic Redundancy Check) vypočítaný z předchozích bajtů v bloku, včetně kódu typu bloku a datových polí bloku, ale bez pole délky. CRC je vždy přítomen, dokonce i pro bloky neobsahující žádná data.

Délka dat bloku může být libovolný počet bajtů až do maxima; implementátoři proto nemohou předpokládat, že bloky jsou zarovnány na hranicích větších než bajty.

Bloky se mohou objevit v libovolném pořadí, s výhradou omezení kladených na jednotlivé typy bloků. (Jedním významným omezením je, že IHDR se musí objevit jako první a IEND jako poslední; blok IEND tedy slouží jako značka konce souboru.) Může se objevit více bloků stejného typu, ale pouze pokud je to pro tento typ výslovně povoleno.

#### Typy bloků

Typy bloků jsou rozděleny do kategorií **Kritické** a **Doplňkové** na základě 4bajtové hodnoty ASCII, která je přiřazena typu bloku. Všechny implementace musí porozumět a úspěšně vykreslit standardní kritické části. Platný obrázek PNG musí obsahovat blok IHDR, jeden nebo více bloků IDAT a blok IEND.

### Komprese

Metoda komprese PNG 0 (jediná metoda komprese v současnosti definovaná pro PNG) specifikuje kompresi deflate/inflate s posuvným oknem o velikosti nejvýše 32768 bajtů. Deflate komprese je derivát LZ77 používaný v programech zip, gzip, pkzip a souvisejících programech. Byl proveden rozsáhlý výzkum podporující jeho status bez patentů. Komprimovaná data v datovém toku zlib jsou uložena jako série bloků, z nichž každý může představovat nezpracovaná (nekomprimovaná) data, data komprimovaná LZ77 kódovaná pevnými Huffmanovými kódy nebo komprimovaná data LZ77 kódovaná vlastními Huffmanovými kódy. Bit markeru v posledním bloku jej identifikuje jako poslední blok, což umožňuje dekodéru rozpoznat konec komprimovaného datového toku.

#### Předkompresní filtrování

K přípravě obrazových dat na optimální kompresi se používají předkompresní filtry. Metoda filtrování PNG definuje pět základních typů filtrů takto:

|Typ filtru|Název|Předpokládaná hodnota|
---|---|---|
|0|Žádný|Skenovací řádek je přenášen nezměněný|
|1|Sub|Přenese rozdíl mezi každým bajtem a hodnotou odpovídajícího bajtu předchozího pixelu.|
|2|Nahoru|Filtr Up() je stejný jako filtr Sub() s tím rozdílem, že jako prediktor se používá pixel bezprostředně nad aktuálním pixelem, nikoli jen vlevo od něj.|
|3|Průměr|Filtr Average() používá průměr dvou sousedních pixelů (vlevo a nahoře) k předpovědi hodnoty pixelu.|
|4|Paeth|Filtr Paeth() vypočítá jednoduchou lineární funkci tří sousedních pixelů (vlevo, nahoře, vlevo nahoře) a poté vybere jako prediktor sousední pixel, který je nejblíže vypočtené hodnotě.|

Algoritmy filtrování se aplikují na „bajty“, nikoli na pixely, bez ohledu na bitovou hloubku nebo barevný typ obrázku. Filtrační algoritmy pracují na bajtové sekvenci tvořené skenovacím řádkem. Pokud obrázek obsahuje alfa kanál, jsou alfa data filtrována stejným způsobem jako obrazová data.

Když je obraz prokládaný, každý průchod prokládaného vzoru je pro účely filtrování považován za nezávislý obraz. Filtry pracují na bajtových sekvencích tvořených pixely skutečně přenášenými během průchodu a „předchozí skenovací řádek“ je ten, který byl předtím přenesen ve stejném průchodu, nikoli ten, který sousedí v úplném obrazu. Všimněte si, že dílčí obraz přenášený jedním průchodem je vždy obdélníkový, ale má menší šířku a/nebo výšku než celý obraz. Když je tento dílčí obrázek prázdný, filtrování se nepoužije.

## Reference ##

* [PNG – domovská stránka](http://www.libpng.org/pub/png/)

