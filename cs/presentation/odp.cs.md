{
  "date" : "2019-10-11",
  "keywords" :[ "soubor odp", "formát souboru odp", "co je soubor odp", "soubor", "příklad odp", "přípona souboru odp", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice Presentation File Format",
  "description":"Další informace o formátu souboru ODP a rozhraních API, která mohou vytvářet a otevírat soubory ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ODP?

Soubory s příponou .odp představují formát prezentačního souboru používaný OpenOffice.org ve standardu OASISOpen. Soubor prezentace je kolekce snímků, kde každý snímek může obsahovat text, obrázky, formátování, animace a další média. Tyto snímky jsou publiku prezentovány ve formě prezentací s vlastním nastavením prezentace. Soubory ODP lze otevřít aplikacemi, které odpovídají formátu OpenDocument (jako je OpenOffice nebo StarOffice).

## Stručná historie

Specifikace formátu souboru ODP jsou založeny na standardu vyvinutém jako specifikace ODF. Tyto specifikace se v minulosti vyvíjely ve formě tří verzí vyvinutých a publikovaných OASIS takto:

`2005` - Verze 1.0 byla zveřejněna v květnu 2005
`2007` - Verze 1.1 byla zveřejněna v únoru 2007
`2011` - Verze 1.2 byla zveřejněna v září 2011

Při přechodu z verzí ODF 1.0 na 1.1 došlo k poměrně malým změnám. [Verze ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) je nejnovější verzí specifikací ODF a vývojáři by ji měli konzultovat při vývoji aplikací souvisejících se čtením/zápisem ODS.

## Specifikace formátu souboru

Formát OpenDocument podporuje reprezentaci dokumentu jako jeden dokument XML a také kolekci několika dílčích dokumentů v rámci balíčku jako archiv [ZIP](/compression/zip/). Každý ze souborů z archivu ZIP ukládá část kompletního dokumentu. Každý vnořený dokument ukládá určitý aspekt dokumentu. Například jeden vnořený dokument obsahuje informace o stylu a jiný vnořený dokument obsahuje obsah dokumentu. Typický dokument ODF má následující součásti:

* `content.xml` – Obsah dokumentu a automatické styly použité v obsahu.
* `styles.xml` – Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
* `meta.xml` – Metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
* `settings.xml` – Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

Kromě toho může být v balíčku mnoho dalších vnořených dokumentů, jako je miniatura dokumentu, obrázky atd.

Soubory tabulkových dokumentů jsou podmnožinou souborů ODF, kde je obsah (listy) uložen v vnořeném dokumentu content.xml.

## Reference

* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

