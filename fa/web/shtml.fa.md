{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"فایل shtml",
"فرمت فایل shtml",
"نوع فایل shtml",
"فایل",
"نوع",
"فایل shtml چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML - سمت سرور شامل فایل HTML",
  "description": "درباره قالب فایل SHTML و APIهایی که می توانند فایل های SHTML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-fal"
}
},
  "lastmod": "2021-05-20"
}

## فایل SHTML چیست؟

یک فایل با پسوند .shtml یک صفحه وب است که به زبان [HTML](/web/html/) نوشته شده است و شامل دستورالعمل های سرور است. همچنین ممکن است شامل فایل های سمت سرور مشابه فایل های ASP برای بارگذاری سریع تر باشد. فایل‌های سمت سرور همچنین می‌توانند حاوی کدهای اجرایی باشند که می‌تواند سرعت بارگذاری سرور را کندتر از حد معمول کند. فایل های SHTML شبیه به HTML هستند اما امکان استفاده از دستورات سرور ساده را نیز دارند. این دستورات سرور در یک زبان برنامه نویسی کامپیوتری ساده به نام Server Side Includes (SSI) انجام می شود. SHTML تا حد زیادی توسط سایر زبان های برنامه نویسی سمت سرور مانند [PHP](/programming/php/) جایگزین شده است.

## فرمت فایل SHTML

فایل‌های SHTML در متن ساده نوشته می‌شوند و از [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) استفاده می‌کنند که در سمت سرور اجرا می‌شوند. این دستورات سمت سرور را می توان حتی برای اتصال به پایگاه داده با استفاده از درایورهای پایگاه داده و واکشی داده های کاربران از جداول استفاده کرد.

## مثال SHTML

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


