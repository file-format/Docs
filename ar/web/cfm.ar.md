{
  "date" : "2021-07-13",
  "keywords" :["CFM", "extension", "file", "format", "system", "Cold Fusion Markup Language", "language", "CFM web pages", "CFML engine", "CFML"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup" ,
  "description":"تعرف على تنسيق ملف CFM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CFM وفتحها." ,
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-07-13"
}

## ما هو ملف CFM؟ ##

تحتوي صفحات الويب والملفات المستخدمة في ** Cold Fusion Markup Language ** على امتدادات CFM وتسمى صفحات الويب CFM. تعمل لغة البرمجة النصية لتطوير الويب على Google App Engine و .NET framework و JVM. يمكن أن تحتوي على لغة برمجة أو رمز للغة. عندما يتم الوصول إلى أي من صفحاته بواسطة المستخدم ، يقوم خادم الويب الخاص بـ ColdFusion بتنفيذها. CFScript (القريبة من JavaScript) أو يمكن استخدام العلامات لكتابة CFML. يمكن استخدام CFML لإنشاء لغات أخرى بخلاف [HTML](/ar/ web / html /) مثل [CSS](/ar/ web / css /) و [JavaScript](/ar/ web / js /) و [XML](/ar/ web / xml /) والمزيد.

يتم استخدام هذه اللغة والعلامات التي تدعمها في الغالب في تطوير تطبيقات الويب الديناميكية.يمكن تشغيل الملفات مباشرة في المتصفح عبر الإنترنت في حالة حدوث أي خطأ أثناء الاستخدام دون اتصال لمنصة تطوير التطبيق.
 

يعمل CFML بطريقة يتم فيها إعطاء امتدادات ملفات خادم معينة (.cfc ، .cfm) للمعالجة إلى محرك CFML. إذا كانت المحركات تعتمد على Java ، فسيتم تحقيق ذلك باستخدام Java servlets. يقوم محرك CFML بمعالجة الوظائف والعلامات فقط ويعيد الوظائف والنصوص الموجودة خارج علامات CFML إلى خادم الويب دون أي تغيير.


## نبذة تاريخية ##

في عام 1995 ، تم إنشاؤه لأول مرة من قبل شركة تدعى Allaire. في عام 2005 استحوذت عليها Adobe ولا تزال تقدم خدمات لتطوير ColdFusion حتى الآن. بمرور السنين ، تم تطويره وترقيته من قبل العديد من الأشخاص والشركات. في عام 2012 ، تم إطلاق مؤسسة تسمى OpenCFML. في وقت لاحق ، في عام 2015 ، قدم Railo السابق خدماته لتحسين أداء CFM وجعل الموارد أقل من أجل وظائف أفضل. تم إطلاق آخر تحديث له في عام 2020 والذي تم الإعلان عن استمراره حتى عام 2028.

## تنسيق ملف CFM ##

يتكون رمز ملفات CFM وصفحات الويب في الغالب من علامات مثل HTML ولكن مع اختلاف طفيف. هذه الملفات مسؤولة عن تنفيذ العمليات المختلفة التي تمكّن البرامج النصية لـ ColdFusion من تشغيلها.
* يمكن الوصول إلى هذه الملفات وتشغيلها مباشرة على كل من Windows و macOS باستخدام متصفح أي نظام تشغيل.
* يوفر Adobe ColdFusion النظام الأساسي لتطوير صفحات الويب والتطبيقات الديناميكية على جهاز الكمبيوتر.
* يمكن استخدام أي محرر نصوص مثل NotePad أو أي محرر نصوص آخر في نظام التشغيل لفتح هذه الملفات لأن هذه الملفات تستند إلى نص.
* عندما يتم فتح أي ملف CFM في محرر نصوص ، فإنه يعرض رمزًا يتكون من العلامات والنصوص التي لن يفهمها المرء إلا إذا كان مطور ويب.

## مثال على استخدام CFM ##

يوضح ما يلي مثال استخدام بسيط لملف CFM.

### مستند CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## مراجع ##

- [CFM - ويكيبيديا](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

