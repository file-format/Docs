{
  "date" : "2019-10-11",
  "keywords" :[ "файл mpkg", "формат файлу mpkg", "що таке файл mpkg", "файл", "приклад mpkg", "розширення файлу mpkg", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу MPKG - файл метапакета",
  "description":"Дізнайтеся про формат файлу MPKG та API, які можуть створювати та відкривати файли MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Що таке файл MPKG?

Файл із розширенням .mpkg — це архівний файл інсталятора, який переважно зустрічається в операційних системах MacOS. Він містить усі необхідні інсталяційні файли програми без необхідності зберігати відповідні файли окремо. Один файл MPKG може містити файли пакетів [PKG](/uk/compression/pkg/) як один із файлів інсталяції на додаток до інших файлів. Файли MPKG не можна відкрити будь-яким загальним програмним забезпеченням і автоматично запускаються в MacOS за допомогою Apple Installer.

## Формат файлу MPKG

Файл MPKG містить різні типи файлів, які потрібні для інсталяції кількох пакетів, які він містить. Це можна побачити на зображенні нижче, яке є деревоподібною структурою зразка файлу MPKG. Ця структура дерева експортується за допомогою команди `tree` на терміналі MacOS.

{{< figure src="../mpkg.png" alt="Формат файлу MPKG" >}}

Опис різних елементів на зображенні такий.

`Каталог пакетів` - зберігає список файлів pkg, тобто список підпакетів
`Каталог ресурсів` - зберігає ресурси, які використовує pkg, наприклад локалізовані ресурси та зображення, документи RTF, PDF документи тощо.
`Файл Distribution.dist` – XML-документ, що містить таку інформацію, як підпакети для встановлення та сценарії виконання

Зразок файлу XML для файлу MPKG може виглядати наступним чином залежно від пов’язаних підпакетів.

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
  if(!(/uk/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - підпакет, який потрібно встановити. Це каталог зі структурою Bundle у форматі pkg. Він містить підкаталог Contents.

## Список літератури

* [Плоскі пакети OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Менеджер пакетів C++ MPKG](https://github.com/puellavulnerata/mpkg)

