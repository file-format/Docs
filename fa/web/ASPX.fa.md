{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"فایل aspx",
"فرمت فایل aspx",
"نوع فایل aspx",
"فایل",
"نوع",
"فایل aspx چیست"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل ASPX",
  "description": "راهنمای فرمت فایل شما برای یادگیری فایل ASPX و APIهایی که می توانند فایل های ASPX را ایجاد و باز کنند.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-faX"
}
}،
  "lastmod": "2020-09-10"
}

## فایل ASPX چیست؟

یک فایل با پسوند .aspx یک صفحه وب است که با استفاده از چارچوب ASP.NET مایکروسافت که بر روی سرورهای وب اجرا می شود تولید شده است. ASPX مخفف عبارت Active Server Pages Extended است و این صفحات در مرورگر وب در انتهای کاربر هنگام دسترسی به URL نمایش داده می شوند. این جانشین فناوری [ASP](/web/asp/) است که در انتهای سرور نیز تولید می‌شود اما از چارچوب دات‌نت استفاده نمی‌کند. صفحات ASP.NET ممکن است حاوی اسکریپت های [C#](/programming/cs/) یا [VB.NET](/programming/vb/) باشند که توسط وب سرور برای ارائه به کاربر در مرورگر وب به HTML ترجمه می شوند. صفحات ASPX همچنین فرم های وب دات نت نامیده می شوند. اینها را می توان با برنامه هایی مانند Microsoft Visual Studio، Adobe Dreamweaver، Notepad++ و هر ویرایشگر متنی باز و ایجاد کرد.

## فرمت فایل ASPX

فرم های وب ASP.NET مبتنی بر مدل رویداد محور برای تعامل با برنامه وب هستند. مرورگر که یک کاربر نهایی است، یک فرم وب را به سرور ارسال می کند و سرور در پاسخ یک صفحه نشانه گذاری کامل یا صفحه HTML را برمی گرداند. مدل جزء ASP.NET مدل شی را برای صفحات ASPX ارائه می دهد. این مدل توضیح می دهد:

 * همتای سمت سرور تقریباً همه عناصر یا برچسب‌های HTML، مانند \<form style=;text-align:right;direction:rtl> و \<input> .
 * کنترل های سرور، که به توسعه رابط کاربری پیچیده کمک می کند. برای مثال، کنترل Calendar یا کنترل Gridview.

فایل های ASPX از ASP.NET **Code Behind model** برای ساخت این صفحات استفاده می کنند.

### کد درون خطی

کد نمونه ای که به صورت درون خطی در صفحه ASPX تعبیه شده است و همه عملکردها را برای پیاده سازی کاربر فراهم می کند. کد [C#](/programming/cs/) زیر یک صفحه نمونه ASP.NET را نشان می دهد که شامل کد درون خطی است:

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

### کد-پشت

کد را می توان در فایل های کلاس جداگانه نوشت و ذخیره کرد تا HTML را از منطق ارائه جدا کند. این باعث می شود لایه ارائه مستقل از کد اجرایی باشد. در زیر کد پشتی برای ارائه به کاربر آمده است.

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

پیاده سازی C# از منطق واقعی برای لایه ارائه به شرح زیر است.

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

## منابع

 * [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

