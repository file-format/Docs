{
  "date": "2019-10-11",
  "keywords": [
"asax",
"فایل asax",
"فرمت فایل asax",
"نوع فایل asax",
"فایل",
"نوع",
"فایل asax چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX - فایل برنامه سرور ASP.NET",
  "description": "یاد بگیرید که فایل ASAX و APIهایی که می توانند فایل های ASAX را ایجاد و باز کنند چیست.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-fax"
}
},
  "lastmod": "2021-06-07"
}

## فایل ASAX چیست؟

یک فایل با پسوند asax. فایلی است که توسط برنامه های ASP.NET استفاده می شود که در سمت سرور قرار دارد. این شامل کدی برای پاسخگویی به رویدادهای سطح برنامه و جلسه است که توسط ASP.NET یا توسط ماژول های HTTP مطرح شده است. این همچنین شامل رسیدگی به برخی رویدادها هنگام راه اندازی یا خاموش شدن برنامه می شود. فایل‌های ASAX اختیاری هستند و تنها یک فایل ASAX به برنامه‌های وب اضافه می‌شود تا رویدادها و خطاهای سطح برنامه را در سطح جهانی مدیریت کند. برخلاف صفحات ASPX، فایل های ASAX حاوی هیچ کدی برای اجرای عملکرد برنامه نیستند.

## فرمت فایل ASAX

فایل های ASAX در قالب فایل متنی ساده نوشته می شوند و قابل خواندن توسط انسان هستند. رایج ترین فایل ASAX مورد استفاده Global.asax است که در دایرکتوری ریشه یک برنامه ASP.NET قرار دارد. وب سرورها به گونه ای پیکربندی شده اند که تماس های ورودی به این فایل را رد کنند تا کاربران را از دانلود یا مشاهده کد این فایل منع کنند.

### Global.ASAX - نمونه ای از فرمت فایل ASAX

یک فایل ASAX شامل چندین بخش است که برای مدیریت رویدادهای سطح برنامه نوشته شده است. اینها به شرح زیر است.

 * **دستورالعمل های برنامه** - دستورالعمل های کاربردی برچسب هایی هستند که برای تعریف تنظیمات اختیاری خاص برنامه مورد استفاده قرار می گیرند تا توسط تجزیه کننده ASP.NET هنگام پردازش فایل Global.asax استفاده شود. این دستورالعمل ها در ابتدای فایل Global.asax قرار دارند و به صورت زیر تعریف می شوند.

```
<%@ خصیصه دستوری=مقدار [ویژگی=مقدار…]%>
```
 * **بلوک های اعلام کد** - بلوک های اعلام کد برای تعریف بخش هایی از کد سرور استفاده می شود که در فایل های برنامه ASP.NET در داخل \ تعبیه شده است.<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
 * ** بلوک های رندر کد ** - این ها کد یا عباراتی را که هنگام رندر صفحه اجرا می شوند، تعریف می کنند. دو سبک بلوک های رندر کد شامل کد درون خطی و عبارات درون خطی هستند. اولی برای تعریف خطوط یا بلوک های کد مستقل استفاده می شود، در حالی که از lateral به عنوان میانبر برای فراخوانی متد Write استفاده می شود.

## منابع

 * [بررسی اجمالی هندلرهای HTTP و ماژول های HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Syntax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

