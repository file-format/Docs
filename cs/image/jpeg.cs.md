{
  "date" : "2019-11-25",
  "keywords" :[ "soubor jpeg", "formát souboru jpeg", "co je soubor jpeg", "soubor", "příklad jpeg", "přípona souboru jpeg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - formát souboru obrázku",
  "description":"Další informace o formátu souborů JPEG a rozhraních API, která mohou vytvářet a otevírat soubory JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Co je soubor JPEG? ##

JPEG je typ obrazového formátu, který se ukládá pomocí metody ztrátové komprese. Výstupní obraz, jako výsledek komprese, je kompromisem mezi velikostí úložiště a kvalitou obrazu. Uživatelé mohou upravit úroveň komprese tak, aby dosáhli požadované úrovně kvality a zároveň snížili velikost úložiště. Kvalita obrazu je zanedbatelně ovlivněna, pokud je na obraz aplikována komprese 10:1. Čím vyšší je hodnota komprese, tím vyšší je zhoršení kvality obrazu.

## Specifikace formátu souboru ##

Formát obrazového souboru JPEG byl standardizován skupinou Joint Photographic Experts Group a odtud název JPEG. Formát byl zvolen pro ukládání a přenos fotografických obrázků na webu. Téměř všechny operační systémy nyní mají prohlížeče, které podporují vizualizaci obrázků JPEG, které jsou často uloženy také s příponou JPG. Dokonce i webové prohlížeče podporují vizualizaci obrázků JPEG. Než se pustíme do specifikací formátu souborů JPEG, je třeba zmínit celkový proces jednotlivých kroků při vytváření JPEG.

### Kroky komprese JPEG ###

**Transformace:** Barevné obrázky jsou transformovány z RGB do jasového/chrominančního obrazu (oko je citlivé na jas, nikoli na chrominanci, takže chrominanční část může ztratit mnoho dat, a proto může být vysoce komprimována.

**Vzorkování dolů:** Vzorkování dolů se provádí pro barevnou složku a ne pro složku jasu. Vzorkování dolů se provádí buď v poměru 2:1 horizontálně a 1:1 vertikálně (2h 1 V). Obraz se tedy zmenšuje, protože se nedotýkáte složky 'y', nedochází ke znatelné ztrátě kvality obrazu.

**Uspořádání do skupin:** Pixely každé barevné složky jsou uspořádány do skupin 8×2 pixelů nazývaných „datové jednotky“, pokud počet řádků nebo sloupců není násobkem 8, spodní řádek a sloupce zcela vpravo jsou duplikovány.

**Diskrétní kosinová transformace:** Diskrétní kosinová transformace (DCT) je poté aplikována na každou datovou jednotku, aby se vytvořila mapa 8×8 transformovaných komponent. DCT zahrnuje určitou ztrátu informací kvůli omezené přesnosti počítačové aritmetiky. To znamená, že i bez mapy dojde k určité ztrátě kvality obrazu, ale obvykle je malá.

**Kvantizace:** Každá z 64 transformovaných složek v datové jednotce je rozdělena samostatným číslem nazývaným její 'Kvantizační koeficient (QC)' a poté zaokrouhlena na celé číslo. Zde se informace nenávratně ztratí, velká kontrola kvality způsobí další ztráty. Obecně platí, že většina nástrojů JPEG umožňuje použití tabulek QC doporučených standardem JPEG.

**Kódování:** 64 kvantovaných transformovaných koeficientů (které jsou nyní celá čísla) každé datové jednotky je zakódováno pomocí kombinace RLE a Huffmanova kódování.

**Přidání záhlaví:** Poslední krok přidá záhlaví a všechny použité parametry JPEG a vydá výsledek.

Dekodér JPEG používá kroky v obráceném pořadí k vytvoření původního obrazu z komprimovaného obrazu.

### Struktura souboru ###

Obrázek JPEG je reprezentován jako sekvence segmentů, kde každý segment začíná značkou. Každá značka začíná bajtem 0xFF následovaným příznakem značky, který představuje typ značky. Užitná zátěž následovaná značkou se liší podle typu značky. Běžné typy značek JPEG jsou uvedeny níže:

|Krátký název|Bajty|Úžitková zátěž|Název|Komentáře
---|---|---|---|---|
|SOI|0xFF, 0xD8|žádné|Začátek obrázku|
|S0F0|0xFF, 0xC0|proměnná velikost|Začátek rámce|
|S0F2|0xFF, 0xC2|proměnná velikost|Začátek rámečku|
|DHT|0xFF, 0xC4|proměnná velikost|Definovat Huffmanovy tabulky|
|DQT|0xFF, 0xDB|proměnná velikost|Definovat tabulku(y) kvantifikace|
|DRI|0xFF, 0xDD|4 bajty|Definovat interval restartu|
|SOS|0xFF, 0xDA|proměnná velikost|Začátek skenování|
|RSTn|0xFF, 0xD//n//(/cs//n//#0..7)|žádné|Restartovat|
|APPn|0xFF, 0xE//n//|proměnná velikost|Specifické pro aplikaci|
|COM|0xFF, 0xFE|proměnná velikost|Komentář|
|EOI|0xFF, 0xD9|žádný|Konec obrázku|

V rámci entropicky kódovaných dat je po libovolném bajtu 0xFF kodérem před další bajt vložen bajt 0x00, takže se nezdá, že by tam byla značka tam, kde žádná není zamýšlena, což zabraňuje chybám v rámování. Dekodéry musí přeskočit tento 0x00 bajt. Tato technika, nazývaná [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (viz část specifikace JPEG F.1.2.3), se aplikuje pouze na data kódovaná entropií, nikoli na data užitečného zatížení značek. . Všimněte si však, že entropicky kódovaná data mají několik vlastních značek; konkrétně značky Reset (0xD0 až 0xD7), které se používají k izolaci nezávislých částí entropicky kódovaných dat, aby bylo umožněno paralelní dekódování, a kodéry mohou tyto značky Reset v pravidelných intervalech vkládat (ačkoli ne všechny kodéry to dělají).

