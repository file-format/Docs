{
  "date" : "2019-10-11",
  "keywords" :[ "soubor apng", "formát souboru apng", "co je soubor apng", "soubor", "příklad apng", "přípona souboru apng", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru APNG - animovaný přenosný síťový grafický soubor",
  "description":"Další informace o formátu souboru APNG a rozhraních API, která mohou vytvářet a otevírat soubory APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor APNG?

Soubor s příponou .apng (Animated Portable Network Graphics) je rastrový grafický formát a je neoficiálním rozšířením Portable Network Graphic ([PNG](/cs/image/png/) ). Skládá se z několika snímků (každý z obrázku PNG), které představují sekvenci animace. To poskytuje podobnou vizualizaci jako soubor [GIF](/cs/image/gif/). Soubory APNG podporují 24bitové obrázky a 8bitovou průhlednost. APNG je zpětně kompatibilní s neanimovanými soubory GIF. Soubory APNG používají stejnou příponu .png a lze je otevřít aplikacemi, jako je Mozilla Firefox, Chrome s podporou APNG, aplikace iMessage pro iOS 10.

## Stručná historie

* Specifikace APNG byly vytvořeny v roce 2004, aby poskytovaly podporu pro animované obrázky PNG
* Dekodéry APNG byly vyvinuty s mnohem menšími rozměry a za použití zadní strany dekodéru PNG
* Po průběžných úvahách byl formulován nový typ MIME image/apng, přičemž rozšíření zůstalo stejné jako .png místo .apng
* APNG bylo oficiálně odmítnuto skupinou PNG dne 20. dubna 2007 kvůli jeho jednotnosti s obrázky PNG a zároveň má odlišné specifikace

## Formát souboru APNG

Soubory APNG jsou uloženy jako binární soubory na disku a používají rozšířené specifikace PNG pro animované obrázky. První snímek souboru APNG je normální proud PNG, který lze číst pomocí dekodérů PNG pro zobrazení. Formát souboru APNG odpovídá specifikacím PNG a data jsou uložena v segmentech nazývaných kusy. APNG však představilo následující nové kousky:

`Animation Control Chunk (acTL)` - Označuje, že tento soubor je animovaný soubor PNG, nikoli normální soubor PNG. Funguje jako značka a předchází blok IDAT. Obsahuje také počet snímků a informace o časech pro opakování animací

„Chunk kontroly rámce“ – Vyskytuje se na začátku každé a metadatové informace, jako jsou rozměry, poloha, aplikace průhlednosti a informace o nahrazení předchozím nebo následujícím snímkem, jakmile skončí.

`Frame Data Chunk` - Ukládá obsah snímku a začíná pořadovým číslem. Toto pořadové číslo má stejnou strukturu jako výchozí část IDAT obrázku.

{{< figure src="../APNG.png" alt="Animovaný PNG - Formát souboru APNG" >}}

APNG je zpětně kompatibilní s PNG, protože specifikace laterálu byly navrženy tak, že aplikace, která čte soubor PNG, má jednoduše ignorovat části, kterým nerozumí. Specifikace týkající se bitové hloubky, typu barev, komprese, filtrů, metod prokládání a informací o paletě se používají stejně jako u výchozího formátu PNG.

## APNG vs GIF

Vzhledem k tomu, že GIF již existuje a je používán po dlouhou dobu, možná vás zajímá, jak se APNG liší od GIF. Následuje sada srovnání mezi APNG a GIF, která poskytuje stručnou představu o obou formátech souborů.

||APNG|GIF|
---|---|---|
|Zveřejněno|2004|1987|
|Barevná hloubka|24 bitů|8 bitů|
|Snímková frekvence|Neomezeno|10 snímků za sekundu|
|Transparentnost|Úplná a částečná|Úplná|
|Komprese|Velmi dobrá|Dobrá|

## Reference

* [Formát souboru APNG](https://en.wikipedia.org/wiki/APNG)
* [Specifikace oficiálního formátu PNG](https://www.w3.org/TR/PNG/)

