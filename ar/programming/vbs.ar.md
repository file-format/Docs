{
  "date" : "2021-08-24", 
  "keywords" :["vbs" , "file" , "extension" , "تنسيق الملف" , "Visual Basic Script" , "Programming Guide" , "vbs example" , "Microsoft Visual Basic" , "VBScript"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - ملف البرنامج النصي Visual Basic" ,
  "description":"تعرف على تنسيق ملف VBS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VBS وفتحها." ,
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-08-24"
}

## ما هو ملف VBS؟

VBS أو VBScript متصل بإصدار البرنامج النصي من Microsoft Visual Basic. في بيئة الحوسبة ، يُسمح للمستخدم بالوصول إلى العديد من جوانبها والتحكم فيها. يُسمح لـ VBScript باستخدام نموذج يسمى ** Component Object Model ** للاستفادة من عناصر وأدوات البيئة. تم تحديد هذه البيئة للعمل وتشغيل VBScript.

إنه يشبه جافا سكريبت عندما يصل إليه العميل في مجال تطوير الويب. يتم استخدامه أيضًا بواسطة الخوادم لمعالجة صفحات الويب. يمكن اعتباره في بعض الأنواع الأخرى من ملفات البرمجة النصية مثل تطبيقات [HTML](/ar/web/html/).


## نبذة تاريخية ##

تم إطلاقه لأول مرة في عام 1996 ، كجزء من التقنيات المستخدمة من قبل Microsoft والمخصصة لنصوص Windows. تم تطويره خصيصًا لمساعدة مطوري الويب في البداية. في نفس العام ، تم إصدار مستكشف Microsoft Windows المسمى Internet Explorer إلى جانب ميزات Visual Basic Script.

مع التقدم في التكنولوجيا وتطوير الويب ، تم إطلاق العديد من إصدارات VBScript جنبًا إلى جنب مع العديد من الميزات المتقدمة. علاوة على ذلك ، في العام المقبل ، ستكون لغة البرمجة النصية هذه جزءًا من Microsoft Windows بميزات جديدة.

## مواصفات تكنيكال ##

بالنسبة لصفحات الويب الموجودة على جانب الخادم ، يتم استخدام أدوات مثل ** صفحات الخادم النشطة ** جنبًا إلى جنب مع VBScript. يمكن أيضًا استخدام لغة البرمجة النصية هذه في مكون البرنامج النصي لنظام التشغيل Windows. يتم تخزين ملفات هذه اللغة بملحق .vbs في Windows.

هناك العديد من هياكل التحكم مثل الحلقات المستخدمة في كود هذه اللغة. كما يتضمن أيضًا وسيطات من سطر الأوامر ويمكن تسميتها أو عدم تسميتها. يمكن تخزين ملفات هذه اللغة في المجلدات أو على سطح المكتب لنظام التشغيل Windows. على الرغم من عدم وجود بيئة تطوير متكاملة محددة لبرامج VBScript مثل Microsoft Script Editor توفر تسهيلات لتطوير هذه اللغة.

عندما يتم استضافة VBScript بواسطة مضيف البرنامج النصي لـ Windows ، فإنه يوفر العديد من الميزات الشائعة جدًا للغات البرمجة النصية ولكنها غير متوفرة في Visual Basic 6.0. تتضمن الميزات التي تتضمن وصولاً سهلاً أو مباشرًا طابعات الشبكة ، وسيطات سطر الأوامر غير المسماة والمسماة ، و stdout ، و stdin ، ومشاركة الشبكة ، و Windows Management Instrumentation ، ومعلومات المستخدم الخاصة بالشبكات مثل عضوية المجموعة ، وغير ذلك الكثير.

## مثال تنسيق ملف VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## المرجعي ##

* [VBS - بواسطة Wikipedia](https://en.wikipedia.org/wiki/VBScript)



