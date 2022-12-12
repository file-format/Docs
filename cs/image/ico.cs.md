{
  "date" : "2019-10-11",
  "keywords" :[ "soubor ico", "formát souboru ico", "co je soubor ico", "soubor", "příklad ico", "přípona souboru ico", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Formát souboru obrázku",
  "description":"Další informace o formátu souborů ICO a rozhraních API, která mohou vytvářet a otevírat soubory ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ICO?

Soubory s příponou ICO jsou typy souborů obrázků používané jako ikona pro znázornění aplikace v [Microsoft Windows] (https://www.microsoft.com/en-us/windows). Ty se dodávají v různých velikostech, podpoře barev a rozlišení, aby vyhovovaly požadavkům displeje. Dalším podobným formátem souboru obrázku v systému Microsoft Windows je [CUR](/cs/image/cur/) pro znázornění kurzoru a definuje aktivní bod v záhlaví obrázku. V systému MacOS slouží formáty souborů ICNS stejnému účelu jako soubory ICO. Několik online webových stránek a aplikací poskytuje funkci vytváření takových souborů a převod jiných formátů obrázků, jako je [BMP](/cs/image/bmp/), [PNG](/cs/image/png/) atd., na formát souboru ikon. Oficiální internetový typ média registrovaný IANA pro soubory ICO je image/vnd.microsoft.icon.

## Stručná historie ##

Ikony byly představeny s uvedením Microsoft Windows 1.0. Ty měly rozměry 32x32 a byly jednobarevné. S příchodem win32 byla zavedena podpora pro obrázky ikon ve skutečných barvách s rozměry až 256 x 256 pixelů. Windows XP byl první, který poskytl podporu pro obrázky ikon v 32bitových barvách, což umožnilo přidat k ikoně poloprůhledné oblasti, jako jsou stíny, vyhlazování a efekty připomínající sklo. Společnost Microsoft doporučila pouze velikosti ikon do 48 × 48 pixelů pro systém Windows XP. Systém Windows Vista přidal do Průzkumníka Windows zobrazení ikon 256 × 256 pixelů a také podporu pro komprimovaný formát [PNG] (/cs/image/png/). Pokud uživatelé používají vyšší rozlišení a režimy s vysokým DPI, doporučují se větší formáty ikon (například 256×256).

## Formát souboru ICO ##

Jeden soubor ICO se skládá z jednoho nebo více malých obrázků různých velikostí a barevných hloubek. Přítomnost obrázků různých velikostí je pro vhodné škálování při různých rozlišeních obrazovky. Všechny hodnoty v souborech ICO/CUR jsou uvedeny v [little-endian](https://en.wikipedia.org/wiki/Little-endian) pořadí bajtů.

Soubor ICO se skládá z hlavičky ikony, adresáře ikon,

|Pole|Popis
---|---|
|Záhlaví ikony|Ukládá obecné informace o souboru ICO.
|Adresář[1..n]|Ukládá obecné informace o každém obrázku v souboru.
|Ikona #1|Skutečná "data" pro první obrázek ve starém formátu AND/XOR DIB nebo novějším PNG
|...|
|Ikona #n|Data pro poslední obrázek ikony

### Záhlaví ###

|Offset|Velikost (v bajtech)|Účel
---|---|---|
|0|2|Vyhrazeno. Vždy musí být 0.
|2|2|Určuje typ obrázku: 1 pro obrázek ikony (.ICO), 2 pro obrázek kurzoru (.CUR). Ostatní hodnoty jsou neplatné.
|4|2|Určuje počet obrázků v souboru.

### Adresář ###

Adresář obsažený v souboru ICO, reprezentovaný jako struktura ICONDIR, obsahuje strukturu ICONDIRECTORY pro každý obrázek v souboru. Totéž následuje souvislý blok všech bitmapových dat obrázku. Toto je znázorněno níže.

|Odsazení|Velikost|Popis
---|---|---|
|0 (0)|1|Šířka, při 256 pixelech by měla být 0
|1 (1)|1|Výška, při 256 pixelech by měla být 0
|2 (2)|1|Počet barev, měl by být 0, pokud je více než 256 barev
|3 (3)|1|Vyhrazeno, mělo by být 0
|4 (4)|2|Barevné plochy ve formátu .ICO by měly být 0 nebo 1 nebo aktivní bod X ve formátu .CUR
|6 (6)|2|Bitů na pixel ve formátu .ICO nebo aktivní bod Y ve formátu .CUR
|8 (8)|4|Velikost bitmapových dat v bajtech.
|12 (C)|4|Odsazení v souboru.

## Reference ##

* [ICO – podle Wikipedie](https://en.wikipedia.org/wiki/ICO_(formát_souboru))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

