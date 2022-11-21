{
  "date" : "2019-10-11",
  "keywords" :["aspx" , "ملف aspx" , "تنسيق ملف aspx" , "نوع ملف aspx" , "ملف" , "النوع" , "ما هو ملف aspx"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف ASPX" ,
  "description" :"دليل تنسيق الملف الخاص بك للتعرف على ملف ASPX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASPX وفتحها." ,
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف ASPX؟

الملف ذو الامتداد .aspx عبارة عن صفحة ويب تم إنشاؤها باستخدام إطار عمل Microsoft ASP.NET يعمل على خوادم الويب. يرمز ASPX إلى Active Server Pages Extended ويتم عرض هذه الصفحات في مستعرض الويب عند نهاية المستخدم عند الوصول إلى عنوان URL. إنه خليفة لتقنية [ASP] (/ar/ web / asp /) والتي يتم إنشاؤها أيضًا في نهاية الخادم ولكنها لا تستخدم .NET framework. قد تحتوي صفحات ASP.NET على [C #] (/ar/ برمجة / cs /) أو [VB.NET] (/ar/ برمجة / vb /) نصوص تمت ترجمتها إلى HTML بواسطة خادم الويب لعرضها على المستخدم في متصفح الويب. تسمى صفحات ASPX أيضًا نماذج ويب .NET. يمكن فتحها وإنشاؤها باستخدام تطبيقات مثل Microsoft Visual Studio و Adobe Dreamweaver و Notepad ++ وأي محرر نصوص.

## تنسيق ملف ASPX

تستند نماذج الويب ASP.NET إلى النموذج المستند إلى الحدث للتفاعلات مع تطبيق الويب. المتصفح ، كونه مستخدمًا نهائيًا ، يرسل نموذج ويب إلى الخادم ويعيد الخادم صفحة ترميز كاملة أو صفحة HTML ردًا على ذلك. يقدم طراز مكون ASP.NET طراز كائن لصفحات ASPX. يصف هذا النموذج:

* نظائر جانب الخادم لجميع عناصر أو علامات HTML تقريبًا ، مثل \<form style=";text-align:right;direction:rtl"> و \<input> .
* ضوابط الخادم ، والتي تساعد في تطوير واجهة مستخدم معقدة. على سبيل المثال ، عنصر تحكم التقويم أو عنصر تحكم Gridview.

تستخدم ملفات ASPX نموذج ASP.NET ** Code Behind ** لبناء هذه الصفحات.

### التعليمات البرمجية المضمنة

نموذج التعليمات البرمجية المضمنة في صفحة ASPX وتوفر كافة الوظائف لتنفيذ المستخدم. تمثل التعليمات البرمجية [C #] (/ar/ البرمجة / cs /) التالية نموذج صفحة ASP.NET تتضمن تعليمات برمجية مضمنة:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### كود خلف

يمكن كتابة التعليمات البرمجية وتخزينها في ملفات فئة منفصلة لفصل HTML عن منطق العرض. هذا يجعل طبقة العرض مستقلة عن الكود القابل للتنفيذ. فيما يلي الكود الخلفي للعرض على المستخدم.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

يكون تنفيذ C # للمنطق الفعلي لطبقة العرض كما يلي.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## مراجع

* [ASP.NET WebApps - Microsoft] (https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

