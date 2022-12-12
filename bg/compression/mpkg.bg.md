{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg файл", "mpkg файлов формат", "какво е mpkg файл", "файл", "mpkg пример", "mpkg файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат MPKG – файл с мета пакет",
  "description":"Научете за файловия формат MPKG и API, които могат да създават и отварят MPKG файлове.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Какво е MPKG файл?

Файл с разширение .mpkg е архивен инсталационен файл, намиращ се най-вече в операционни системи MacOS. Той съдържа всички необходими инсталационни файлове на приложението, без да е необходимо да съхранявате свързаните файлове отделно. Един MPKG файл може да съдържа пакетни файлове [PKG](/bg/compression/pkg/) като един от инсталационните файлове в допълнение към други файлове. MPKG файловете не могат да се отварят с общ софтуер и се изпълняват автоматично на MacOS с помощта на Apple Installer.

## MPKG файлов формат

Един MPKG файл съдържа различни типове файлове, които са необходими за инсталирането на множество пакети, които съдържа. Това може да се види от изображението по-долу, което е дървовидната структура на примерен MPKG файл. Тази дървовидна структура се експортира с помощта на командата `tree` на MacOS терминал.

{{< figure src="../mpkg.png" alt="MPKG файлов формат" >}}

Описанието на различните елементи в изображението е както следва.

`Пакетна директория` - съхранява списък с pkg файлове, т.е. списък с под-пакети
`Директория с ресурси` - съхранява ресурси, използвани от pkg, като локализирани ресурси и изображения, Rtf документи, pdf документи и др.
„Файл Distribution.dist“ – xml документ, съдържащ информация като подпакети за инсталиране и скриптове по време на изпълнение

Примерен XML файл за MPKG файл може да изглежда както следва в зависимост от свързаните подпакети.

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
  if(!(/bg/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - е подпакетът, който ще се инсталира. Това е директория на структурата на Bundle във формат pkg. Съдържа поддиректория Съдържание.

## Препратки

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

