{
  "date" : "2019-10-11",
  "keywords" :[ "soubor psd", "formát souboru psd", "co je soubor psd", "soubor", "příklad psd", "přípona souboru psd", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop Image File Format",
  "description":"Další informace o formátu souborů PSD a rozhraních API, která mohou vytvářet a otevírat soubory PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PSD?

PSD, Photoshop Document, představuje nativní formát souborů Adobe Photoshop používaný pro návrh a vývoj grafiky. Soubory PSD mohou obsahovat obrazové vrstvy, vrstvy úprav, masky vrstev, anotace, informace o souborech, klíčová slova a další prvky specifické pro Photoshop. Soubory Photoshopu mají výchozí příponu .PSD a mají maximální výšku a šířku 30 000 pixelů a limit délky dva gigabajty.

## Specifikace formátu souboru PSD ##

Data v souboru PSD jsou uložena v pořadí bajtů big endian. To znamená prohození krátkých a dlouhých celých čísel při čtení nebo zápisu na platformě Windows. Formát souboru Photoshopu je rozdělen do pěti hlavních částí. Má mnoho délkových značek, které lze použít k přesunu z jedné sekce do druhé. Značky délky jsou obvykle doplněny bajty, aby se zaokrouhlovaly na nejbližší 2 nebo 4 bajtový interval. Pět hlavních částí je:

* Záhlaví souboru
* Data barevného režimu
* Zdroje obrázků
* Informace o vrstvě a masce
* Obrazová data

Kvůli shodě by měla být data zapsána do všech těchto polí v sekci, protože Photoshop se může pokusit přečíst celou sekci. To také znamená, že při zápisu do souboru se do přeskočených polí zapisují nuly. Pole délky v úsecích oddělených délkou by se mělo použít k rozhodnutí, kdy ukončit čtení. Ve většině případů pole délky udává počet následujících bajtů, nikoli záznamů. Při čtení souboru je třeba mít na paměti následující body.

* Hodnoty ve sloupci "Length" ve všech tabulkách jsou v bajtech.
* Všechny hodnoty definované jako řetězec Unicode se skládají z:
* Pole o délce 4 bajtů představující počet znaků v řetězci (nikoli bajtů).
* Řetězec hodnot Unicode, dva bajty na znak.

### Záhlaví souboru ###

Záhlaví souboru obsahuje základní vlastnosti obrázku.

|Délka|Popis
---|---|
|4|Podpis: vždy se rovná '8BPS' . Nepokoušejte se číst soubor, pokud podpis neodpovídá této hodnotě.
|2|Verze: vždy rovna 1. Nepokoušejte se číst soubor, pokud verze neodpovídá této hodnotě. (~*~*PSB~*~* verze je 2.)
|6|Rezervováno: musí být nula.
|2|Počet kanálů v obraze, včetně všech alfa kanálů. Podporovaný rozsah je 1 až 56.
|4|Výška obrázku v pixelech. Podporovaný rozsah je 1 až 30 000.
|4|Šířka obrázku v pixelech. Podporovaný rozsah je 1 až 30 000.
|2|Hloubka: počet bitů na kanál. Podporované hodnoty jsou 1, 8, 16 a 32.
|2|Barevný režim souboru. Podporované hodnoty jsou: Bitmap # 0; Stupně šedi # 1; Indexováno # 2; RGB # 3; CMYK # 4; vícekanálový # 7; Duotone # 8; Laboratoř číslo 9.

### Sekce dat barevného režimu ###

Sekce dat barevného režimu je strukturována takto:


|Délka|Popis
---|---|
|4|Délka následujících barevných dat
|proměnná|data barev

Data barevného režimu jsou dostupná pouze pro indexovanou barvu a duotón, jak je definováno v poli režimu v části Záhlaví souboru. Pro všechny ostatní režimy je tato sekce reprezentována 4bajtovými nulovanými hodnotami. U indexovaných barevných obrázků je délka 768 a data barev obsahují tabulku barev pro obrázek v neprokládaném pořadí. U dvoubarevných obrázků obsahují data barev specifikaci duplexu (jejíž formát není dokumentován). Jiné aplikace, které čtou soubory Photoshopu, mohou s dvojbarevným obrazem zacházet jako s šedým obrazem a při čtení a zápisu souboru pouze zachovávají obsah dvoubarevných informací.

### Sekce zdrojů obrázků ###

Třetí část souboru obsahuje zdroje obrázků. Začíná polem délky, po kterém následuje řada bloků zdrojů.


|Délka|Popis
---|---|
|4|Délka části zdroje obrázku. Délka může být nulová.
|Proměnná|Prostředky obrázků (bloky zdrojů obrázků)

Zdroje obrázků se používají k ukládání nepixelových dat spojených s obrázky, jako jsou dráhy nástroje pera. Jsou označovány jako zdrojové bloky, protože obsahují data, která byla uložena v prostředku Macintosh v dřívějších verzích Photoshopu. Základní struktura bloků prostředků obrazu je uvedena níže:


|Délka|Popis
---|---|
|4|Podpis: '8BIM'
|2|Jedinečný identifikátor zdroje. ID prostředků obrázků obsahuje seznam ID prostředků používaných aplikací Photoshop.
|Proměnná|Název: Pascalův řetězec, doplněný tak, aby byla velikost stejná (null název se skládá ze dvou bajtů po 0)
|4|Skutečná velikost dat zdrojů, která následuje
|Proměnná|Data zdrojů popsaná v částech o jednotlivých typech zdrojů. Je polstrovaná, aby byla velikost rovnoměrná.

Zdroje obrázků používají několik standardních ID čísel.

### Informace o vrstvě a masce ###

Čtvrtá část souboru Photoshopu obsahuje informace o vrstvách a maskách, jako je počet vrstev, kanály ve vrstvách, rozsahy prolnutí, klávesy vrstvy úprav, vrstvy efektů a parametry masky. Pokud nejsou žádné vrstvy nebo masky, je tato sekce reprezentována vynulovaným 4bajtovým polem. Při čtení tohoto oddílu je třeba věnovat zvláštní pozornost délce úseků kvůli vynulovaným hodnotám. Uspořádání sekce vrstvy a masky je následující:


|Délka|Popis
---|---|
|4|Délka sekce s informacemi o vrstvě a masce. (délka PSB je 8 bajtů.)
|Proměnná|Informace o vrstvě
|Proměnná|Informace o masce globální vrstvy
|Proměnná|Série označených bloků obsahujících různé typy dat.

#### Informace o vrstvě ####

Následující tabulka ukazuje organizaci informací vrstvy na vysoké úrovni.


|Délka|Popis
---|---|
|4|Délka informační sekce vrstev, zaokrouhlená nahoru na násobek 2. (délka PSB je 8 bajtů.)
|2|Počet vrstev. Pokud se jedná o záporné číslo, jeho absolutní hodnotou je počet vrstev a první alfa kanál obsahuje údaje o průhlednosti pro sloučený výsledek.
|Proměnná|Informace o každé vrstvě. Viz Záznamy vrstev popisuje strukturu těchto informací pro každou vrstvu.
|Proměnná|Obrazová data kanálu. Obsahuje jeden nebo více záznamů obrazových dat pro každou vrstvu. Vrstvy jsou ve stejném pořadí jako v informacích o vrstvě

### Data obrázku ###

Data obrazových bodů jsou obsažena v části Obrazová data souboru. Uspořádání dat v sekci Obrazová data je v rovinném pořadí, tj. nejprve všechna červená data, poté všechna zelená data atd. Každá rovina je uložena v pořadí skenovacích řádků, bez výplňových bajtů. Sekce obrazových dat je uspořádána ve formátu jak je uvedeno v následující tabulce.

|Délka|Popis
---|---|
|2|Metoda komprese: *0 = nezpracovaná obrazová data * 1 = komprimovaná RLE obrazová data začínají počtem bajtů pro všechny skenované řádky (řádky * kanály), přičemž každý počet je uložen jako dvoubajtová hodnota. Následují komprimovaná data RLE, přičemž každý skenovací řádek je komprimován samostatně. Komprese RLE je stejný kompresní algoritmus, který používá rutina PackBits pro Macintosh ROM a standard TIFF. *2 = ZIP bez predikce *3 = ZIP s predikcí.
|Proměnná|Obrazová data. Rovinné pořadí = RRR GGG BBB atd.

## Reference ##

* [Specifikace formátu souboru PSD – od společnosti Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Formát souboru Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

