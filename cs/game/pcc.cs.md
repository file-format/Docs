{
  "date" : "2021-09-08",
  "keywords" :[ "soubor pcc", "formát souboru pcc", "co je soubor pcc", "soubor", "příklad pcc", "přípona souboru pcc", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru Mass Effect PCC a rozhraních API, která mohou vytvářet a otevírat soubory PCC.",
  "title" :"PCC - Mass Effect Package File",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Co je soubor PCC?

Soubor s .pcc je soubor [Hra s hromadným efektem](https://www.ea.com/games/mass-effect/mass-effect-3), který obsahuje herní data pro úpravu herního obsahu, jako jsou modely, textury a pokoje. Mass Effect 2 a 3 jsou první střílečky založené na herním enginu Unreal Engine 3. Hra byla původně vyvinuta společností [Bioware](https://www.bioware.com/about/), která ponechala většinu herních zdrojů ve svém proprietárním formátu souborů PCC. Společnost Bioware získala společnost Electronic Arts, přední globální vydavatel interaktivní zábavy.

## Formát souboru PCC – Další informace

Soubory PCC obsahují komprimované a/nebo nekomprimované struktury, které přispívají k celkové organizaci souborů.

### Struktura komprimovaného PCC

Komprimovaný soubor PCC se skládá z tabulek a dat, která jsou rozdělena do bloků. Každý blok obsahuje proměnný počet komprimovaných bloků.

* `Hlavička bloků` – 16bajtová společná hlavička obsahující informace o blokech.
* `Chunk Header` – 16bajtová hlavička obsahující informace o nezpracovaných komprimovaných datech obsažených ve formě bloku.

### Nekomprimovaná struktura PCC

Nekomprimované soubory PCC jsou rozděleny do následujících pěti částí.

* `Header` - obsahuje základní informace o struktuře souboru PCC.
* `Tabulka názvů` - obsahuje název nalezený uvnitř balíčku včetně importních tříd, exportů a vlastností exportu.
* `Import Table` - obsahuje všechny třídy a objekty importované PCC.
* `Exportovat tabulku` - obsahuje všechny objekty uložené v balíčku. Každý export se může lišit velikostí.

## Reference

* [Me3Explorer – formát souboru PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Hra Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

