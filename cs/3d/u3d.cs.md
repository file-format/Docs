{
  "date" : "2019-10-11",
  "keywords" :[ "soubor u3d", "formát souboru u3d", "co je soubor u3d", "soubor", "příklad u3d", "přípona souboru u3d", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Univerzální 3D formát souboru",
  "description":"Další informace o formátu souboru U3D a rozhraních API, která mohou otevírat a vytvářet soubory U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor U3D?

**U3D** (Universal 3D) je komprimovaný formát souboru a datová struktura pro 3D počítačovou grafiku. Obsahuje informace o 3D modelu, jako jsou trojúhelníkové sítě, osvětlení, stínování, pohybová data, čáry a body s barvou a strukturou. Formát byl přijat jako standard[ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm) v srpnu 2005. Dokumenty 3D [PDF](/cs/pdf/) podporují U3D vkládání objektů a lze je zobrazit v aplikaci Adobe Reader (verze 7 a novější).

Formát U3D byl vyvinut s ohledem na cíl vytvořit univerzální standard pro trojrozměrné ukládání a výměnu dat. Formát však nachází své hlavní využití spíše v kódování pro 3D PDF, než aby byl používán jako výměnný formát. Acrobat 3D převede podporovaný typ 3D souboru po převodu do PDF buď na U3D, nebo PRC.

## Formát souboru U3D

Soubory U3D jsou v binárním formátu souboru, který prošel čtyřmi vydáními, jak je popsáno v referenčním dokumentu [ECMA-363] (http://www.ecma-international.org/publications/standards/Ecma-363.htm), což vede k aktualizaci specifikací s každým vydáním. Standard souboru PDF ISO-32000 přijímá U3D jako povolenou anotaci a typ multimédií.

První vydání U3D bylo zaměřeno na klíčové reprezentace vlastností 3D grafiky, jako je geometrie, barva, textury, osvětlení, kosti a animace založené na transformaci. Druhé a třetí vydání opravilo některé chyby v prvním vydání, přičemž třetí verze byla nejběžněji používaným typem průmyslového softwaru. Čtvrté vydání poskytuje definice pro primitiva vyššího řádu (zakřivené povrchy). [Specifikace U3D] (http://www.ecma-international.org/publications/standards/Ecma-363.htm) jsou k dispozici online pro uživatele na webových stránkách ECMA.

### Datové typy v souborech U3D

Binární soubor bude obsahovat následující typy: U8, U16, U32, U64, I16, I32, F32, F64 a String.

* U8: 8bitové celé číslo bez znaménka
* U16: 16bitové celé číslo bez znaménka
* U32: 32bitové celé číslo bez znaménka
* U64: 64bitové celé číslo bez znaménka
* I16 : 16bitové celé číslo se znaménkem
* F32: IEEE jeden přesný plovák.
* F64: IEEE plovák s dvojitou přesností.
* Řetězec: Řetězce v souboru U3D začínají 16bitovým celým číslem bez znaménka, které definuje celkovou délku znaků v řetězci. Řetězce jsou vždy zpracovány jako malá a velká písmena.

## Struktura souboru U3D

Soubor U3D obsahuje sekvenci bloků. V každém souboru U3D jsou 3 různé typy bloku.

* Blok záhlaví souboru
* Blok prohlášení
* Blok pokračování

Zavaděč určí konec bloku, pokud data v tomto bloku nejsou vyžadována nebo pokud dekodér pro tento typ bloku není k dispozici.

{{< figure src="../u3d.png" alt="Formát souboru U3D" >}}

### Blok záhlaví souboru
Blok záhlaví souboru obsahuje informace o souboru, které načtený používá k určení způsobu čtení souboru.

### Blok prohlášení

Bloky deklarací obsahují informace o objektech v souboru. Objekty v deklaračním bloku musí být definovány.

### Blok pokračování

Další informace pro objekty deklarované v bloku Declaration jsou uvedeny v bloku pokračování. Každý blok pokračování musí být spojen s blokem prohlášení.


## Reference ##

* [Formát souboru U3D – Wikipedie](https://en.wikipedia.org/wiki/Universal_3D)
* [Specifikace formátu souboru ECMA U3D](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

