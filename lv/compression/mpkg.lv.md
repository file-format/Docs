{
  "date": "2019-10-11",
  "keywords": [
"mpkg failu",
"mpkg faila formātā",
"kas ir mpkg fails",
"failu",
"mpkg piemērs",
"mpkg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPKG faila formāts — meta pakotnes fails",
  "description": "Uzziniet par MPKG faila formātu un API, kas var izveidot un atvērt MPKG failus.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-lvg"
}
},
  "lastmod": "2021-04-02"
}

## Kas ir MPKG fails?

Fails ar paplašinājumu .mpkg ir arhīva instalēšanas fails, kas galvenokārt atrodams MacOS operētājsistēmās. Tajā ir visi nepieciešamie lietojumprogrammas instalācijas faili, bez nepieciešamības glabāt saistītos failus atsevišķi. Atsevišķs MPKG fails var saturēt pakotnes failus [PKG](/compression/pkg/) kā vienu no instalācijas failiem papildus citiem failiem. MPKG failus nevar atvērt ar vispārēju programmatūru, un tie tiek automātiski izpildīti operētājsistēmā MacOS, izmantojot Apple Installer.

## MPKG faila formāts

MPKG fails satur dažāda veida failus, kas nepieciešami vairāku tajā ietverto pakotņu instalēšanai. To var redzēt zemāk esošajā attēlā, kas ir MPKG faila parauga koka struktūra. Šī koka struktūra tiek eksportēta, izmantojot MacOS termināļa komandu tree.

{{< figure src="../mpkg.png" alt="MPKG faila formāts" >}}

The description of different elements in the image is as follow.

Pakešu direktorijs - saglabā pkg failu sarakstu, tas ir, apakšpakešu sarakstu
`Resursu direktorijs` - glabā pkg izmantotos resursus, piemēram, lokalizētos resursus un attēlus, Rtf dokumentus, pdf dokumentus utt.
Distribution.dist fails — XML dokuments, kurā ir informācija, piemēram, instalējamās apakšpakotnes un izpildlaika skripti.

XML faila paraugs MPKG failam var izskatīties šādi atkarībā no saistītajām apakšpaketēm.

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
`app.pkg' — ir instalējamā apakšpakotne. Tas ir paketes struktūras direktorijs pkg formātā. Tas satur apakšdirektoriju Saturs.

## Atsauces

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG pakotņu pārvaldnieks](https://github.com/puellavulnerata/mpkg)


