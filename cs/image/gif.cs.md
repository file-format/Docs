{
  "date" : "2019-10-11",
  "keywords" :[ "soubor gif", "formát souboru gif", "co je soubor gif", "soubor", "příklad gif", "přípona souboru gif", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Formát souboru obrázku",
  "description":"Další informace o formátu souboru GIF a rozhraních API, která mohou vytvářet a otevírat soubory GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GIF? ##

Formát GIF nebo Graphical Interchange Format je typ vysoce komprimovaného obrázku. GIF, vlastněný Unisysem, používá kompresní algoritmus LZW, který nesnižuje kvalitu obrazu. Pro každý obrázek GIF obvykle povoluje až 8 bitů na pixel a v celém obrázku je povoleno až 256 barev. Na rozdíl od obrázku [JPEG](/cs/image/jpeg/), který může zobrazit až 16 milionů barev a poměrně se dotýká hranic lidského oka. Když se objevil internet, zůstaly GIFy nejlepší volbou, protože vyžadovaly malou šířku pásma a byly kompatibilní s grafikou, která spotřebovává plné barevné plochy. Animovaný GIF kombinuje četné obrázky nebo snímky do jednoho souboru a zobrazuje je v sekvenci, aby vytvořil animovaný klip nebo krátké video. Omezení barev jsou až 256 pro každý snímek a pravděpodobně budou nejméně vhodná pro reprodukci jiných obrázků a fotografií s barevným přechodem.

## Formát souboru GIF ##

Koncepčně mají soubory GIF grafickou oblast pevné velikosti vyplněnou nulou nebo více obrázky. Některé soubory GIF rozdělují grafickou plochu nebo bloky pevné velikosti na dílčí obrázky, které v případě animovaného GIFu fungují jako animované snímky. Formát GIF používá k uložení bitmapových dat hloubku pixelů 1 až 8 bitů. K uložení obrázků se vždy používají data barevného modelu RGB a palety. Záhlaví s pevnou délkou ("GIF87a" nebo "GIF89a") v závislosti na verzi definuje začátek typického souboru GIF.

V současné době jsou k dispozici dvě verze GIF: 87a a 89a. První je původní formát GIF, zatímco druhý je nový formát GIF. V tomto formátu souboru jsou charakteristiky bloků a rozměry pixelů zmíněny v deskriptoru logické obrazovky s pevnou délkou. Existence a velikost globální tabulky barev může být specifikována deskriptorem obrazovky, který sleduje další podrobnosti, pokud jsou k dispozici. Upoutávka je poslední bajt souboru, který obsahuje jeden bajt středníku ASCII. Typické rozložení souboru GIF87a je následující:

### Záhlaví ###

Záhlaví obsahuje šest bajtů a používá se k určení typu souboru jako GIF. Ačkoli je logický deskriptor obrazovky oddělen od skutečného záhlaví, někdy je považován za druhé záhlaví. Stejná struktura, která se používá pro uložení hlavičky, může ukládat logický deskriptor obrazovky. Všechny soubory GIF začínají 3bajtovým podpisem a jako identifikátor používají znaky „GIF“. Verze má také velikost tři bajty a deklaruje verzi souboru GIF.

### Logický deskriptor obrazovky ###

Popisovač obrázku s pevnou délkou určuje obrazovku a informace o barvě potřebné k vytvoření obrázku GIF. Pole Výška a Šířka ohraničují nejmenší hodnotu rozlišení obrazovky, která je povinná pro zobrazení obrazových dat. Není-li zobrazovací zařízení schopno zobrazit specifikované rozlišení, bude pro vhodné zobrazení obrazu potřeba změnit měřítko. Obrazovka a informace o barevné mapě se zobrazují ve čtyřech podpolích níže uvedené tabulky (zatímco bit 0 je nejméně významný bit):


|Bity|Podpole
---|---|
|0-2|Velikost globální tabulky barev
|3|Příznak řazení tabulky barev
|4-6|Barevné rozlišení
|7|Globální příznak tabulky barev

#### Globální tabulka barev ####

Volitelná globální tabulka barev je umístěna hned za logickým deskriptorem obrazovky. Tato tabulka mapovaná pro indexování dat barev pixelů uvnitř obrazových dat. Pokud neexistuje globální tabulka barev, každý obrázek v souboru GIF používá svou místní barvu. Pokud chybí globální i místní tabulka barev, je lepší zadat výchozí tabulku barev. Série tříbajtových trojic tvoří prvky tabulky barev. Každý bajt charakterizuje hodnotu barvy RGB. Červená, zelená a modrá barva se používají jako hodnoty každého prvku tabulky barev. Položky v globální tabulce barev zasahují maximálně 256 položek a vždy představují mocninu dvou.

#### Data obrázku ####

Obrazová data ukládají bajt nekódovaných symbolů následovaný propojeným seznamem dílčích spolu s daty kódovanými LZW.

#### Upoutávka ####

Trailer představuje jeden bajt dat, který je posledním znakem v souboru. Hodnota tohoto bajtu je trvale 3Bh a určuje konec datového toku. Každý soubor GIF musí mít v posledním z každého souboru upoutávku.

## Reference ##

* [formát souboru GIF](https://en.wikipedia.org/wiki/GIF)

