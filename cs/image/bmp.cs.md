{
  "date" : "2019-10-11",
  "keywords" :[ "soubor bmp", "formát souboru bmp", "co je soubor bmp", "soubor", "příklad bmp", "přípona souboru bmp", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - formát souboru obrázku",
  "description":"Další informace o formátu souborů BMP a rozhraních API, která mohou vytvářet a otevírat soubory BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Co je soubor BMP? #

Soubory s příponou .BMP představují soubory bitmapových obrázků, které se používají k ukládání bitmapových digitálních obrázků. Tyto obrázky jsou nezávislé na grafickém adaptéru a nazývají se také formát souboru bitmap nezávislý na zařízení (DIB). Tato nezávislost slouží k otevření souboru na více platformách, jako jsou Microsoft Windows a Mac. Souborový formát BMP může ukládat data jako dvourozměrné digitální obrázky v monochromatickém i barevném formátu s různými barevnými hloubkami.

## Specifikace formátu souboru BMP ##

Bitmapy nezávislé na zařízení fungují jako pomůcka při výměně bitmap mezi zařízeními a aplikacemi. Vzhledem k neustálému vývoji tohoto formátu souboru se informace obsažené v záhlaví mohou lišit od verze Bitmap. Jeden bitmapový soubor se skládá ze struktur s pevnou i proměnnou velikostí v určitém pořadí.

Struktury v bitmapovém souboru jsou uspořádány v následujícím pořadí:


|Struktura|Volitelné|Velikost|Účel
---|---|---|---|
|Záhlaví souboru|Ne|14|Uložení obecných informací o souboru bitmapového obrázku
|Záhlaví DIB|Ne|Pevná velikost|K uložení podrobných informací o bitmapovém obrázku a definování formátu pixelů
|Extra Bit Masks|Ano|12 nebo 16 bajtů|Pro definování formátu pixelů
|Paleta barev|Polovolitelné|Proměnná velikost|K definování barev používaných bitmapovými obrazovými daty
|Mezera1|Ano|Proměnná-velikost|Zarovnání struktury
|Pixel Array|No|Variable-size|Pixelový formát je definován hlavičkou DIB nebo extra bitovými maskami.
|Mezera2|Ano|Proměnná velikost|Zarovnání struktury
|ICC Color profile|Ano|Variable-size|Pro definování barevného profilu pro správu barev

Když je bitmapový obrázek načten do paměti, stane se strukturou DIB, kterou systém Windows používá prostřednictvím rozhraní GDI API. Záhlaví souboru není součástí této datové struktury. Barva může také obsahovat 16bitové položky, které tvoří indexy aktuálně odkazované palety namísto explicitních definic barev RGB. Podívejme se na některé z nich podrobně, zejména na záhlaví.

### Záhlaví bitmapového souboru ###

Záhlaví bitmapového souboru je podobné jiným záhlavím souborů používaným k identifikaci souboru. Protože existují různé varianty formátu souboru BMP, první 2 bajty formátu souboru BMP jsou znak "B" a poté znak "M" v kódování ASCII. Všechny celočíselné hodnoty jsou uloženy ve formátu little-endian.

|Posun hex|Odsazení dek|Velikost|Účel
---|---|---|---|
|00|0|2 bajty|Pole záhlaví používané k identifikaci souboru BMP a DIB je 0x42 0x4D v hexadecimální soustavě, stejně jako BM v ASCII. Může následovat možné hodnoty.* **BM** – Windows 3.1x, 95, NT, ... atd. * **BA** – bitmapové pole struktury OS/2 * **CI** – struktura OS/2 barevná ikona * **CP** – ukazatel stálé barvy OS/2 * **IC** – ikona struktury OS/2 * **PT** – ukazatel OS/2
|02|2|4 bajty|Velikost souboru BMP v bajtech
|06|6|2 bajty|Vyhrazeno; skutečná hodnota závisí na aplikaci, která obrázek vytváří
|08|8|2 bajty|Vyhrazeno; skutečná hodnota závisí na aplikaci, která obrázek vytváří
|0A|10|4 bajty|Offset, tj. počáteční adresa, bajtu, kde lze nalézt data bitmapového obrázku (pole pixelů).

#### DIB hlavička (bitmapová informační hlavička) ####

Tato hlavička představuje podrobné informace o obrázku. Na základě těchto informací bude určena aplikace, která bude použita k zobrazení obrazu na obrazovce. Všechny tyto hlavičky obsahují pole DWORD (32bitové) určující jejich velikost, takže aplikace může snadno určit hlavičku použitou v obrázku. To je v podstatě způsobeno tím, že formát DIB prošel několika rozšířeními. Následuje záhlaví DIB s uvedenými poli.

#### Paleta barev ####

Paleta barev BMP je pole struktur, které určují hodnoty intenzity RGB každé barvy v paletě barev zobrazovacího zařízení. Každý pixel v bitmapových datech ukládá jednu hodnotu použitou jako index v paletě barev. Informace o barvě uložené v prvku na tomto indexu určují barvu tohoto pixelu. Dostupnost barev v bitmapovém souboru se liší následovně:

* Jedno, 4 a 8bitové – očekává se, že vždy bude obsahovat paletu barev
* Šestnáct, 24 a 32 bitů – nikdy neobsahují barevné palety
* Šestnáctibitové a 32bitové soubory BMP – obsahují hodnoty masky bitových polí namísto barevné palety

#### Pixel Storage ####

Bitmapové pixely jsou uloženy jako bity sbalené do řádků, kde je velikost každého řádku zaokrouhlena nahoru na násobek 4 bajtů (32bitové DWORD) pomocí odsazení. Celkový počet bajtů potřebných k uložení pixelů obrázku nelze přímo vypočítat pouhým počítáním bitů. Vzhledem k tomu, že se jedná o odsazení, je vyžadován efekt zaokrouhlení velikosti každého řádku na násobek 4 bajtů. Výplňové bajty (ne nutně 0) se připojují na konec řádků, aby se délka řádků zvýšila na násobek čtyř bajtů. Když je pole pixelů načteno do paměti, každý řádek musí začínat adresou paměti, která je násobkem 4.

Obrázek je ve skutečnosti popsán 32bitovou reprezentací DWORD pole pixelů. Pixely jsou obvykle uloženy „zdola nahoru“, počínaje levým dolním rohem, zleva doprava a poté řádek po řádku odspodu nahoru. Formáty pixelů a jejich důsledky jsou uvedeny níže:

* Formát 1 bit na pixel (1 bpp) podporuje 2 různé barvy (například: černá a bílá).
* Formát 2 bity na pixel (2 bpp) podporuje 4 různé barvy a ukládá 4 pixely na 1 bajt, přičemž pixel nejvíce vlevo je ve dvou nejvýznamnějších bitech. Každá hodnota pixelu je 2bitový index do tabulky až 4 barev.
* Formát 4 bity na pixel (4 bpp) podporuje 16 různých barev a ukládá 2 pixely na 1 bajt, přičemž pixel zcela vlevo je ve výraznějším kousku. Hodnota každého pixelu je 4bitový index do tabulky až 16 barev.
* Formát 8 bitů na pixel (8 bpp) podporuje 256 různých barev a ukládá 1 pixel na 1 bajt. Každý bajt je index do tabulky s až 256 barvami.
* Formát 16 bitů na pixel (16 bpp) podporuje 65 536 různých barev a ukládá 1 pixel na 2 bajty WORD. Každé SLOVO může definovat alfa, červený, zelený a modrý vzorek pixelu.
* Formát 24bitových pixelů (24bpp) podporuje 16 777 216 různých barev a ukládá hodnotu 1 pixelu na 3 bajty. Každá hodnota pixelu definuje červené, zelené a modré vzorky pixelu (8.8.8.0.0 v zápisu RGBAX). Konkrétně v pořadí: modrá, zelená a červená (8 bitů na každý vzorek).
* Formát 32 bitů na pixel (32 bpp) podporuje 4 294 967 296 různých barev a ukládá 1 pixel na 4 bajty DWORD. Každý DWORD může definovat alfa, červený, zelený a modrý vzorek pixelu.

## Reference ##

* [Formát Windows MetaFile](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Formát souboru BMP](https://en.wikipedia.org/wiki/BMP_file_format)

