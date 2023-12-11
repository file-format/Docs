{
"datum": "2023-03-01",
  "keywords": [
"soubor čipu",
"co je soubor čipu",
"soubor",
"jak otevřít soubor čipu",
"přípona souboru čipu",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CHIP - soubor anotace Microarray",
  "description":"Další informace o formátu souborů CHIP a rozhraních API, která mohou vytvářet a otevírat soubory CHIP.",
  "linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
      "parent": "spreadsheet"
}
},
"lastmod": "2023-03-01"
}

## Co je soubor CHIP?

CHIP file je anotační soubor microarray a souvisí se softwarem Gene Set Enrichment Analysis (GSEA). GSEA je výpočetní metoda, která vyhodnocuje, zda předdefinovaná sada genů (genová sada) vykazuje statisticky významné rozdíly mezi dvěma biologickými stavy, jako je zdravá tkáň versus nemocná tkáň nebo buňky léčené léky versus neléčené. K provedení GSEA potřebujete datovou sadu genové exprese a databázi genové sady. Databáze genových sad obsahuje informace o genech v genových sadách, jako je jejich funkce, dráha nebo tkáňově specifická exprese.

CHIP soubor je specifický typ databáze genových sad, kterou používá GSEA. Obsahuje informace o genech a sadách genů, které jsou relevantní pro platformu microarray používanou v experimentu. Soubor CHIP poskytuje anotace pro každou sondu na mikročipu, jako je symbol genu, název genu, popis genu a umístění chromozomů. Tato informace se používá ke spárování sond s geny v datovém souboru genové exprese a k jejich přiřazení k příslušným genovým sadám pro analýzu GSEA.

Chcete-li použít soubor CHIP v GSEA, musíte jej importovat do softwaru a propojit jej s datovou sadou microarray. GSEA podporuje různé platformy microarray a pro mnohé z nich poskytuje předpřipravené soubory CHIP. Můžete však také vytvořit svůj vlastní soubor CHIP pomocí databází anotací z externích zdrojů, jako je NCBI nebo Ensembl.

## Více informací

Soubor CHIP není tabulkový procesor, ale lze jej otevřít a upravit v tabulkovém procesoru, jako je Microsoft Excel nebo Tabulky Google. Soubor CHIP je typ textového souboru, který obsahuje data oddělená tabulátory, která lze snadno importovat do tabulkového procesoru pro prohlížení a úpravy.

V tabulkovém procesoru můžete manipulovat s daty v souboru CHIP a přidávat, odebírat nebo upravovat anotace pro geny a sady genů na mikročipu. Můžete například použít tabulkový procesor k přidání vlastních anotací pro geny, které nejsou obsaženy v původním souboru CHIP, nebo ke sloučení více souborů CHIP z různých zdrojů do jednoho souboru.

Je však důležité poznamenat, že soubor CHIP má specifický formát a strukturu, které musí být zachovány pro kompatibilitu se softwarem GSEA. Pokud upravíte obsah souboru CHIP v tabulkovém procesoru, měli byste se ujistit, že úpravy nezmění formát souboru nebo obsah způsobem, který by mohl ovlivnit přesnost nebo platnost analýzy GSEA.

## Jak otevřít soubor CHIP?

Protože soubor CHIP obsahuje data oddělená tabulátory, takže pokud chcete zobrazit data tabulky, můžete je otevřít v aplikaci Microsoft Excel.

## Reference
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
