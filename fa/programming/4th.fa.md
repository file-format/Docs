
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فایل چهارم - فرمت فایل زبان چهارم",
  "description":"با مثال و APIهایی که می توانند فایل های چهارم را ایجاد و باز کنند، با فرمت فایل .4 آشنا شوید.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-fa",
      "parent" : "programming"
}
}،
  "lastmod" : "2023-02-09"
}

## فایل چهارم چیست؟

یک فایل با پسوند فایل .4 یک فایل برنامه نویسی است که برای **زبان برنامه نویسی چهارم** ایجاد شده است. این شامل کد منبع برای برنامه های نوشته شده به زبان برنامه نویسی Forth است و خروجی را هنگام اجرای برنامه تولید می کند. این فقط یک فایل زبان برنامه نویسی دیگر است که شبیه فایل منبع [C](/programming/c/) و [C++](/programming/cpp/) است.

## فرمت فایل چهارم - اطلاعات بیشتر


### مثال کد زبان برنامه نویسی چهارم

در اینجا یک مثال از یک برنامه ساده نوشته شده در Forth است که فاکتوریل یک عدد معین را محاسبه می کند:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * دو مقدار را در بالای پشته ضرب می کند. ساختارهای if و start/until جریان برنامه را کنترل می کنند.

برای استفاده از این برنامه، باید تعریف را در مفسر Forth وارد کنید و سپس کلمه فاکتوریل را با شماره ای که می خواهید فاکتوریل آن را پیدا کنید فراخوانی کنید:

```
10 factorial .
```
این منجر به خروجی 3628800 می شود که فاکتوریل 10 است.

## منابع

 * [زبان برنامه نویسی چهارم](https://en.wikipedia.org/wiki/Forth_(programming_language))

