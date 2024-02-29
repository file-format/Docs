{
  "date": "2023-06-12",
  "keywords": [
"پختن",
"فایل bak",
"نشانک‌های BAK Chromium",
"فایل باک چیست",
"نحوه باز کردن فایل bak",
"فایل",
"پسوند فایل bak",
"افزونه"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل BAK - پشتیبان‌گیری از نشانک‌های کرومیوم",
  "description": "درباره قالب نشانک‌های کرومیوم BAK و APIهایی که می‌توانند فایل‌های BAK را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-fa",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## فایل BAK چیست؟

یک فایل .bak در زمینه مرورگرهای وب مبتنی بر Chromium، مانند Google Chrome و Microsoft Edge، اساساً یک فایل پشتیبان از نشانک‌های شما است. این نشانک ها به عنوان یک لیست متن ساده ذخیره می شوند و فرمت فایل مورد استفاده JSON است. هدف این فایل‌های .bak حفاظت از نشانک‌های شما با ارائه یک نسخه پشتیبان است که در صورت حذف یا گم شدن تصادفی قابل بازیابی است.

مرورگرهای مبتنی بر کروم، از جمله Google Chrome، به طور معمول این فایل‌های پشتیبان را ایجاد می‌کنند و معمولاً نام «Bookmarks.bak» را به آن‌ها می‌دهند. آنها اساساً یک عکس فوری از نشانک های شما در یک زمان خاص هستند.

## نحوه استفاده از فایل .bak برای بازیابی نشانک های خود

1. **فایل پشتیبان را بیابید:** معمولاً در یک پوشه خاص مرتبط با نمایه Chromium شما قرار دارد. مکان دقیق بسته به سیستم عامل شما می تواند متفاوت باشد.

در ویندوز: به «C:\Users» نگاه کنید<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

در macOS: در «~/Library/Application Support/Chromium/Default/Bookmarks.bak» جستجو کنید.

در لینوکس: «~/.config/chromium/Default/Bookmarks.bak» را علامت بزنید.

3. مطمئن شوید که مرورگر Chromium شما بسته است.
4. نام فایل Bookmarks.bak را با حذف پسوند .bak تغییر دهید، بنابراین به سادگی Bookmarks نامیده می شود.
5. Chromium را راه اندازی کنید.

با تغییر نام فایل .bak به نشانک ها، Chromium از آن به عنوان فایل نشانک فعلی استفاده می کند و نشانک های قبلی شما باید بازیابی شوند.

## پشتیبان‌گیری از نشانک‌های کرومیوم

پشتیبان‌گیری از نشانک‌های Chromium خود یک اقدام احتیاطی عاقلانه است تا اطمینان حاصل شود که صفحات وب و نشانی‌های وب ذخیره شده مهم خود را از دست نمی‌دهید. Chromium یک مرورگر منبع باز است که به عنوان پایه برای مرورگرهای دیگر مانند Google Chrome و Microsoft Edge عمل می کند. برای پشتیبان‌گیری از نشانک‌های Chromium خود، این مراحل را دنبال کنید:

## روش 1: پشتیبان گیری دستی

1. **باز کردن Chromium**: مرورگر Chromium را در رایانه خود راه اندازی کنید.

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **انتخاب مکان**: جایی را که می خواهید فایل نشانک های صادر شده در رایانه خود ذخیره کنید، انتخاب کنید. نام فایل پیش فرض bookmarks.html است، اما در صورت تمایل می توانید آن را تغییر دهید. آن را در مکانی که به خاطر خواهید آورد ذخیره کنید.

6. **ذخیره**: روی دکمه ذخیره یا صادر کردن کلیک کنید تا نشانک های خود را به عنوان یک فایل HTML ذخیره کنید.

نشانک‌های شما اکنون به‌عنوان یک فایل HTML پشتیبان‌گیری شده‌اند. می‌توانید این فایل را برای نگهداری در یک درایو خارجی یا فضای ذخیره‌سازی ابری کپی کنید.

## روش 2: همگام سازی با حساب Google (در صورت وجود)

اگر در Chromium به حساب Google وارد شده‌اید، می‌توانید از ویژگی همگام‌سازی داخلی نیز برای ایمن نگه داشتن نشانک‌های خود و همگام‌سازی بین دستگاه‌ها استفاده کنید. به این ترتیب، نشانک‌های شما به‌طور خودکار در حساب Google شما پشتیبان‌گیری می‌شوند.

1. **باز کردن Chromium**: مرورگر Chromium را راه اندازی کنید و مطمئن شوید که به حساب Google خود وارد شده اید.

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **همگام‌سازی و سرویس‌های Google**: در تب تنظیمات، روی «Sync and Google services» در نوار کناری سمت چپ کلیک کنید.

4. **همگام‌سازی داده‌های خود**: در بخش «همگام‌سازی»، مطمئن شوید که «نشانک‌ها» روشن است. این نشانک های شما را با حساب Google شما همگام می کند.

اکنون از نشانک‌های شما به‌طور خودکار پشتیبان‌گیری می‌شود و با حساب Google شما همگام‌سازی می‌شود. می‌توانید با ورود به حساب Google خود در هر دستگاهی با Chromium یا مرورگر دیگری که از همگام‌سازی Google پشتیبانی می‌کند، به آنها دسترسی داشته باشید.

به یاد داشته باشید که به طور دوره‌ای از نشانک‌های خود به صورت دستی نیز نسخه پشتیبان تهیه کنید، به خصوص اگر می‌خواهید یک نسخه محلی داشته باشید که صرفاً به همگام‌سازی حساب Google شما وابسته نباشد.

## نحوه باز کردن فایل BAK

اگر می‌خواهید داده‌های خام پشتیبان‌گیری از نشانک‌های خود را کاوش کنید، می‌توانید فایل «Bookmarks.bak» را با ویرایشگرهای متنی مختلف مانند Microsoft Visual Studio Code (در چندین پلتفرم موجود)، Microsoft Notepad (برای کاربران ویندوز)، Apple TextEdit باز کنید. (برای کاربران مک)، یا هر ویرایشگر متن دیگری به انتخاب شما. انجام این کار به شما امکان می دهد بوک مارک ها و ابرداده های موجود در فایل را مشاهده کنید.

می توانید فایل Bookmarks.bak را باز کرده و با استفاده از نرم افزارهای مختلف ویرایش متن و ویرایشگرهای کد، محتویات آن را مشاهده کنید. در اینجا برخی از گزینه های رایج استفاده می شود:

1. کد ویژوال استودیو (VS Code)
2. دفترچه یادداشت (ویندوز)
3. TextEdit (Mac)
4. متن عالی
5. Notepad++
6. اتم
7. نانو و ویم (لینوکس)
8. WordPad (ویندوز)

## سایر فایل های BAK

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.bak** استفاده می کنند.

**پایگاه اطلاعاتی**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**بازی**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**متفرقه**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**تنظیمات**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## منابع
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
