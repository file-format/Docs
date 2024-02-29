{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فایل AIDL - فایل زبان تعریف رابط اندروید",
  "description":"با مثال و APIهایی که می توانند فایل های AIDL را ایجاد و باز کنند، درباره فرمت فایل AIDL چیست.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-fa",
      "parent" : "programming"
}
}،
  "lastmod" : "2022-10-30"
}

## فایل AIDL چیست؟

یک فایل AIDL (زبان تعریف رابط اندروید) به توسعه دهندگان اندروید اجازه می دهد تا بین برنامه های مختلف ارتباط برقرار کنند. بر اساس رابط برنامه نویسی، مشتری و سرویس هر دو توافق می کنند که با استفاده از ارتباطات بین فرآیندی (IPC) ارتباط برقرار کنند. فایل AIDL حاوی کد منبع [Java](/programming/java/) برای تعریف این رابط‌ها و قراردادها برای ارتباط بین برنامه‌ها است.

می‌توانید فایل‌های AIDL را با Google Android Studio یا هر ویرایشگر متنی مانند Microsoft Notepad و Notepad++ باز کنید.

## فرمت فایل AIDL - اطلاعات بیشتر

AIDL فایل های متنی هستند که دارای رابط های ارتباطی بین برنامه ها هستند. سیستم عامل اندروید به یک فرآیند اجازه دسترسی به حافظه فرآیند دیگر را نمی دهد. این باعث می شود که فرآیندها برای درک سیستم عامل زیربنایی، اشیاء خود را به موارد اولیه تقسیم کنند و فرآیند ساختارهای ارتباطی را برای توسعه دهنده ایجاد کنند.

### چه نوع داده هایی توسط AIDL پشتیبانی می شوند؟

AIDL به طور پیش فرض از انواع داده های زیر پشتیبانی می کند.

 * همه انواع اولیه در زبان برنامه نویسی جاوا (مانند int، long، char، boolean و غیره)
 * رشته
 * CharSequence
 * فهرست کنید
 * نقشه

## نمونه فایل AIDL

در زیر یک نمونه فایل AIDL آورده شده است.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## منابع

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

