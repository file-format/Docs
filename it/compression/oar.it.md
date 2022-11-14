{
  "date" : "2021-04-08",
  "keywords" :[ "file remo", "formato file remo", "cos'è un file remo", "file", "esempio remo", "estensione file remo", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Formato file archivio OpenSimulator",
  "description":"Scopri il formato di file OAR e le API che possono creare e aprire file OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Che cos'è un file OAR?

Un file con estensione .oar è un file di archivio utilizzato dall'applicazione OpenSimulator, che è un server di applicazioni 3D open source per creare un ambiente virtuale accessibile a più utenti sulla rete. Il formato file OAR fornisce i dati delle risorse necessari per caricare completamente il terreno, le trame degli oggetti e gli inventari su un sistema diverso. OpenSimulator ha anche un'hypergrid opzionale che consente agli utenti di visitare altre installazioni di OpenSimulator sul Web. I file OAR hanno un'applicazione/remo di tipo MIME Internet e contengono uno o più file archiviati.


## Formato file OAR

OAR sono file binari archiviati in un formato di file di archivio compresso. L'ultima versione del formato file OAR è la [versione 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) che presenta importanti modifiche rispetto alla precedente [versione 0.8](http://opensimulator.org/wiki/OAR_Format_0 .8). L'ultima versione supporta l'archiviazione di più regioni in un unico OAR e non è retrocompatibile con le versioni di OpenSimulator precedenti alla 0.7.5. Un file OAR è un file tar compresso con gzip (tar.gz) nel formato tar unix originale (non USTAR).

## Esempio di regioni OAR
I file AOR possono contenere più regioni. La struttura dell'archivio è la seguente (questo esempio contiene 4 regioni):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Il file di controllo dell'archivio contiene un numero di versione principale per definire la compatibilità con future modifiche al formato. La presenza di asset in formato OAR è indicata dall'elemento booleano<assets_included> . Le informazioni sulle regioni incluse sono contenute in un manifest presente nel file di controllo. Un esempio di Archive.xml è il seguente.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Riferimenti

* [Formato OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

