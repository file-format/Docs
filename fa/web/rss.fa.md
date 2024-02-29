{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"جزئي",
"افزونه",
"فایل",
"قالب",
"وب",
"سندیکای واقعا ساده",
"نرم افزار Userland"
]،
  "author": {
    "display_name": "Sami Cheema"
}،
  "draft": "false",
  "toc": true,
  "title": "RSS - پیوندی واقعا ساده",
  "description": "با فرمت فایل RSS و APIهایی که می توانند فایل های RSS ایجاد و باز کنند آشنا شوید.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-fas"
}
}،
  "lastmod": "2021-06-24"
}

## فایل RSS چیست؟ ##

فایلی با پسوند rss. به عنوان Really Simple Syndication شناخته می شود. RSS یک نوع فایل به آسانی یا به راحتی توسط کامپیوتر، فایل XML است. این فایل های XML با هر گونه تغییر در داده ها یا به روز رسانی یک وب سایت یا صفحه وب به طور خودکار به روز می شوند. اطلاعات به روز شده همراه با ابرداده (نام نویسنده، نام ناشر، تاریخ انتشار و غیره) و سایر محتوای وب سایت توسط فایل های RSS کاربر استخراج شده و در قالبی خوانا ارائه می شود. بهترین ویژگی این فایل‌های RSS این است که به‌صورت بلادرنگ کار می‌کنند و به‌روزرسانی‌ها، اخبار، انتشارات، یعنی جدیدترین، در بالای فایل نمایش داده می‌شوند. با استفاده از یک فایل RSS، به راحتی می توانید با کشیدن محتوای مرتبط از وب و خواندن آن با استفاده از یک فایل RSS، یک فایل حاوی آخرین به روز رسانی های هر موضوعی که به آن علاقه دارید ایجاد کنید.

## تاریخچه مختصر ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. عملکرد دو فایل تقریباً مشابه است و می توان با اطمینان فرض کرد که مفهوم RSS بر اساس عملکرد RDF شکل گرفته است، یک فایل خوان که برای جمع آوری ابرداده استفاده می شود.

## مشخصات فنی ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. نسخه های مختلفی از فایل های RSS مختلف مانند 0.91، 0.92، 2.0 و غیره وجود دارد. فایل هر نسخه مطابق با مشخصات و استانداردهای آن نسخه خاص است. 

## مثال RSS ##

مثال زیر یک مثال ساده از RSS است.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## ارجاع ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
