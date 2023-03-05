{
  "date" : "2021-05-20",
  "keywords" :["shtml", "shtml file", "shtml file format", "shtml file type", "file", "type", "what is a shtml file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - جانب الخادم يتضمن ملف HTML" ,
  "description":"تعرف على تنسيق ملف SHTML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SHTML وفتحها." ,
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-20"
}

## ما هو ملف SHTML؟

الملف بامتداد .shtml هو صفحة ويب مكتوبة بلغة [HTML](/ar/ web / html /) وتتضمن إرشادات الخادم. قد يحتوي أيضًا على جانب الخادم يتضمن ملفات مشابهة لملفات ASP من أجل تحميل أسرع. يمكن أن تحتوي ملفات جانب الخادم أيضًا على تعليمات برمجية قابلة للتنفيذ يمكن أن تجعل الخادم يتم تحميله بشكل أبطأ من المعتاد. تشبه ملفات SHTML ملفات HTML ولكنها تسمح أيضًا باستخدام أوامر الخادم البسيطة. يتم تنفيذ أوامر الخادم هذه بلغة برمجة كمبيوتر بسيطة تسمى Server Side Includes (SSI). تم استبدال SHTML إلى حد كبير بلغات برمجة أخرى من جانب الخادم مثل [PHP](/ar/ برمجة / php /).

## تنسيق ملف SHTML

تتم كتابة ملفات SHTML بنص عادي وتستخدم [أوامر SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) التي يتم تنفيذها على جانب الخادم. يمكن استخدام أوامر جانب الخادم هذه حتى للاتصال بقاعدة البيانات باستخدام برامج تشغيل قاعدة البيانات وجلب بيانات المستخدمين من الجداول.

## مثال SHTML

تُستخدم إرشادات جانب الخادم في تطبيقات مثل عداد زوار الصفحة أو تقويم صفحة الويب. يعرض المثال التالي الأعمدة الأربعة الأولى من الأسطر الثلاثة الأولى من قاعدة بيانات المستخدمين.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## مراجع

* [يتضمن جانب الخادم](https://en.wikipedia.org/wiki/Server_Side_Includes)

