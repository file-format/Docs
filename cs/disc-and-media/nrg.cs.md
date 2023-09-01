{
  "date" : "2021-08-16",
  "keywords" :[ "soubor nrg", "formát souboru nrg", "co je soubor nrg", "soubor", "příklad nrg", "přípona souboru nrg", "přípona", "formát", "zápatí nrg", "soubor formát nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů NRG a rozhraních API, která mohou vytvářet a otevírat soubory NRG.",
  "title" :"NRG - Formát souboru obrazu disku",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Co je soubor NRG?

Formát souboru obrázku, který je vytvořen pomocí optického disku, je považován za formát souboru NRG. Tento formát je speciálně vytvořen společností Nero pro nástroj Nero Burning Rom. Pro ukládání obrazů disků se tento formát považuje za používaný, protože je vhodný pro tyto konkrétní soubory. Tyto soubory mohou být ve formě přesné kopie disku CD nebo DVD nebo mohou mít několik souborů, které lze připojit jako disk. Další populárnější formáty souborů, jako jsou formáty souborů [ISO](/cs/compression/iso/), jsou ty, do kterých lze tyto soubory převést na některé základní nástroje. Soubory NRG se většinou používají k vytváření záloh nebo kopií některých důležitých dat nebo disků.

## Formát souboru NRG ##

Tento formát souboru byl vyvinut společností Nero AG jako formát obrazu disku. Měl specifickou vlastnost nástroje Nero Burning Rom, protože byl vyvinut pro ukládání obrazů disků. Jeho první verze byla určena k ukládání hodnot jako 32bitová celá čísla. Byla však spuštěna jeho druhá verze a obsahovala podporu pro 64bitová celá čísla.

## Technické specifikace ##

Na začátku souboru tento formát neukládá svá data jako záhlaví. Stejně jako zápatí je připojeno na konec souboru. Ve formě kousků IFF se ukládají informace o obrázku. Offset prvního bloku lze získat čtením zápatí NRG na posledních 8 až 12 bytech souboru. Ve všech verzích formátu souboru NRG jsou k němu připojeny bloky, DAOI, CD text, typ média s informacemi o relaci, informace o disku, Relo a konec řetězce. Pořadí bajtů je big-endian a všechny celočíselné hodnoty jsou v době uložení bez znaménka.

### Hlavní kusy ###

#### Tahač ####

Tento cue sheet je snadno dostupný ve všech verzích formátu souborů NRG. Část **CUEX** znamená bloky zřetězení pevné velikosti a každý z nich představuje startovací bod.

#### Informace o DAO ####

Tyto informace jsou také přítomny ve všech verzích formátu NRG. Kousky **DAOI** ukládají příslušné konkrétní informace ve 2 částech. Jeho první část se skládá pouze z dat specifických pro relaci. Jeho druhá část pouze opakuje šedou informaci týkající se sledování a je pouze jednou pro každou stopu.

#### CD-text ####

To je k dispozici ve druhé verzi NRG. Část **CDTX** se skládá z nezpracovaného zřetězení textového balíčku CD, který má pro každý 18 bajtů.

#### Rozšířené informace o skladbě ####

To je k dispozici ve všech verzích formátu souboru NRG. Tyto části se používají pro ukládání informací o sledování pro stopu relací najednou. Tyto údaje se opakují pouze jednou v případě každé stopy.

#### Informace o relaci ####

To je také k dispozici ve všech verzích formátu souboru NRG. Informace o kouscích relací je třeba využít k rychlému skenování obrazu relace a následnému sledování počtu.

#### Konec řetězce ####

Chunk of end znamená signály, že nyní již nejsou žádné další části, které je třeba číst, a to je také dostupné ve všech verzích NRG.


## Reference ##

* [NRG – podle Wikipedie](https://en.wikipedia.org/wiki/NRG_(file_format))


