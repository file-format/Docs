{
  "date": "2021-05-20",
  "keywords": [
"stml",
"فایل stml",
"فرمت فایل stml",
"نوع فایل stml",
"فایل",
"نوع",
"فایل stml چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML - فایل HTML SSI",
  "description": "با فرمت فایل STML و APIهایی که می توانند فایل های STML را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-fal"
}
},
  "lastmod": "2021-05-20"
}

## فایل STML چیست؟

یک فایل با پسوند .stml یک صفحه وب با دستورالعمل های سمت سرور است که زمانی که کاربر صفحه را در مرورگر وب بارگیری می کند، اجرا می شود. صفحات STML حاوی کد سمت سرور است که شامل قسمت های سرور برای انجام کارهایی است که با HTML ساده امکان پذیر نیست. اگرچه STML شبیه به [HTML](/web/html/) است، اما STML با اجرای دستورات روی سرور، که شامل سمت سرور (SSI) نیز می‌شود، قدرت بیشتری ارائه می‌دهد. با معرفی زبان های برنامه نویسی جدید با برنامه نویسی سمت سرور مانند PHP، استفاده از STML کاهش یافته است، اگرچه هنوز توسط تمام فناوری های سمت سرور پشتیبانی می شود. فایل های STML را می توان در هر ویرایشگر متنی باز کرد و برای به روز رسانی دستورات ویرایش کرد.

## فرمت فایل STML

STML بر اساس فرمت فایل متنی ساده ascii است که برای انسان قابل خواندن است. با این حال، از نحوی که با استفاده از [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) که در سمت سرور اجرا می‌شوند، تعریف و تمرین می‌شود، پیروی می‌کند. مانند هر زبان برنامه نویسی سمت سرور دیگر، STML می تواند از دستورات سمت سرور برای انجام کارهایی مانند شمارنده بازدیدکنندگان صفحه، تقویم صفحه وب، بازیابی سوابق از پایگاه داده و موارد مشابه استفاده کند.

## مثال STML

دستورالعمل های سمت سرور در برنامه هایی مانند شمارنده بازدیدکنندگان صفحه یا تقویم صفحه وب استفاده می شود. مثال زیر، چهار ستون اول از سه خط اول پایگاه داده کاربران را نمایش می دهد.

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
## منابع

* [Server Side Includes] (https://en.wikipedia.org/wiki/Server_Side_Includes)


