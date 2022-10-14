{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg-Datei", "mpkg-Dateiformat", "was ist eine mpkg-Datei", "Datei", "mpkg-Beispiel", "mpkg-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG-Dateiformat - Metapaketdatei",
  "description":"Erfahren Sie mehr über das MPKG-Dateiformat und APIs, die MPKG-Dateien erstellen und öffnen können.",
  "linktitle" :"MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Was ist eine MPKG-Datei?

Eine Datei mit der Erweiterung .mpkg ist eine Archivinstallationsdatei, die hauptsächlich auf MacOS-Betriebssystemen zu finden ist. Es enthält alle erforderlichen Installationsdateien der Anwendung, ohne dass zugehörige Dateien separat aufbewahrt werden müssen. Eine einzelne MPKG-Datei kann Paketdateien [PKG](/de/compression/pkg/) als eine der Installationsdateien zusätzlich zu anderen Dateien enthalten. MPKG-Dateien können nicht mit allgemeiner Software geöffnet werden und werden unter MacOS automatisch mit Apple Installer ausgeführt.

## MPKG-Dateiformat

Eine MPKG-Datei enthält verschiedene Dateitypen, die für die Installation mehrerer darin enthaltener Pakete erforderlich sind. Dies ist aus dem Bild unten ersichtlich, das die Baumstruktur einer Beispiel-MPKG-Datei darstellt. Diese Baumstruktur wird mit dem Befehl „tree“ auf dem MacOS-Terminal exportiert.

{{< figure src="../mpkg.png" alt="MPKG-Dateiformat" >}}

Die Beschreibung der verschiedenen Elemente im Bild ist wie folgt.

„Packages Directory“ – speichert eine Liste von pkg-Dateien, d. h. eine Liste von Unterpaketen
„Ressourcenverzeichnis“ – speichert von pkg verwendete Ressourcen wie lokalisierte Ressourcen und Bilder, RTF-Dokumente, PDF-Dokumente usw.
Datei „Distribution.dist“ – Ein XML-Dokument, das Informationen wie zu installierende Unterpakete und Laufzeitskripte enthält

Eine Beispiel-XML-Datei für eine MPKG-Datei kann abhängig von den zugehörigen Unterpaketen wie folgt aussehen.

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
  if(!(/de/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - ist das zu installierende Unterpaket. Es ist ein Verzeichnis der Bundle-Struktur im pkg-Format. Es enthält ein Unterverzeichnis Contents.

## Verweise

* [OSX-Flat-Pakete](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG-Paketmanager](https://github.com/puellavulnerata/mpkg)

