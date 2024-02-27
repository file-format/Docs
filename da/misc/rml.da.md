{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML - Elixir-rapportskabelonfil",
  "description":"Lær om RML-filer og API'er, der kan oprette og åbne RML-filer.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-da",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Hvad er en RML fil?

En RML-fil er en rapporteringsskabelonfil med rapporteringsmotoren [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Skabelonfilen bruges til at generere rapporter med datakilden forbundet til Elixir FileSystem. Data læses og udfyldes i RML-skabelonfilen og kan eksporteres til en række forskellige filformater såsom [PDF](/pdf/), [RTF](/word-processing/rtf/) og regnearket [XLS](/spreadsheet/xls/). Elixir Repertoire-rapporteringsmotor kan tilsluttes en lang række JDBC-datakilder.

## RML filformat

De interne filstrukturdetaljer for RML-filformat er ikke offentligt tilgængelige. Filerne genereres og gemmes internt af Elixir Repertoire-applikationen for at generere rapporter med data udfyldt fra de tilsluttede datakilder. RML-skabelonfilen indeholder det overordnede layout og pladsholderoplysninger for den endelige rapport, der skal genereres ud fra dataene.

## Hvordan man RML skabelon fil?

For at generere RML-skabelon i Elixir Repertoire kan følgende trin følges.

1. Tilslut en JDBC-datakilde til filsystemet.
1. Start guiden Rapportskabelon
1. Brug softwaren til at finde datakildens .ds-fil
1. Vælg tabelrapport som valg af eksport
1. Vælg de felter, der skal inkluderes i rapportskabelonen
1. Til sidst, når du klikker på knappen Udfør, tilføjes First report.rml til lageret og åbnes for at vise fanen Layout.

## Referencer

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)


