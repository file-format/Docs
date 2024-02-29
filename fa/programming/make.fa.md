{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "ساخت فایل - فایل اسکریپت Xcode Makefile",
  "description": "با فرمت XCode MakeFile و APIهایی که می توانند فایل های MakeFile را ایجاد و باز کنند، آشنا شوید.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-fae"
}
}،
  "lastmod": "2020-09-10"
}


## فایل MAKE چیست؟

فایل MAKE یک فایل اسکریپت XCode است که کامپایل کد را سازماندهی می کند. برای کامپایل و پیوند دادن برنامه ها از چندین فایل کد منبع استفاده می شود. این کمک می کند تا تصمیم بگیرید که کدام بخش از یک برنامه بزرگ زمانی که برنامه نیاز به به روز رسانی دارد باید دوباره کامپایل شود. بسته به اینکه چه فایل‌هایی تغییر کرده‌اند، فایل‌ها را با استفاده از یک سری دستورالعمل اجرا کنید.

## فرمت فایل MAKE مثال

محتویات زیر با استفاده از ابزار Make اجرا شده و خروجی ها به صورت زیر است.

```
hello:
	echo "hello world"
```
**تولید خروجی**

```
$ make
echo "hello world"
hello world
```

## منابع
 * [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
 * [راهنمای Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

