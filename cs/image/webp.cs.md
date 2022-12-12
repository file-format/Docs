{
  "date" : "2019-10-11",
  "keywords" :[ "soubor webp", "formát souboru webp", "co je soubor webp", "soubor", "příklad webp", "přípona souboru webp", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google Raster Image File Format",
  "description":"Další informace o formátu souboru WEBP a rozhraních API, která mohou vytvářet a otevírat soubory WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor WEBP?

WebP, představený společností Google, je moderní formát rastrových webových obrázků, který je založen na bezztrátové a ztrátové kompresi. Poskytuje stejnou kvalitu obrazu a výrazně snižuje velikost obrazu. Protože většina webových stránek používá obrázky jako efektivní reprezentaci dat, použití obrázků WebP na webových stránkách vede k rychlejšímu načítání webových stránek. Podle Googlu jsou bezztrátové obrázky WebP o 26 % menší ve srovnání s [PNG](/cs/image/png/), zatímco ztrátové obrázky WebP jsou o 25–34 % menší než srovnatelné obrázky [JPEG](/cs/image/jpeg/). Obrázky jsou porovnávány na základě indexu strukturní podobnosti (SSIM) mezi WebP a jinými formáty souborů obrázků. WebP je sesterský projekt formátu multimediálních kontejnerů [WebM](https://en.wikipedia.org/wiki/WebM).

## Přehled funkcí WebP ##

Obrázky WebP používají proces komprese založený na predikci pixelů z jejich okolních bloků, což vede k tomu, že pixely lze použít vícekrát v jednom souboru. Podporuje animované obrázky a očekává se, že v budoucnu bude podporovat další funkce. Společnost Google zpřístupnila zdrojový kód [online](https://developers.google.com/speed/webp/download) pro svůj kodér a dekodér, aby jej bylo možné použít tam, kde je to nutné. Obrázek WebP poskytuje podporu pro:

* **Ztrátová komprese:** Ztrátová komprese je založena na kódování klíčových snímků [VP8](http://en.wikipedia.org/wiki/VP8). VP8 je formát pro kompresi videa vytvořený společností On2 Technologies jako nástupce formátů VP6 a VP7.
* **Bezztrátová komprese:** Formát bezztrátové komprese je vyvinut týmem WebP.
* **Transparentnost:** 8bitový alfa kanál je užitečný pro grafické obrázky. Alfa kanál lze použít spolu se ztrátovým RGB, což je funkce, která v současnosti není dostupná u žádného jiného formátu.
* **Animace:** Podporuje animované obrázky ve skutečných barvách.
* **Metadata:** Může obsahovat metadata EXIF a XMP (používaná například fotoaparáty).
* **Barevný profil:** Může mít vložený ICC profil.

Ztrátová komprese WebP používá ke kódování obrazu prediktivní kódování, stejnou metodu, kterou používá video kodek VP8 pro kompresi klíčových snímků ve videích. Prediktivní kódování používá hodnoty v sousedních blocích pixelů k predikci hodnot v bloku a poté zakóduje pouze rozdíl.

Bezeztrátová komprese WebP využívá již viděné fragmenty obrázků k přesné rekonstrukci nových pixelů. Může také použít místní paletu, pokud není nalezena žádná zajímavá shoda.

## Formát souboru ##

Formát souboru WebP je založen na formátu dokumentu RIFF (resource interchange file format). Kontejner WebP poskytuje podporu nad rámec funkcí, které obsahují pouze jeden obrázek zakódovaný jako klíčový snímek VP8. Základním prvkem souboru RIFF je blok, který se skládá z:


|Pole|Popis
---|---|
|Chunk FourCC: 32 bitů|ASCII čtyřmístný kód používaný pro identifikaci bloku
|Velikost bloku: 32 bitů (uint32)|Velikost bloku bez tohoto pole, identifikátor bloku nebo výplň
|Užitečné zatížení bloku: Byty velikosti bloku|Datové užitečné zatížení. Pokud je velikost bloku lichá, přidá se jeden výplňový bajt ~-~-, který by měl být 0 ~-~-
|ChunkHeader ('ABCD')|Používá se k popisu záhlaví FourCC a Chunk Size jednotlivých bloků, kde 'ABCD' je FourCC pro blok. Velikost tohoto prvku je 8 bajtů.

### Záhlaví WebP ###

Záhlaví souboru WebP je následující:

* Záhlaví RIFF – 32 bitů představujících znaky ASCII 'R' 'I' 'F' 'F'
* Velikost souboru - 32 bitů (uint32) představující velikost souboru v bajtech počínaje offsetem 8. Maximální hodnota tohoto pole je 2^32 minus 10 bajtů, a tedy velikost celého souboru je maximálně 4GiB minus 2 bajty .
* 'WEBP' - 32 bitů představujících znaky ASCII 'W' 'E' 'B' 'P'

### Ztrátový formát souboru ###

Obrázky WebP používají ztrátový formát souboru, pokud je obrázek založen na ztrátovém kódování a nevyžaduje žádné pokročilé/rozšířené funkce, jako je průhlednost, animace, alfa atd. Ztrátové obrázky jsou menší a podporují je i starší aplikace.

Soubor WebP se v tomto případě skládá z:

* 12 bajtů záhlaví souboru WebP
* Chunk VP8

[Průvodce formátem a dekódováním dat VP8](https://tools.ietf.org/html/rfc6386) ilustruje specifikace formátu bitového toku VP8.

### Bezztrátový formát souboru ###

Toto rozložení se používá, když je obraz založen na bezztrátovém kódování a nejsou potřeba pokročilé funkce poskytované externím formátem. Starší aplikace však nemusí být schopny takové soubory číst.

Soubor WebP se v tomto případě skládá z:

* 12 bajtů záhlaví souboru WebP
* Kus VP8L

## Reference ##

* [WebP Developer's Reference – By Google](https://developers.google.com/speed/webp/)
* [Formát souboru WebP – podle Wikipedie](https://en.wikipedia.org/wiki/WebP)

