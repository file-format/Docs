{
  "date" : "2019-10-11",
  "keywords" :[ "soubor jp2", "formát souboru jp2", "co je soubor jp2", "soubor", "příklad jp2", "přípona souboru jp2", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Formát souboru obrázku",
  "description":"Další informace o formátu souboru JP2 a rozhraních API, která mohou vytvářet a otevírat soubory JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Co je soubor JP2? ##

JPEG 2000 (**JP2**) je systém kódování obrazu a nejmodernější standard komprese obrazu. Využívá vlnkovou technologii pro kódování bezeztrátového obsahu v jakékoli kvalitě najednou. Navíc, bez jakékoli podstatné penalizace v účinnosti kódování, JPEG 2000 má schopnost přistupovat ke stejnému obsahu a účinně jej dekódovat do řady dalších rozlišení a kvalit. Toky kódu v JPEG 2000 jsou výrazně škálovatelné a mají oblasti zájmu, které poskytují možnost prostorového náhodného přístupu.

JPEG 2000 vyniká jako jeden z nejvíce škálovatelných standardů. Různé části obrazu lze uložit pomocí různých kvalit. Pozoruhodné eskalace výkonu lze dosáhnout uspořádáním toku kódu různými způsoby. Nicméně JP2 vyžaduje složité a výpočetně náročné kodéry/dekodéry jako výsledek této flexibility. Ve srovnání s JPEG vytváří JPEG 2000 pouze vyzváněcí artefakty, které vytvářejí kroužky poblíž okraje obrazu a mohou být rozmazané, zatímco JPEG používá 8×8 bloků vizuálních artefaktů, které mohou být jak vyzváněcí, tak blokující artefakty. Obsahuje až 16 384 různých komponent s rozměry v terapixelech a přesností, která může dosahovat až 38 bitů/vzorek.

## Dějiny ##

V roce 2000 navrhl výbor Joint Photographic Experts Group JP2 s cílem vylepšit vlastní JPEG standard založený na diskrétní kosinové transformaci pomocí této nové metody založené na vlnkách. Komise JPEG měla za cíl poskytovat své základní metody bez licenčních poplatků. V konkurenci 20 společností zvítězila licence JP2 o vlásek. JPEG 2000 byl deklarován jako standard ISO, ačkoli většina webových prohlížečů není připravena poskytnout JPEG 2000 od roku 2017.

## Části obrazového kódovacího systému JPEG 2000 ##

Následují hlavní části, které tvoří kompletní sadu standardů pro JPEG 2000.


|Část|Název|Popis|Číslo
---|---|---|---|
|Část 1|Základní kódovací systém| Definuje syntaxi toku kódu. Různé fáze zapojené do dekódování obrázků JPEG 2000. Vysvětluje základní formát souboru JP2, metadata a práva IP, která mají být poskytnuta.|ISO/IEC 15444-1
|Část 2|Rozšíření|Definuje rozšíření pro tok kódu ve formátu souboru a umožňuje ukázky ukázek HDR, specifikace barevného prostoru, oříznutí, geometrické transformace; různé animace, metadata a tok více kódů.|ISO/IEC 15444-2
|Část 3|Motion JPEG 2000 (MJ2 nebo MJP2)|Představit formát souboru pro sekvence pohybu, kódování obrázků v nezávislém toku kódu.|ISO/IEC 15444-3
|Část 4|Shoda|Uvádí testovací techniky pro kódování a dekódování a kontroluje soubory pro proudy holého kódu i soubory JP2.|ISO/IEC 15444-4
|Část 5|Referenční software|Skládá se ze dvou balíčků zdrojového kódu (Java, C), které implementují systém kódování Core a jsou dostupné pod licencemi open source.|ISO/IEC 15444-5
|Část 6|Formát souboru složeného obrázku|Definuje formát souboru JPM a umožňuje zobrazení vícestránkových dokumentů pro aplikace podobné faxu. Podporuje použití JBIG2 a JPEG.|ISO/IEC 15444-6
|Část 8|JPEG 2000 Secured (JPSEC)|Zajišťuje bezpečnost transakcí, obsahu a technologií a umožňuje zabezpečené toky JPEG 2000 bitů.|ISO/IEC 15444-8
|Část 9|JPIP|Definuje nástroje v síťovém prostředí pro přístup k metadatům a snímkům a uvádí Interaktivní a efektivní protokoly|ISO/IEC 15444-9
|Část 10|JP3D|Volumetrické rozšíření části 1 a zavádí rozměr Z. Rozšiřuje koncept dlaždic, kódových bloků, okrsků a funkcí usnadnění 3D oblasti zájmu.|ISO/IEC 15444-10
|Část 11|JPWL|Zabývá se dobře organizovaným přenosem přes bezdrátovou síť náchylnou k chybám. Toto rozšíření je kompatibilní s dekodéry|ISO/IEC 15444-11
|Část 13|Kodér základní úrovně|Definuje implementaci kodéru základní úrovně systému kódování jádra.|ISO/IEC 15444-13
|Část 14|JPXML|Reprezentace v XML a vysvětluje segmenty značek a metody pro přístup k interním datům snímků.|ISO/IEC 15444-14
|Část 15|HTJ2K (Ve vývoji)|Určuje alternativní algoritmus blokového kódování. Algoritmus nabízí desetinásobně zvýšenou propustnost a bezztrátové kódování/dekódování.|

## Formát souboru JP2 ##

JPEG 2000 definuje formát souboru i tok kódu stejným způsobem jako JPEG-1. Přestože jsou ukázky obrázků výhradně popsány v JPEG 2000, JPEG-1 obsahuje další přidané informace o barevném prostoru a rozlišení, které jsou nezbytné pro kódování obrázku. Pokud je obrázek uložen jako soubor JPEG 2000, použije se jako přípona **.jp2**. Tento formát souboru je dále vylepšován rozšířením JPEG 2000 part-2, které definuje animační mechanismy a konfiguraci mnoha proudů kódu do jednoho obrázku. Přípona **.jpx** se používá při ukládání obrázků pomocí tohoto rozšířeného formátu souboru. Vzhledem k tomu, že data kódového toku nejsou považována za primárně uložená v souborech, není pro tento účel definována žádná standardní přípona. I když pro účely testování často dostává příponu **.jpc** nebo **.j2k**. Na rozdíl od JPEG-1 volí JPEG 2000 jiný způsob kódování metadat ve formátu XML. Standard 12234-1.4 (od komise ISO TC42) se používá jako reference mezi tagy Exif a komponentami XML. JPEG 2000 může obsahovat standard ISO, XMP uvnitř.

### Kousky ###
Soubory JPEG 2000 se skládají z po sobě jdoucích bloků. Každý chunk má 8bajtové záhlaví: 4bajtová velikost chunku (big-endian, vysoký byte první) a 4bajtový typ chunk – jeden z předdefinovaných podpisů: „jP“ nebo „jP2“.

Druhý blok musí být typu "ftyp" a má podtyp na offsetu 8. JPEG 2000 definovaný podtypem, který musí být jednou z hodnot: "jp2 "(typ souboru \*.JP2), "jp20" (soubor typ \*.JPA), "jpm" (typ souboru \*.JPM), "jpx" (typ souboru \*.JPX).

Opakujeme bloky, dokud není detekován neznámý typ, skládáme soubor obrázku/videa JPEG 2000.

### Transformace barev ###

Zpočátku je nutná transformace obrázků z barevného prostoru RGB do jiného barevného prostoru. Pro tento účel existují dva způsoby: Nevratná transformace barev (ICT) a Reverzibilní transformace barev (RCT). První používá barevný prostor YC,,B,,C,,R,, a musí být implementován v pevné/plovoucí desetinné čárce, zatímco později upravený barevný prostor YUV a je svou povahou reverzibilní.// //Není omezeno na model RGB, JPEG Jazyk 2000 používá transformaci více komponent.

### Obklady ###

Po dokončení transformace barev se obraz převede na obdélníkové oblasti zvané dlaždice, které lze transformovat a kódovat samostatně. Velikost všech dlaždic bude stejná nebo lze celý obrázek považovat za jednu dlaždici. Decoder využívá výhody dlaždic a spotřebovává méně paměti nebo může některé dlaždice částečně zakódovat. Tato technika má však nevýhodu v degradaci kvality obrazu.

### Waveletová transformace ###

Obraz po dlaždicování je vlnkově transformován, což může být buď nevratné nebo reverzibilní, a implementováno pomocí schématu konvoluce nebo zvedání.

### Kompresní poměr ###

V závislosti na fyzikálních vlastnostech obrázku je dosaženo kompresního zisku 20 % Predikce prostorové redundance JPEG 2000 hraje zásadní roli v procesu komprese a obrázky s vysokým rozlišením mají tendenci získat největší výhodu.

## Aplikace obsluhované standardním ##

* Nahrávání, úpravy a ukládání snímků HD videa
* Lékařské snímky a biometrie
* satelitní snímky, dálkový průzkum Země a detekce pohybu
* Komunikace klient/server, síťová distribuce a úložiště.
* Digitální kino, příspěvek živého vysílání HDTV, digitalizované audio-vizuální věci

## Reference ##

* [Přehled JPEG 2000] (https://jpeg.org/jpeg2000)
* [Systém kódování obrázků JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

