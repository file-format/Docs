{
  "date" : "2019-10-11",
  "keywords" :[ "soubor mpkg", "formát souboru mpkg", "co je soubor mpkg", "soubor", "příklad mpkg", "přípona souboru mpkg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MPKG - soubor balíčku meta",
  "description":"Další informace o formátu souborů MPKG a rozhraních API, která mohou vytvářet a otevírat soubory MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Co je soubor MPKG?

Soubor s příponou .mpkg je archivní instalační soubor, který se většinou nachází v operačních systémech MacOS. Obsahuje všechny požadované instalační soubory aplikace bez nutnosti uchovávat související soubory samostatně. Jeden soubor MPKG může kromě jiných souborů obsahovat soubory balíčku [PKG](/cs/compression/pkg/) jako jeden z instalačních souborů. Soubory MPKG nelze otevřít žádným obecným softwarem a na MacOS se spouštějí automaticky pomocí Apple Installer.

## Formát souboru MPKG

Soubor MPKG obsahuje různé typy souborů, které jsou nutné pro instalaci více balíčků, které obsahuje. To je patrné z obrázku níže, na kterém je stromová struktura ukázkového souboru MPKG. Tato stromová struktura je exportována pomocí příkazu `tree` na terminálu MacOS.

{{< figure src="../mpkg.png" alt="Formát souboru MPKG" >}}

Popis různých prvků na obrázku je následující.

`Packages Directory` - ukládá seznam souborů pkg, tedy seznam dílčích balíčků
`Resources Directory` – ukládá zdroje používané pkg, jako jsou lokalizované zdroje a obrázky, Rtf dokumenty, pdf dokumenty atd.
`Soubor Distribution.dist` – XML dokument obsahující informace, jako jsou dílčí balíčky, které mají být nainstalovány, a runtime skripty

Vzorový soubor XML pro soubor MPKG může vypadat následovně v závislosti na přidružených dílčích balíčcích.

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
  if(!(/cs/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - je dílčí balíček, který se má nainstalovat. Je to adresář struktury Bundle ve formátu pkg. Obsahuje podadresář Contents.

## Reference

* [Ploché balíčky OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

