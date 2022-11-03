{
  "date" : "2019-10-11",
  "keywords" :[ "файл mpkg", "формат файла mpkg", "что такое файл mpkg", "файл", "пример mpkg", "расширение файла mpkg", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла MPKG — файл метапакета",
  "description":"Узнайте о формате файла MPKG и API-интерфейсах, которые могут создавать и открывать файлы MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .MPKG вариант №

Файл с расширением .mpkg представляет собой архивный установочный файл, который в основном используется в операционных системах MacOS. Он содержит все необходимые установочные файлы приложения без необходимости хранить связанные файлы отдельно. Один файл MPKG может содержать файлы пакета [PKG](/ru/compression/pkg/) в качестве одного из установочных файлов в дополнение к другим файлам. Файлы MPKG нельзя открыть с помощью какого-либо общего программного обеспечения, и они автоматически запускаются в MacOS с помощью Apple Installer.

## Формат файла MPKG

Файл MPKG содержит файлы различных типов, необходимые для установки нескольких содержащихся в нем пакетов. Это видно из изображения ниже, которое представляет собой древовидную структуру образца файла MPKG. Эта древовидная структура экспортируется с помощью команды `tree` в терминале MacOS.

{{< figure src="../mpkg.png" alt="Формат файла MPKG" >}}

Описание различных элементов изображения выглядит следующим образом.

`Каталог пакетов` - хранит список файлов pkg, то есть список вложенных пакетов.
«Каталог ресурсов» — хранит ресурсы, используемые pkg, такие как локализованные ресурсы и изображения, документы в формате Rtf, документы в формате PDF и т. д.
`Distribution.dist file` — XML-документ, содержащий такую информацию, как устанавливаемые подпакеты и сценарии выполнения.

Пример файла XML для файла MPKG может выглядеть следующим образом в зависимости от связанных подпакетов.

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
  if(!(/ru/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - это подпакет, который нужно установить. Это каталог структуры Bundle в формате pkg. Он содержит подкаталог Contents.

## использованная литература

* [Плоские пакеты OSX] (https://matthew-brett.github.io/docosx/flat_packages.html)
* [Диспетчер пакетов C++ MPKG] (https://github.com/puellavulnerata/mpkg)

