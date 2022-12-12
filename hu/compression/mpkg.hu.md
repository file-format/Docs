{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg fájl", "mpkg fájl formátum", "mi az mpkg fájl", "fájl", "mpkg példa", "mpkg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG fájlformátum - meta csomagfájl",
  "description":"További információ az MPKG fájlformátumról és az MPKG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Mi az MPKG fájl?

Az .mpkg kiterjesztésű fájl egy archív telepítőfájl, amely többnyire MacOS operációs rendszereken található. Tartalmazza az alkalmazás összes szükséges telepítőfájlját anélkül, hogy a kapcsolódó fájlokat külön kellene tárolni. Egyetlen MPKG-fájl más fájlok mellett a [PKG](/hu/compression/pkg/) csomagfájlokat is tartalmazhatja a telepítőfájlok egyikeként. Az MPKG fájlok nem nyithatók meg semmilyen általános szoftverrel, és automatikusan végrehajtódnak MacOS rendszeren az Apple Installer segítségével.

## MPKG fájl formátum

Egy MPKG-fájl különböző típusú fájlokat tartalmaz, amelyek a benne lévő több csomag telepítéséhez szükségesek. Ez látható az alábbi képen, amely egy minta MPKG fájl fastruktúrája. Ez a fastruktúra a MacOS terminálon található "tree" paranccsal kerül exportálásra.

{{< figure src="../mpkg.png" alt="MPKG fájlformátum" >}}

A képen látható különböző elemek leírása a következő.

"Csomagok könyvtára" - a pkg fájlok listáját tárolja, vagyis az alcsomagok listáját
"Erőforrások könyvtára" - a pkg által használt erőforrásokat tárolja, például lokalizált erőforrásokat és képeket, Rtf dokumentumokat, pdf dokumentumokat stb.
"Distribution.dist fájl" – olyan információkat tartalmazó xml-dokumentum, mint a telepítendő alcsomagok és a futásidejű szkriptek

Az MPKG-fájl XML-mintája a következőképpen nézhet ki a kapcsolódó alcsomagoktól függően.

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
  if(!(/hu/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
"app.pkg" - a telepítendő alcsomag. Ez a Bundle szerkezet könyvtára pkg formátumban. Tartalmaz egy Tartalom alkönyvtárat.

## Hivatkozások

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

