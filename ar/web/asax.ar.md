{
  "date" : "2019-10-11",
  "keywords" :["asax" , "ملف asax" , "تنسيق ملف asax" , "نوع ملف asax" , "ملف" , "نوع" , "ما هو ملف asax"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ملف تطبيق خادم ASP.NET" ,
  "description" :"تعرف على كيفية معرفة ما هو ملف ASAX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASAX وفتحها." ,
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-07"
}

## ما هو ملف ASAX؟

الملف ذو الامتداد .asax هو ملف تستخدمه تطبيقات ASP.NET الموجودة على جانب الخادم. يحتوي على رمز للاستجابة للأحداث على مستوى التطبيق والجلسة التي تم رفعها بواسطة ASP.NET أو بواسطة وحدات HTTP النمطية. يتضمن هذا أيضًا التعامل مع أحداث معينة عند بدء تشغيل التطبيق أو إيقاف تشغيله. تعد ملفات ASAX اختيارية ويتم إضافة ملف ASAX واحد فقط إلى تطبيقات الويب للتعامل مع الأحداث والأخطاء على مستوى التطبيق على المستوى العالمي. على عكس صفحات ASPX ، لا تحتوي ملفات ASAX على أي تعليمات برمجية لتنفيذ وظائف التطبيق.

## تنسيق ملف ASAX

تتم كتابة ملفات ASAX بتنسيق ملف نصي عادي ويمكن قراءتها من قبل الإنسان. ملف ASAX الأكثر استخدامًا هو Global.asax الموجود في الدليل الجذر لتطبيق ASP.NET. تم تكوين خوادم الويب لرفض أي مكالمات واردة إلى هذا الملف لمنع المستخدمين من تنزيل أو عرض رمز هذا الملف.

### Global.ASAX - مثال على تنسيق ملف ASAX

يتكون ملف ASAX الفردي من أقسام متعددة تمت كتابتها للتعامل مع الأحداث على مستوى التطبيق. هذه هي على النحو التالي.

* ** توجيهات التطبيق ** - توجيهات التطبيق عبارة عن علامات تُستخدم لتحديد الإعدادات الاختيارية الخاصة بالتطبيق ليتم استخدامها بواسطة محلل ASP.NET عند معالجة ملف Global.asax. توجد هذه التوجيهات في بداية الملف Global.asax ويتم تعريفها على النحو التالي.

""
<٪ @ سمة التوجيه = القيمة [السمة = القيمة…]٪>
""
* ** كتل إعلان التعليمات البرمجية ** - تُستخدم كتل إعلان التعليمات البرمجية لتحديد أقسام التعليمات البرمجية للخادم المضمنة في ملفات تطبيق ASP.NET داخل \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* ** Code Render Blocks ** - تحدد هذه الكود أو التعبيرات المضمنة التي يتم تنفيذها عند عرض الصفحة. يشتمل نمطا كتل عرض التعليمات البرمجية على تعليمات برمجية مضمنة وتعبيرات مضمنة. يتم استخدام السابق لتحديد الأسطر أو كتل التعليمات البرمجية القائمة بذاتها ، بينما يتم استخدام الجانب كاختصار لاستدعاء طريقة الكتابة.

## مراجع

* [نظرة عامة على معالجات HTTP ووحدات HTTP النمطية](https://msdn.microsoft.com/en-us/library/bb398986 (v = مقابل 100))
* [Global.asax Syntax](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw (v = مقابل 100))

