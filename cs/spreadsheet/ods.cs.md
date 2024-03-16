{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "soubor", "rozšíření", "formát souboru", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souboru, abyste věděli, co je soubor ODS a rozhraní API, která je mohou vytvářet a otevírat.",
  "title" :"Co je soubor ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor ODS?

Soubory s příponou .ods představují formát OpenDocument Spreadsheet Document, který může uživatel upravovat. Data jsou uložena v souboru ODF do řádků a sloupců. Je to formát založený na XML a je jedním z několika podtypů v rodině Open Document Formats (ODF). Formát je specifikován jako součást specifikací ODF 1.2 publikovaných a spravovaných OASIS. Soubory ODS pro úpravy a manipulaci může otevírat řada aplikací ve Windows i jiných operačních systémech, včetně aplikací Microsoft Excel, NeoOffice a LibreOffice. Soubory ODS lze také různými aplikacemi převést do jiných tabulkových formátů, jako jsou [XLS](/cs/spreadsheet/xls/), [XLSX](/cs/spreadsheet/xlsx/) a další.

## Stručná historie ##

Specifikace formátu souboru ODS jsou založeny na standardu vyvinutém jako specifikace ODF. Tyto specifikace se v minulosti vyvíjely ve formě tří verzí vyvinutých a publikovaných OASIS takto:

`2005`- Verze 1.0 byla zveřejněna v květnu 2005

`2007` - Verze 1.1 byla zveřejněna v únoru 2007

`2011` - Verze 1.2 byla zveřejněna v září 2011

Při přechodu z verzí ODF 1.0 na 1.1 došlo k poměrně malým změnám. [Verze ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) je nejnovější verzí specifikací ODF a vývojáři by ji měli konzultovat při vývoji aplikací souvisejících se čtením/zápisem ODS.

## Formát souboru ODS ##

Formát OpenDocument podporuje reprezentaci dokumentu jako jeden dokument XML a také kolekci několika dílčích dokumentů v rámci balíčku jako archiv [ZIP](/cs/compression/zip/). Každý ze souborů z archivu ZIP ukládá část kompletního dokumentu. Každý vnořený dokument ukládá určitý aspekt dokumentu. Například jeden vnořený dokument obsahuje informace o stylu a jiný vnořený dokument obsahuje obsah dokumentu. Typický dokument ODF má následující součásti:

* `content.xml` – Obsah dokumentu a automatické styly použité v obsahu.
* `styles.xml` – Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
* `meta.xml` – Metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
* `settings.xml` – Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

Kromě toho může být v balíčku mnoho dalších vnořených dokumentů, jako je miniatura dokumentu, obrázky atd.

Soubory tabulkových dokumentů jsou podmnožinou souborů ODF, kde je obsah (listy) uložen v vnořeném dokumentu content.xml.

## Reference ##

* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

