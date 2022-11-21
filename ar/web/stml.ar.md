{
  "date" : "2021-05-20",
  "keywords" :["stml" , "ملف stml" , "تنسيق ملف stml" , "نوع ملف stml" , "ملف" , "النوع" , "ما هو ملف stml"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"STML - ملف SSI HTML" ,
  "description":"تعرف على تنسيق ملف STML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات STML وفتحها." ,
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-20"
}

## ما هو ملف STML؟

الملف بامتداد .stml هو صفحة ويب تحتوي على إرشادات من جانب الخادم يتم تنفيذها عندما يقوم المستخدم بتحميل الصفحة في متصفح الويب. تحتوي صفحات STML على تعليمات برمجية من جانب الخادم تحتوي على جانب الخادم يتضمن أداء مهام لا يمكن تحقيقها باستخدام HTML عادي. على الرغم من أنه مشابه لـ [HTML] (/ar/ web / html /) ، يوفر STML المزيد من القوة عن طريق تشغيل الأوامر على الخادم ، وتسمى أيضًا Server Side Includes (SSI). مع إدخال لغات برمجة جديدة مع البرمجة النصية من جانب الخادم مثل PHP ، يتم تقليل استخدام STML على الرغم من أنه لا يزال مدعومًا من قبل جميع تقنيات جانب الخادم. يمكن فتح ملفات STML في أي محرر نصوص وتحريرها لتحديث الأوامر.

## تنسيق ملف STML

يعتمد STML على تنسيق ملف نصي عادي يمكن للبشر قراءته. ومع ذلك ، فإنه يتبع بناء الجملة كما تم تعريفه وممارسته باستخدام [أوامر SSI] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) التي يتم تنفيذها على جانب الخادم. مثل أي لغة برمجة نصية أخرى من جانب الخادم ، يمكن لـ STML استخدام أوامر جانب الخادم لأداء مهام مثل عداد زوار الصفحة وتقويم صفحة الويب واسترداد السجلات من قاعدة البيانات وغيرها من المهام المماثلة.

## مثال STML

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

* [يتضمن جانب الخادم] (https://en.wikipedia.org/wiki/Server_Side_Includes)

