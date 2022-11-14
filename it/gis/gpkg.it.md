{
  "date" : "2021-07-29",
  "keywords" :[ "file gpkg", "formato file gpkg", "cos'è un file gpkg", "file", "esempio gpkg", "estensione file gpkg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - File in formato GeoPackage",
  "description":"Scopri il formato di file GPKG e le API che possono creare e aprire file GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Che cos'è un file GPKG?
Un file con estensione .gpkg è costituito da un sistema di informazioni geografiche implementato come un contenitore di database SQLite contenente dati e tabelle di metadati con definizioni tipiche, limitazioni di formato, asserzioni di integrità e vincoli di contenuto. È stato pubblicato nel 2014; definito dall'OGC (Open Geospatial Consortium) per conto dell'esercito americano. Vari governi, organizzazioni commerciali e open source supportano ampiamente il GeoPackage.

## Formato file GPKG
Un GeoPackage è costituito da un file di database SQLite 3 esteso; uno standard definisce un insieme di regole (convenzioni obbligatorie) per:
- Memorizzazione di set di immagini a matrice di piastrelle
- Caratteristiche vettoriali
- Mappe raster a varie scale
- Metadati e schema

È possibile estendere un GeoPackage utilizzando le regole di estensione definite nella clausola 2.3 dello standard. Lo scopo della progettazione di un GeoPackage era quello di creare un database il più leggero possibile e includerlo in un unico file pronto per l'uso. Ciò lo rende ideale per applicazioni mobili in modalità offline e condivisione rapida su dispositivi di archiviazione cloud o USB, ecc.

### Contenuti GPKG
I GeoPackage contengono un certo numero di tabelle, come altri database relazionali. Queste tabelle possono essere definite dall'utente o tabelle di metadati. I GeoPackage sono costituiti da due tabelle di metadati obbligatori:

#### gpkg_contents
Un sommario per un GeoPackage. Le colonne obbligatorie in questa tabella sono:

- **table_name**: il nome effettivo della tabella dati definita dall'utente;
- **data_type**: il tipo di dati, ad esempio titoli, caratteristiche e attributi;
- **identificatore e descrizione**: testo leggibile;
- **last_change**: la data informativa dell'ultima modifica, in formato ISO 8601 ;
- **min_x, min_y, max_x e max_y**: le estensioni spaziali del contenuto. ;
- **srs_id**: sistema di riferimento spaziale .

#### gpkg_spatial_ref_sys
Per contenuto di riferimento spaziale; inclusi, a titolo esemplificativo ma non esaustivo, riquadri e funzionalità, ogni riga del contenuto deve fare riferimento a un sistema di riferimento di coordinate; memorizzato nella tabella **gpkg_spatial_ref_sys**. Le colonne obbligatorie in questa tabella sono:

- **srs_name, description**: un nome leggibile e una descrizione per l'SRS;
- **srs_id**: un identificatore univoco per l'SRS; anche la chiave primaria per la tabella;
- **organizzazione**: nome senza distinzione tra maiuscole e minuscole dell'organizzazione di definizione.
- **organization_coordsys_id**: ID numerico dell'SRS assegnato dall'organizzazione;
- **definizione**: definizione del testo noto dell'SRS.


## Riferimenti

* [GeoPackage - di Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Guida introduttiva a GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

