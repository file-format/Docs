{
  "date" : "2019-10-11",
  "keywords" :[ "file mpkg", "formato file mpkg", "cos'è un file mpkg", "file", "esempio mpkg", "estensione file mpkg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MPKG - File meta pacchetto",
  "description":"Scopri il formato di file MPKG e le API che possono creare e aprire file MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Che cos'è un file MPKG?

Un file con estensione .mpkg è un file di installazione di archivio, che si trova principalmente sui sistemi operativi MacOS. Contiene tutti i file di installazione richiesti dell'applicazione senza la necessità di conservare i file associati separatamente. Un singolo file MPKG può contenere file di pacchetto [PKG](/it/compression/pkg/) come uno dei file di installazione oltre ad altri file. I file MPKG non possono essere aperti con nessun software generale e vengono eseguiti automaticamente su MacOS utilizzando Apple Installer.

## Formato file MPKG

Un file MPKG contiene diversi tipi di file necessari per l'installazione di più pacchetti in esso contenuti. Questo può essere visto dall'immagine sottostante che è la struttura ad albero di un file MPKG di esempio. Questa struttura ad albero viene esportata usando il comando `tree` sul terminale MacOS.

{{< figure src="../mpkg.png" alt="Formato file MPKG" >}}

La descrizione dei diversi elementi nell'immagine è la seguente.

`Directory dei pacchetti` - memorizza un elenco di file pkg, ovvero un elenco di sottopacchetti
`Resources Directory` - memorizza le risorse utilizzate da pkg, come risorse e immagini localizzate, documenti Rtf, documenti pdf, ecc.
`File Distribution.dist` - Un documento xml contenente informazioni come pacchetti secondari da installare e script di runtime

Il file XML di esempio per un file MPKG può apparire come segue a seconda dei sottopacchetti associati.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/it/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - è il sottopacchetto da installare. È una directory della struttura Bundle in formato pkg. Contiene una sottodirectory Contents.

## Riferimenti

* [Pacchetti OSX Flat](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Gestione pacchetti C++ MPKG](https://github.com/puellavulnerata/mpkg)

