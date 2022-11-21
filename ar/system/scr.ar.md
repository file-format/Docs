{
  "date" : "2021-07-13",
  "keywords" :["scr file", "what is a scr file", "file", "scr example", "scr file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - ملف شاشة Windows" ,
  "description":"تعرف على تنسيق ملف SCR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SCR وفتحها." ,
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-07-13"
}

## SCR ما ه
الملف ذو الامتداد .scr هو ملف شاشة توقف يستخدمه نظام التشغيل Microsoft Windows. وهو يتألف من رسوم متحركة أو رسوم بيانية أو عرض شرائح أو فيديو يمكن استخدامه كشاشة توقف لنظام Windows. يتم تخزين ملفات SCR بشكل شائع في الدليل الرئيسي لنظام التشغيل Microsoft Windows. كان من المفترض أن تمنع شاشات التوقف CRT أو شاشات الكمبيوتر البلازما من المعاناة من حالة تحدث عندما تعرض الشاشة نفس الصورة لفترة طويلة جدًا. على الرغم من أن الشاشات الأحدث لا تعاني في مثل هذه الحالة ، إلا أن شاشات التوقف لا تزال تستخدم لمنع الشاشة لأسباب أمنية.

## تنسيق ملف SCR
شاشة التوقف هي برنامج كمبيوتر يملأها بصور أو أنماط متحركة عندما لا يتم تنفيذ أي نشاط على جهاز الكمبيوتر لفترة طويلة. تم تقديم شاشات التوقف لمنع احتراق الفوسفور على البلازما وأنبوب أشعة الكاثود (CRT) وشاشات الكمبيوتر OLED. عادةً ما يتم إعداد شاشات التوقف لتطبيق طبقة أساسية من الأمان ، من خلال طلب كلمة مرور لإعادة فتح الجهاز. عادةً ما يتم تطوير شاشات التوقف وترميزها باستخدام لغات برمجة مختلفة بالإضافة إلى واجهات رسومات. يستخدم مطورو شاشات التوقف في الغالب لغات البرمجة C أو C ++ ، جنبًا إلى جنب مع المكتبات الرسومية أو GDIs ، مثل OpenGL ، الذي يعمل على العديد من الأنظمة الأساسية القادرة على العرض ثلاثي الأبعاد. يتم حفظ إخراج شاشات التوقف كملف قابل للتنفيذ محمول.

### استخدام ملف SCR
في شاشات CRT القديمة أو شاشات البلازما ، تم الإبلاغ عن احتراق الشاشة لأنه تم عرض نفس الصورة على الشاشة لفترة طويلة. يحدث احتراق الشاشة عندما تتغير خصائص المناطق المكشوفة لطلاء الفوسفور داخل الشاشة تدريجياً ويؤدي في النهاية إلى صورة ظل داكنة على الشاشة. لذلك كان من المفترض أن تغير شاشات التوقف صورة الشاشة بشكل مستمر وعادة ما تكون ملفات .scr ضرورية لشاشات أجهزة الصراف الآلي أو آلات تذاكر السكك الحديدية. في وقت لاحق ، تم حل المشكلة على شاشات LCD والإصدارات الأكثر تقدمًا من الشاشات. لذلك لا تزال شاشات التوقف مستخدمة في العصر الحديث لحماية الأجهزة الخاملة من استخدام الشخص الثاني. يتطلب كلمة المرور أو النمط لإعادة الوصول إلى الجهاز.

## إنشاء شاشة توقف باستخدام C #
على الرغم من أنه يمكننا إنشاء شاشة توقف بأي من لغات البرمجة .NET ، إلا أنه يتم توفير لغة البرمجة C # هنا:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
قم بتغيير امتداد الملف القابل للتنفيذ من. exe إلى .scr. لذلك يمكن تسمية ملف SCR باسم ScreenSaver.scr.

## مراجع

* [شاشة التوقف] (https://en.wikipedia.org/wiki/Screensaver)
* [اكتب شاشة توقف تعمل بالفعل] (https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


