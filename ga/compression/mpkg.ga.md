{
  "date": "2019-10-11",
  "keywords": [
"comhad mpkg",
"Formáid comhaid mpkg",
"Cad is comhad mpkg ann",
"comhad",
"sampla mpkg",
"Síneadh comhad mpkg",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid MPKG - Comhad Pacáiste Meta",
  "description": "Foghlaim faoi fhormáid comhaid MPKG agus APIs ar féidir leo comhaid MPKG a chruthú agus a oscailt.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-gag"
}
},
  "lastmod": "2021-04-02"
}

## Cad is comhad MPKG ann?

Is comhad suiteálaí cartlainne é comhad le síneadh .mpkg, a fhaightear go príomha ar Chórais Oibriúcháin MacOS. Tá gach comhad suiteála riachtanach den fheidhmchlár ann gan aon ghá le comhaid ghaolmhara a choinneáil ar leithligh. Is féidir comhaid phacáiste [PKG](/compression/pkg/) a bheith i gcomhad MPKG amháin mar cheann de na comhaid suiteála chomh maith le comhaid eile. Ní féidir comhaid MPKG a oscailt le haon bhogearraí ginearálta agus déantar iad a fhorghníomhú go huathoibríoch ar MacOS ag baint úsáide as Apple Installer.

## Formáid Chomhaid MPKG

Tá cineálacha éagsúla comhad i gcomhad MPKG atá riachtanach chun pacáistí iolracha atá ann a shuiteáil. Is féidir é seo a fheiceáil ón íomhá thíos arb é an struchtúr crann atá i gcomhad samplach MPKG. Easpórtáiltear an struchtúr crann seo trí úsáid a bhaint as ordú `tree` ar teirminéal MacOS.

{{< figure src="../mpkg.png" alt="Formáid Chomhaid MPKG" >}}

The description of different elements in the image is as follow.

Stórálann `Eolaire Pacáistí` - liosta de chomhaid pkg, is é sin, liosta fo-Phacáistí
`Eolaire Acmhainní` - stórálann sé acmhainní a úsáideann pkg, mar acmhainní agus íomhánna logánta, doiciméid Rtf, doiciméid pdf, etc.
`Comhad Distribution.dist` - Doiciméad xml ina bhfuil faisnéis ar nós fophacáistí le suiteáil agus scripteanna ama rite

Is féidir breathnú mar seo a leanas ar chomhad samplach XML do chomhad MPKG ag brath ar na fo-phacáistí gaolmhara.

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
Is é `app.pkg` - an fo-phacáiste atá le suiteáil. Is eolaire é den struchtúr Beart i bhformáid pkg. Tá fochomhadlann Ábhar ann.

## Tagairtí

* [Pacáistí Comhréidh OSX](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ Bainisteoir Pacáiste MPKG](https://github.com/puellavulnerata/mpkg)


