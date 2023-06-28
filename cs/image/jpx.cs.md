{
  "date" : "2021-02-10",
  "keywords" :[ "soubor jpx", "formát souboru jpx", "co je soubor jpx", "soubor", "příklad jpx", "přípona souboru jpx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Formát souboru obrázku",
  "description":"Další informace o formátu souborů JPX a rozhraních API, která mohou vytvářet a otevírat soubory JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Co je soubor JPX? ##

Soubor s příponou .jpx je rozšířením formátu souboru JPEG 2000. Využívá primárně kompresi JPEG 2000 a také poskytuje pokročilé funkce, jako je více vrstev pro obraz, různé barevné prostory, neprůhlednost a fragmentované proudy kódu. JPX také umožňuje další komprese, jako je JBIG, CCITT Group3, CCITT Group4 atd. kromě komprese JPEG 2000. Formát souboru JPX byl schválen jako standard [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), ale nemohl získat vřelý příjem kvůli rozsáhlému používání [JPEG ]formát souboru (/cs/image/jpeg/). Mezi aplikace, které mohou otevírat soubory JPX, patří Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 a CorelDraw Graphics Suite 2020.

## Stručná historie

V roce 2000 navrhl výbor Joint Photographic Experts Group JP2 s cílem vylepšit vlastní JPEG standard založený na diskrétní kosinové transformaci pomocí této nové metody založené na vlnkách. Komise JPEG měla za cíl poskytovat své základní metody bez licenčních poplatků. V konkurenci 20 společností zvítězila licence JP2 o vlásek. JPEG 2000 byl deklarován jako standard ISO, ačkoli většina webových prohlížečů není připravena poskytnout JPEG 2000 od roku 2017. V roce 2004 byl formát ISO/IEC 15444-2 veřejně přijat jako rozšíření formátu souboru JP2.

## Formát souboru JPX

Formát souboru JPX byl formulován tak, aby splňoval požadavky aplikací, které potřebovaly datové struktury nad rámec funkcí definovaných formátem souboru [JP2](/cs/image/jp2/). Soubor JP2 s nekompatibilními příponami by mohl vést ke zmatku na trhu, kde někteří čtenáři mohou interpretovat některé soubory JP2, ale ne jiné. JPX je odpovědí, jak se takovým problémům v aplikacích vyhnout.

### Identifikace souboru

Soubory JPX jsou uloženy jako [JPF](/cs/image/jpf/), když jsou uloženy v tradičním počítačovém souborovém systému. To je důvod, proč je termín JPX nejméně běžně používaný ve srovnání s JPF. Soubor JPX začíná následujícími bajty:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organizace souborů

Podobně jako u JP2 je soubor JPX sbírkou krabic, které mají binární strukturu s krabicemi uspořádanými v souvislém pořadí. První pole udává začátek souboru s jeho prvním bajtem a poslední bajt posledního pole představuje poslední bajt souboru.
Binární struktura krabice v souboru JPX je identická se strukturou definovanou ve formátu souboru [JP2](/cs/image/jp2/).

### Uložení CodeStream v JPX

Formát souboru JPX umožňuje rozdělení obrazového kódu na fragmenty. To umožňuje upravit jednu dlaždici obrázku a zapsat upravenou dlaždici na konec souboru bez přepisování celého souboru. Původní formát souboru [JP2](/cs/image/jp2/) omezuje uložení celého toku kódu do souvislé části souboru, což může být problematické pro aplikace pro úpravu obrázků, které mohou chtít upravit jednu dlaždici obrázku a dosáhnout výše uvedená podpora formátem souboru JPX. Fragmentace toku obrazových kódů činí formát souboru JPX lepší než formát souboru JP2. Formát souboru JPX navíc umožňuje zkombinovat více kódových proudů a vytvořit vykreslený výsledek. Kódové toky lze kombinovat jako skládání a animaci.

## Reference ##

* [Přehled JPEG 2000](https://jpeg.org/jpeg2000/)

