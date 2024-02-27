{
  "date": "2019-10-11",
  "keywords": [
"mpkg fil",
"mpkg filformat",
"hvad er en mpkg-fil",
"fil",
"mpkg eksempel",
"mpkg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPKG-filformat - Meta-pakkefil",
  "description": "Lær om MPKG-filformat og API'er, der kan oprette og åbne MPKG-filer.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-dag"
}
},
  "lastmod": "2021-04-02"
}

## Hvad er MPKG fil?

En fil med filtypenavnet .mpkg er en arkivinstallationsfil, der for det meste findes på MacOS-operativsystemer. Den indeholder alle nødvendige installationsfiler af applikationen uden behov for at opbevare tilknyttede filer separat. En enkelt MPKG-fil kan indeholde pakkefiler [PKG](/compression/pkg/) som en af installationsfilerne ud over andre filer. MPKG-filer kan ikke åbnes med nogen generel software og udføres automatisk på MacOS ved hjælp af Apple Installer.

## MPKG filformat

En MPKG-fil indeholder forskellige typer filer, der er nødvendige for installationen af flere pakker, den indeholder. Dette kan ses fra billedet nedenfor, som er træstrukturen af en prøve MPKG-fil. Denne træstruktur eksporteres ved hjælp af 'træ'-kommandoen på MacOS-terminalen.

{{< figure src="../mpkg.png" alt="MPKG filformat" >}}

The description of different elements in the image is as follow.

`Packages Directory` - gemmer en liste over pkg-filer, det vil sige en liste over underpakker
`Resource Directory` - gemmer ressourcer brugt af pkg, såsom lokaliserede ressourcer og billeder, Rtf-dokumenter, pdf-dokumenter osv.
`Distribution.dist-fil` - Et xml-dokument, der indeholder oplysninger såsom underpakker, der skal installeres, og runtime-scripts

Eksempel på XML-fil for en MPKG-fil kan se ud som følger afhængigt af de tilknyttede underpakker.

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
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - er underpakken, der skal installeres. Det er en mappe med pakkestrukturen i pkg-format. Den indeholder en undermappe Indhold.

## Referencer

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)


