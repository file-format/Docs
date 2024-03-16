{
  "date" : "2019-10-11",
  "keywords" :[ "soubor odt", "formát souboru odt", "co je soubor odt", "soubor", "příklad odt", "přípona souboru odt", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - Textový soubor OpenDocument",
  "description":"Další informace o formátu souboru ODT a rozhraních API, která mohou vytvářet a otevírat soubory ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ODT?

Soubory ODT jsou typy dokumentů vytvořených pomocí aplikací pro zpracování textu, které jsou založeny na formátu OpenDocument Text File. Ty jsou vytvořeny pomocí aplikací textového procesoru, jako je bezplatný OpenOffice Writer, a mohou obsahovat obsah, jako je text, obrázky, objekty a styly. Soubor ODT je pro textový procesor Writeru tím, čím je [DOCX](/cs/word-processing/docx/) pro Microsoft Word. Soubory ODT pro úpravy může otevřít několik aplikací včetně Dokumentů Google a webového textového procesoru Google, který je součástí Disku Google. Microsoft Word může také otevírat soubory ODT a ukládat je do jiných formátů, jako je [DOC](/cs/word-processing/doc/) a DOCX.

## Stručná historie ##

Specifikace formátu souboru ODP jsou založeny na standardu vyvinutém jako specifikace ODF. Tyto specifikace se v minulosti vyvíjely ve formě tří verzí vyvinutých a publikovaných OASIS takto:

**2005** Verze 1.0 byla zveřejněna v květnu 2005

**2007:** Verze 1.1 byla zveřejněna v únoru 2007

**2011:** Verze 1.2 byla zveřejněna v září 2011

Při přechodu z verzí ODF 1.0 na 1.1 došlo k poměrně malým změnám. [Verze ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) je nejnovější verzí specifikací ODF a vývojáři by ji měli konzultovat při vývoji aplikací souvisejících se čtením/zápisem ODS.

## Specifikace formátu souboru ##

Formát OpenDocument podporuje reprezentaci dokumentu jako jeden dokument XML a také kolekci několika dílčích dokumentů v rámci balíčku jako archiv [ZIP](/cs/compression/zip/). Každý ze souborů z archivu ZIP ukládá část kompletního dokumentu. Každý vnořený dokument ukládá určitý aspekt dokumentu. Například jeden vnořený dokument obsahuje informace o stylu a jiný vnořený dokument obsahuje obsah dokumentu. Typický dokument ODF má následující součásti:

* content.xml – Obsah dokumentu a automatické styly použité v obsahu.
* styles.xml – Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
* meta.xml – metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
* settings.xml – Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

Kromě nich může být v balíčku mnoho dalších vnořených dokumentů, jako jsou miniatury dokumentu, obrázky atd. Soubory dokumentů jsou podmnožinou souborů ODF, kde je obsah (listy) uložen v subdokumentu //content.xml//.

## Reference ##

* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

