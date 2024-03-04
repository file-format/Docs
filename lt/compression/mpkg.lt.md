{
  "date": "2019-10-11",
  "keywords": [
"mpkg failą",
"mpkg failo formatas",
"kas yra mpkg failas",
"failą",
"mpkg pavyzdys",
"mpkg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPKG failo formatas – meta paketo failas",
  "description": "Sužinokite apie MPKG failo formatą ir API, kurios gali kurti ir atidaryti MPKG failus.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-ltg"
}
},
  "lastmod": "2021-04-02"
}

## Kas yra MPKG failas?

Failas su plėtiniu .mpkg yra archyvo diegimo failas, dažniausiai randamas MacOS operacinėse sistemose. Jame yra visi reikalingi programos diegimo failai ir nereikia laikyti susijusių failų atskirai. Viename MPKG faile, be kitų failų, gali būti paketo failų [PKG](/compression/pkg/) kaip vieną iš diegimo failų. MPKG failų negalima atidaryti naudojant jokią bendrą programinę įrangą ir jie automatiškai vykdomi MacOS naudojant Apple Installer.

## MPKG failo formatas

MPKG faile yra įvairių tipų failai, kurių reikia norint įdiegti kelis jame esančius paketus. Tai matyti iš žemiau esančio paveikslėlio, kuriame yra pavyzdinio MPKG failo medžio struktūra. Ši medžio struktūra eksportuojama naudojant tree komandą MacOS terminale.

{{< figure src="../mpkg.png" alt="MPKG failo formatas" >}}

The description of different elements in the image is as follow.

Paketų katalogas - saugo pkg failų sąrašą, tai yra antrinių paketų sąrašą
Išteklių katalogas – saugo pkg naudojamus išteklius, tokius kaip lokalizuoti ištekliai ir vaizdai, Rtf dokumentai, pdf dokumentai ir kt.
Distribution.dist failas – XML dokumentas, kuriame yra informacijos, pvz., antrinių paketų, kuriuos reikia įdiegti, ir vykdymo scenarijus

Pavyzdinis MPKG failo XML failas gali atrodyti taip, atsižvelgiant į susijusius antrinius paketus.

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
app.pkg – tai antrinis paketas, kurį reikia įdiegti. Tai yra paketo struktūros katalogas pkg formatu. Jame yra turinio pakatalogis.

## Nuorodos

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG paketų tvarkyklė](https://github.com/puellavulnerata/mpkg)


