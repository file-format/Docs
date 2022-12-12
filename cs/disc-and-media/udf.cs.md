{
  "date" : "2021-08-17",
  "keywords" :[ "soubor udf", "formát souboru udf", "co je soubor udf", "soubor", "příklad udf", "přípona souboru udf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů UDF a rozhraních API, která mohou vytvářet a otevírat soubory UDF.",
  "title" :"UDF - Universal Disk Format File",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Co je soubor UDF?
Soubor s příponou .udf je formát obrazu disku obvykle používaný pro ukládání souborů na optická média; lze použít pro vypalování DVD, CD a dalších optických médií; ukládá kolekci souborů pomocí adresářové struktury specifikované ve standardu UDF; umožňuje smazat a upravit soubory na cílovém disku i poté, co byly zapsány. Společnost Optical Storage Technology Association stanovila souborový systém UDF jako standard pro vytvoření společného souborového systému pro všechna optická média, jako jsou přepisovatelná optická média a média pouze pro čtení.

## Formát souboru UDF
Formát souboru UDF je otevřený souborový systém nezávislý na výrobci pro ukládání počítačových dat pro širokou škálu médií. Běžně se používá pro DVD a novější formáty optických disků. Obvykle software ovládá souborový systém UDF v dávkovém procesu a zapisuje jej na optická média v jediném průchodu. Když však zapisuje pakety na přepisovatelná média, UDF umožňuje vytvářet, mazat a měnit soubory na disku podobně jako univerzální souborový systém na vyměnitelných médiích, jako jsou flash disky nebo diskety.
### Specifikace UDF
Standard UDF definuje následující tři varianty souborového systému:

- **Plain Build**: Toto je původní formát podporovaný ve všech revizích UDF. Byl představen v první verzi standardu, tento formát lze použít na jakémkoli typu disku, který umožňuje náhodný přístup pro čtení nebo zápis, jako jsou DVD+RW, pevné disky a média DVD-RAM.
- **VAT build**: Používá se speciálně pro zápis na média s jednorázovým zápisem. DPH je další struktura na disku, která umožňuje zápis paketů; to znamená přemapování fyzických bloků, když jsou soubory nebo jiná data na disku změněna nebo odstraněna. U médií s jednorázovým zápisem je celý disk virtualizován, díky čemuž je povaha jednorázového zápisu pro uživatele transparentní; s diskem lze zacházet stejně jako s přepisovatelným diskem.
- **Spared (RW) build**: Používá se speciálně pro zápis na přepisovatelná média. Přidává extra Sparing Table pro správu chyb, které se nakonec vyskytnou na částech disku, které byly několikrát přepisovány. Tato tabulka ukládá stopu opotřebovaných sektorů a přemapuje je na fungující. Správa defektů UDF se nevztahuje na systémy, které již implementují jinou formu správy defektů, jako je Mount Rainier (MRW) pro optické disky nebo řadič disku pro pevný disk.
 




## Reference


* [Windows Imaging Format – z Wikipedie](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


