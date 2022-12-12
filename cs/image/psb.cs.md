{
  "date" : "2019-10-11",
  "keywords" :[ "soubor psb", "formát souboru psb", "co je soubor psb", "soubor", "příklad psb", "přípona souboru psb", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image File Format",
  "description":"Další informace o formátu souborů PSB a rozhraních API, která mohou vytvářet a otevírat soubory PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PSB?
Adobe photoshop ukládá soubory ve dvou formátech. Soubory o velikosti 30 000 x 30 000 pixelů se ukládají s příponou PSD a soubory větší než PSD až do 300 000 x 300 000 pixelů se ukládají s příponou PSB známou jako „Photoshop Big“. Přesněji řečeno, soubory PSB mohou být velké až 4 EB (přes 4,2 miliardy GB) s obrázky, které mají výšku a šířku až 300 000 pixelů. Na druhou stranu PSD mohou mít maximálně 2 GB a rozměry obrazu 30 000 pixelů.

PSB je také známý jako velkoformátová velikost pro photoshop a podporuje všechny funkce photoshopu, jako jsou vrstvy, efekty a filtry. Photoshop dokáže převést soubor PSB na [PSD](/cs/image/psd/), [JPG](/cs/image/jpeg/) , [PNG](/cs/image/png/), [EPS](/cs/page-description-language/eps/), [GIF](/cs/image/gif/) a další formáty. Velký formát dokumentu Photoshopu je dostupný, jakmile je povolena funkce podokna zpracování souborů v dialogovém okně předvoleb Photoshopu.

## Informace o formátu souboru ##

Formát souboru aplikace Photoshop je rozdělen do pěti hlavních částí s mnoha značkami délky pro pohyb mezi sekcemi.

| Formát souboru
---|
|Záhlaví souboru
| Data barevného režimu
| Zdroje obrázků
| Informace o vrstvě a masce
|(((
Obrazová data
)))

### Záhlaví souboru ###

Hlavička souboru má pevnou délku 26 bajtů a obsahuje základní vlastnosti obrázku.

BYTE podpis [4] – rovná se '8BPS'.

Verze WORD [2] – Číslo verze, PSD # 1, PSB # 2.

BYTE Reserved [6] – Rezervováno a vždy nula.

Kanály WORD [2] – Počet barevných kanálů v obrazu včetně alfa kanálů. Jeho hodnota se pohybuje od 1 do 56.

LONG Rows [4] – Výška obrázku v pixelech, PSD 1-30 000, PSB 1-300 000.

LONG Columns [4] – Šířka obrazu v pixelech, PSD 1-30 000, PSB 1-300 000.

Hloubka slova [2] – Počet bitů na kanál. Podporované hodnoty jsou 1,8,16 a 32.

Režim WORD [2] – Barevný režim souboru.

#### Popis režimu ####


|Režim|Popis
---|---|
|0|Bitmapa (jednobarevná)
|1|Stupně šedi
|2|Indexováno
|3|RGB
|4|CMYK
|7|Multikanál
|8|Duotón (půltón)
|9|Laboratoř

### Data barevného režimu ###

Po sekci záhlaví souboru následuje sekce dat barevného režimu. Blok začíná číslem LONG, které udává délku bloku v bajtech. Struktura dat barevného režimu je následující:

4 bajty – délka následujících barevných dat.

Proměnná – Data barev

Pokud hodnota pole režimu v sekci záhlaví není indexovaná barva nebo duotón, délka bloku bude 0 a za polem délky nebudou žádná data.

U indexovaných barevných obrázků bude délka 768 bajtů, které budou obsahovat 256 barevnou paletu. U duotone budou data obsahovat parametry obrazovky a další související informace.

### Zdroje obrázků ###

Po části dat barevného režimu je třetím blokem část zdrojů obrazu. První čtyři bajty jsou LONG číslo určující délku bloku následované řadou zdrojových bloků. Struktura bloku zdroje obrázku je následující:

BYTE typ [4] – podpis '8BIM'

WORD ID [2] – ID zdroje obrázku. Existuje seznam ID zdrojů, který lze vidět z odkazu na reference.

Název BYTE [Proměnná] – Název: Řetězec Pascal se sudou délkou. ******

LONG Size [4] – Skutečná velikost dat zdrojů, která následuje.

BYTE Data [Proměnná} – Data zdrojů. Je polstrovaná, aby byla rovnoměrná.

Některé formáty zdrojů jsou stručně vysvětleny níže:

**Formát zdroje mřížky a vodítek:** Informace o mřížce a vodítkách jsou uloženy v bloku zdrojů. Tyto zdrojové bloky obsahují 16bajtovou mřížku a vodicí hlavičku následované 5 bajtovými bloky vodicích informací.

**Formát zdroje miniatur:** Informace o náhledu jsou uloženy v bloku zdroje obrázku pro zobrazení náhledu, který se skládá z 28bajtového záhlaví a miniatury JFIF v RGB.

**Formát zdroje vzorníků barev:** Informace o vzorcích barev jsou uloženy v bloku zdroje obrazu s 8bajtovým záhlavím, za nímž následuje blok s informacemi o vzorníku barev s proměnnou délkou.

### Informace o vrstvě a masce ###

Čtvrtý blok je informační blok vrstvy a masky a obsahuje informace o vrstvách a maskách. Nejprve se uloží informace o vrstvě a poté informace o masce.

**Informace o vrstvě:** Informace o vrstvě začínají hodnotou LONG, která ukazuje délku informací o vrstvě. Poté následuje počet hodnot WORD, který ukazuje počet záznamů vrstvy, které mají následovat.

[8] – délka vrstev

[2] – Počet vrstev

[Proměnná] – Informace o každé vrstvě.

[Variable] – Obrazová data kanálu.** **

**Informace o masce:** Struktura masky má následující formát:


|Struktura dat|Název pole| Popis
---|---|---|
|SLOVO| Překryvný barevný prostor| (Není zdokumentováno)
|BYTE[8]| Barevné komponenty| 4x2 bajtové barevné složky
|SLOVO| Neprůhlednost| 0#průhledné, 1#neprůhledné
|BYTE| Druh| 0#invertováno, 1#chráněno, 128#použít uloženou hodnotu
|BYTE| vycpávka| nastavit na nulu

### Data obrázku ###

Poslední část obsahuje data obrazových pixelů. Obrazová data jsou uložena jako série sekvencí v rovinách, tj. nejprve všechna červená data, poté všechna zelená data atd. SLOVO na začátku každého řádku ukazuje velikost v bajtech vztahující se ke každému skenovanému řádku.

[2] – Kompresní metoda:

[Variable] – Obrazová data v rovinném pořadí, tj. RRRR, GGGG, BBBB atd.

Kompresní metody:

0 – Raw Obrazová data

1 – RLE Compressed

2 – Zip bez předpovědi

3 – Zip s predikcí

## reference ##

* [Formát souboru PSB – od společnosti Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

