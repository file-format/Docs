{
  "date" : "2019-10-11",
  "keywords" :["ملف mpkg" , "تنسيق ملف mpkg" , "ما هو ملف mpkg" , "ملف" , "مثال mpkg" , "امتداد ملف mpkg" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف MPKG - ملف حزمة التعريف" ,
  "description":"تعرف على تنسيق ملف MPKG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MPKG وفتحها." ,
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-02"
}

## ما هو ملف MPKG؟

الملف ذو الامتداد .mpkg هو ملف مثبت أرشيف ، يوجد غالبًا في أنظمة تشغيل MacOS. يحتوي على جميع ملفات التثبيت المطلوبة للتطبيق دون الحاجة إلى الاحتفاظ بالملفات المرتبطة بشكل منفصل. يمكن أن يحتوي ملف MPKG واحد على ملفات حزمة [PKG] (/ar/ compression / pkg /) كأحد ملفات التثبيت بالإضافة إلى ملفات أخرى. لا يمكن فتح ملفات MPKG باستخدام أي برنامج عام ويتم تنفيذها تلقائيًا على نظام MacOS باستخدام مثبت Apple.

## تنسيق ملف MPKG

يحتوي ملف MPKG على أنواع مختلفة من الملفات المطلوبة لتثبيت الحزم المتعددة التي يحتوي عليها. يمكن رؤية هذا من الصورة أدناه والتي هي هيكل شجرة لعينة ملف MPKG. يتم تصدير هيكل الشجرة هذا باستخدام أمر "الشجرة" على محطة MacOS.

{{< figure src="../mpkg.png" alt="تنسيق ملف MPKG" >}}

فيما يلي وصف العناصر المختلفة في الصورة.

"دليل الحزم" - يخزن قائمة بملفات pkg ، أي قائمة الحزم الفرعية
"دليل الموارد" - يخزن الموارد المستخدمة بواسطة pkg ، مثل الموارد والصور المترجمة ومستندات Rtf ومستندات pdf وما إلى ذلك.
"ملف التوزيع" - مستند xml يحتوي على معلومات مثل الحزم الفرعية التي سيتم تثبيتها والبرامج النصية الخاصة بوقت التشغيل

يمكن أن يبدو ملف XML النموذجي لملف MPKG على النحو التالي اعتمادًا على الحزم الفرعية المرتبطة.

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
  if(!(/ar/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
"app.pkg" - الحزمة الفرعية المراد تثبيتها. إنه دليل لهيكل الحزمة بتنسيق pkg. يحتوي على دليل فرعي للمحتويات.

## مراجع

* [حزم OSX المسطحة] (https://matthew-brett.github.io/docosx/flat_packages.html)
* [مدير حزم C ++ MPKG] (https://github.com/puellavulnerata/mpkg)

