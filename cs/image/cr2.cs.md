{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru CR2 – obrazový soubor Canon Raw 2",
  "description":"Další informace o formátu souboru CR2 a rozhraních API, která mohou vytvářet a otevírat soubory CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Co je soubor CR2?

Soubor CR2 (Camera RAW 2) je soubor obrázku RAW vytvořený digitálními fotoaparáty Canon. Ukládá původní nezpracovaná bezztrátová obrazová data zachycená fotoaparátem. Formát souboru CR2 byl vyvinut společností Canon pro své digitální fotoaparáty a dokáže zaznamenávat vysoce kvalitní snímky až do 14 bitů RGB. To vytváří vysoce kvalitní snímky s dostatečným prostorem pro následné zpracování. Formát obrazu CR2 používá Canon ve svých modelech fotoaparátů 350D, 20D a 1D. Soubory CR2 jsou soubory RAW a obsahují další informace o metadatech, jako jsou informace o fotoaparátu, informace o objektivu, informace o bracketingu, vyvážení bílé a další nastavení.

## Formát souboru CR2

Soubory CR2 se ukládají na paměťovou kartu fotoaparátu jako binární soubory ve formátu proprietárních souborů společnosti Canon. Formát souboru CR2 nahradil původně používaný formát souboru CRW a později byl nahrazen formátem souboru Canon RAW 3. Formát souboru CR2 je založen na specifikacích [TIFF](/cs/image/tiff/), který má 4 adresáře obrazových souborů (IFD).

|Offset |Obsah |Komentář|
---|---|---|
|0x0000 |Záhlaví |obsahuje řazení bytů, verzi a offset do RAW fotografie|
|vypočteno |IFD#0 |tato část obsahuje sekci Exif, která obsahuje sekci Makernotes.
Informace o obrázku#0|
|vypočítaný |obrázek#0 |malá verze obrázku (velikost jedné čtvrtiny originálu), komprimovaná ve formátu Jpeg|
|vypočítáno |IFD#1 |Informace o obrázku#1.|
|vypočítaný |obrázek#1 |malá verze obrázku, komprimovaná ve formátu Jpeg|
|vypočítáno |IFD#2 |Informace o obrázku#2.|
|vypočítaný |obrázek#2 |malá verze obrázku, nekomprimovaná|
|v záhlaví| IFD#3| Informace o obrázku č. 3, plnorozměrném obrázku RAW|
|vypočítaný |obrázek#3 |Obrázková data RAW, bezeztrátově komprimovaná ve formátu Jpeg (nikoli data RGB!)|

## Výhoda formátu souboru CR2

Ukládání snímků ve formátu RAW umožňuje mnoho následného zpracování fotografie, jako je úprava vyvážení bílé. To je mnohem obtížnější as velkou ztrátou kvality u jiných formátů obrazových souborů, jako je [JPEG](/cs/image/jpeg/).

## Je CR2 lepší než JPEG?

Soubory CR2 jsou nezpracované soubory bez jakékoli ztráty dat, a tedy bez ztráty kvality. JPEG na druhé straně je ztrátový formát souboru obrázku, protože kvůli zmenšení souboru ztrácí některá data. Soubory CR2 jsou tedy vysoce kvalitní a vhodnější pro retuše a vylepšení.

## Reference

* [Formát souboru CR2](http://lclevy.free.fr/cr2/)

