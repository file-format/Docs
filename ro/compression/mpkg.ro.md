{
  "date" : "2019-10-11",
  "keywords" :[ "fișier mpkg", "format fișier mpkg", "ce este un fișier mpkg", "fișier", "exemplu mpkg", "extensie fișier mpkg", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier MPKG - fișier meta pachet",
  "description":"Aflați despre formatul de fișier MPKG și despre API-urile care pot crea și deschide fișiere MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Ce este un fișier MPKG?

Un fișier cu extensia .mpkg este un fișier de instalare a arhivei, care se găsește mai ales pe sistemele de operare MacOS. Conține toate fișierele de instalare necesare ale aplicației fără a fi nevoie să păstrați separat fișierele asociate. Un singur fișier MPKG poate conține fișiere pachet [PKG](/ro/compression/pkg/) ca unul dintre fișierele de instalare în plus față de alte fișiere. Fișierele MPKG nu pot fi deschise cu niciun software general și sunt executate automat pe MacOS utilizând Apple Installer.

## Format de fișier MPKG

Un fișier MPKG conține diferite tipuri de fișiere care sunt necesare pentru instalarea mai multor pachete pe care le conține. Acest lucru poate fi văzut din imaginea de mai jos, care este structura arborescentă a unui exemplu de fișier MPKG. Această structură arborescentă este exportată utilizând comanda `tree` pe terminalul MacOS.

{{< figure src="../mpkg.png" alt="Format de fișier MPKG" >}}

Descrierea diferitelor elemente din imagine este următoarea.

`Packages Directory` - stochează o listă de fișiere pkg, adică o listă de sub-pachete
`Resources Directory` - stochează resursele utilizate de pkg, cum ar fi resurse și imagini localizate, documente Rtf, documente pdf etc.
`Fișier Distribution.dist` - Un document xml care conține informații precum sub-pachetele de instalat și scripturi de rulare

Exemplul de fișier XML pentru un fișier MPKG poate arăta după cum urmează, în funcție de sub-pachetele asociate.

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
  if(!(/ro/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - este subpachetul care trebuie instalat. Este un director al structurii Bundle în format pkg. Conține un subdirector Conținut.

## Referințe

* [Pachete plate OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Manager de pachete C++ MPKG](https://github.com/puellavulnerata/mpkg)

