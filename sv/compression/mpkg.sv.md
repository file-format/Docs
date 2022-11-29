{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg fil", "mpkg filformat", "vad är en mpkg fil", "fil", "mpkg exempel", "mpkg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG-filformat - metapaketfil",
  "description":"Läs mer om MPKG-filformat och API:er som kan skapa och öppna MPKG-filer.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Vad är en MPKG fil?

En fil med filtillägget .mpkg är en arkivinstallationsfil, som oftast finns på MacOS-operativsystem. Den innehåller alla nödvändiga installationsfiler för applikationen utan att behöva hålla tillhörande filer separat. En enskild MPKG-fil kan innehålla paketfiler [PKG](/sv/compression/pkg/) som en av installationsfilerna förutom andra filer. MPKG-filer kan inte öppnas med någon allmän programvara och körs automatiskt på MacOS med Apple Installer.

## MPKG filformat

En MPKG-fil innehåller olika typer av filer som krävs för installation av flera paket den innehåller. Detta kan ses från bilden nedan som är trädstrukturen för en exempel-MPKG-fil. Denna trädstruktur exporteras med kommandot `tree` på MacOS-terminalen.

{{< figure src="../mpkg.png" alt="MPKG filformat" >}}

Beskrivningen av olika element i bilden är som följer.

`Packages Directory` - lagrar en lista med pkg-filer, det vill säga en lista över underpaket
`Resurskatalog` - lagrar resurser som används av pkg, såsom lokaliserade resurser och bilder, Rtf-dokument, pdf-dokument, etc.
`Distribution.dist-fil` - Ett xml-dokument som innehåller information såsom underpaket som ska installeras och runtime-skript

Exempel på XML-fil för en MPKG-fil kan se ut som följer beroende på de associerade underpaketen.

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
  if(!(/sv/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - är underpaketet som ska installeras. Det är en katalog över Bundle-strukturen i pkg-format. Den innehåller en underkatalog för innehåll.

## Referenser

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

