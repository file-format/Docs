{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg-bestand", "mpkg-bestandsformaat", "wat is een mpkg-bestand", "bestand", "mpkg-voorbeeld", "mpkg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG-bestandsindeling - Metapakketbestand",
  "description":"Meer informatie over de MPKG-bestandsindeling en API's die MPKG-bestanden kunnen maken en openen.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Wat is een MPKG-bestand?

Een bestand met de extensie .mpkg is een archiefinstallatiebestand, dat meestal wordt aangetroffen op MacOS-besturingssystemen. Het bevat alle vereiste installatiebestanden van de applicatie zonder dat de bijbehorende bestanden apart hoeven te worden bewaard. Een enkel MPKG-bestand kan naast andere bestanden ook pakketbestanden [PKG](/nl/compression/pkg/) als een van de installatiebestanden bevatten. MPKG-bestanden kunnen niet worden geopend met algemene software en worden automatisch uitgevoerd op MacOS met Apple Installer.

## MPKG-bestandsindeling

Een MPKG-bestand bevat verschillende soorten bestanden die nodig zijn voor de installatie van meerdere pakketten die het bevat. Dit is te zien aan de onderstaande afbeelding, die de boomstructuur is van een voorbeeld van een MPKG-bestand. Deze boomstructuur wordt geëxporteerd met het commando `tree` op de MacOS-terminal.

{{< figure src="../mpkg.png" alt="MPKG-bestandsindeling" >}}

De beschrijving van de verschillende elementen in de afbeelding is als volgt.

`Pakkettenmap` - slaat een lijst met pkg-bestanden op, dat wil zeggen een lijst met subpakketten
`Resources Directory` - slaat bronnen op die door pkg worden gebruikt, zoals gelokaliseerde bronnen en afbeeldingen, Rtf-documenten, pdf-documenten, enz.
`Distribution.dist file` - Een xml-document met informatie zoals te installeren subpakketten en runtime-scripts

Een voorbeeld-XML-bestand voor een MPKG-bestand kan er als volgt uitzien, afhankelijk van de bijbehorende subpakketten.

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
  if(!(/nl/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - is het subpakket dat moet worden geïnstalleerd. Het is een directory van de Bundelstructuur in pkg-formaat. Het bevat een submap Inhoud.

## Referenties

* [OSX platte pakketten](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG-pakketbeheerder](https://github.com/puellavulnerata/mpkg)

