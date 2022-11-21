{
  "date" : "2021-06-29",
  "keywords" :["CPL" , "extension" , "ملف" , "تنسيق" , "نظام" , "ملف لوحة التحكم" , "Windows" , "برامج" , "كمبيوتر" , "تطبيق"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - ملف لوحة التحكم" ,
  "description":"تعرف على تنسيق ملف CPL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CPL وفتحها." ,
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-06-29"
}

## ما هو ملف CPL؟ ##

ملف CPL هو نوع من ملفات "النظام". يتم استخدامه بواسطة نظام التشغيل Windows. ملف CPL هو اختصار لملف لوحة التحكم. هذه الملفات هي ملفات ثنائية يتم فتحها باستخدام لوحة التحكم في نظام تشغيل Microsoft Windows وتستخدم لتمثيل وفتح الأدوات المتوفرة في لوحة التحكم ، مثل الماوس والشاشات والشبكات وغيرها. عادةً ما يتم تخزين ملفات CPL في مجلد النظام على جهازك. لا ينبغي فتح هذه الملفات يدويًا.


## تنسيق ملف CPL ##

يتم توصيل ملفات CPL المختلفة في نظام التشغيل Windows الخاص بك لتمثيل عناصر لوحة التحكم المختلفة. جميع عناصر لوحة التحكم مرتبطة بملف CPL ولها اللاحقة ".cpl" مرفقة بعناصرها.

بعض الأنواع الشائعة من ملفات CPL بتنسيقاتها هي:

* Inetcpl.cpl - لخصائص الإنترنت على جهازك
* Appwiz.cpl - لإضافة أو إزالة خصائص البرامج على جهازك
* Desk.cpl - لعرض خصائص
* Main.cpl - للخصائص المتعلقة بالماوس والخطوط ولوحة المفاتيح والطابعات.
* Netcpl.cpl - للخصائص ذات الصلة بالشبكة
* System.cpl - للخصائص ذات الصلة بالنظام ولإضافة معالج جديد للأجهزة
* TimeDate.cpl - لخصائص التاريخ أو الوقت
* Mlcfg32.cpl - لخصائص Microsoft Exchange أو Windows Messaging
* Intl.cpl - هذا يخص خصائص الإعدادات الإقليمية
* Modem.cpl - للخصائص ذات الصلة بالمودم
* Themes.cpl - يخزن سمات وخصائص سطح المكتب.
* Password.cpl - للحصول على خصائص كلمة المرور
* Mmsys.cpl - لخصائص الوسائط المتعددة
* Wgpocpl.cpl - يخص Microsoft Mail Post Office

## نبذة تاريخية ##

تم تطوير نوع ملف CPL بواسطة Microsoft Windows وهو جزء لا يتجزأ من نظام التشغيل Windows منذ Windows 1.0. لا يزال قيد الاستخدام في جميع إصدارات Windows ، ويتم تخزين جميع خصائص عنصر لوحة التحكم باستخدام نوع الملف هذا.

## مثال CPL ##

يمكن الاطلاع على نموذج ملف CPL أدناه:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
