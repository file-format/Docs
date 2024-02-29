{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"فایل",
"افزونه",
"فرمت فایل",
"اسکریپت ویژوال بیسیک",
"راهنمای برنامه نویسی",
"مثال vbs",
"مایکروسافت ویژوال بیسیک",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS - فایل اسکریپت ویژوال بیسیک",
  "description": "با فرمت فایل VBS و API هایی که می توانند فایل های VBS را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-fas"
}
},
  "lastmod": "2021-08-24"
}

## فایل VBS چیست؟

VBS یا VBScript با نسخه اسکریپت مایکروسافت ویژوال بیسیک متصل است. در محیط محاسباتی، کاربر اجازه دسترسی و کنترل بسیاری از جنبه های آن را دارد. VBScript مجاز است از مدلی به نام **Component Object Model** برای استفاده از عناصر و ابزارهای محیط استفاده کند. این محیط برای کار و اجرای VBScript مشخص شده است.

هنگامی که مشتری در زمینه توسعه وب به آن دسترسی پیدا می کند، مانند جاوا اسکریپت عمل می کند. همچنین توسط سرورها برای پردازش صفحات وب استفاده می شود. می توان آن را در برخی از انواع فایل های اسکریپت نویسی دیگر مانند برنامه های کاربردی [HTML](/web/html/) در نظر گرفت.


## تاریخچه مختصر ##

این برای اولین بار در سال 1996 راه اندازی شد، به عنوان بخشی از فن آوری های مورد استفاده توسط مایکروسافت مشخص شده برای Windows Scripts. در ابتدا به طور خاص برای کمک به توسعه دهندگان وب توسعه داده شد. در همان سال اکسپلورر ویندوز مایکروسافت به نام اینترنت اکسپلورر به همراه ویژگی های ویژوال بیسیک اسکریپت منتشر شد.

با پیشرفت تکنولوژی و توسعه وب، نسخه های زیادی از VBScript به همراه بسیاری از ویژگی های پیشرفته راه اندازی شد. علاوه بر این، در سال آینده، این زبان برنامه نویسی با ویژگی های جدید بخشی از ویندوز مایکروسافت خواهد بود.

## مشخصات فنی ##

برای صفحات وب در سمت سرور، از ابزارهایی مانند **Active Server Pages** به همراه VBScript استفاده می شود. این زبان برنامه نویسی را می توان در مولفه اسکریپت ویندوز نیز استفاده کرد. فایل های این زبان با پسوند .vbs در ویندوز ذخیره می شوند.

ساختارهای کنترلی زیادی مانند حلقه ها وجود دارد که در کدهای این زبان استفاده می شود. همچنین شامل آرگومان هایی می شود که خط فرمان هستند و می توانند با نام یا بدون نام باشند. فایل های این زبان را می توان به سادگی در پوشه ها یا روی دسکتاپ یک سیستم عامل ویندوز ذخیره کرد. اگرچه محیط توسعه یکپارچه خاصی برای برنامه های VBScript مانند Microsoft Script Editor وجود ندارد، تسهیلات توسعه این زبان را فراهم می کند.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. ویژگی هایی که دسترسی آسان یا مستقیم را شامل می شود شامل چاپگرهای شبکه، آرگومان های خط فرمان بی نام و نام، stdout و stdin، اشتراک گذاری شبکه، ابزار مدیریت ویندوز، اطلاعات کاربر شبکه ها مانند عضویت در گروه و موارد دیگر است. 

## فرمت فایل VBS مثال ##

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

## ارجاع ##

* [VBS - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/VBScript)




