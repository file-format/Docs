{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل PS",
  "description": "با فرمت فایل PS و APIهایی که می توانند فایل های PS را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-fas"
}
},
  "lastmod": "2019-09-10"
}

## فایل PS چیست؟ ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## تاریخچه مختصر ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. استیو جابز از اپل از آنها بازدید کرد و به آنها توصیه کرد که PostScript را برای درایو چاپگرهای لیزری تطبیق دهند.

در مارس 1985، اولین چاپگر با مفسر پست اسکریپت جاسازی شده، LaserWriter اپل بود که انقلابی در انتشار دسکتاپ (DTP) ایجاد کرد. استحکام فنی و در دسترس بودن گسترده، PostScript را به زبانی انتخابی برای انتشارات رومیزی و الکترونیکی تبدیل کرده است. در طول سال 1990، یک مترجم برای زبان پست اسکریپت بخش مهمی از چاپگرهای لیزری بود.

## ویژگی های اصلی ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**اشکال:** ماهیت دلخواه، ممکن است شامل خطوط مستقیم، منحنی ها، مربع ها و منحنی های مکعبی باشد که می توانند هم متحرک و هم جدا شوند (در بخش ها و سوراخ ها).

**عملگرهای نقاشی:** به طرح کلی شکل از هر ضخامت، رنگ، پر کردن اجازه می دهند یا اجازه می دهند شکل به عنوان یک برش کشیده شود تا امکان برش هر گرافیک دیگری را فراهم کند.

** رنگ ها: ** دارای تنوع مانند مقیاس خاکستری، RGB، CMYK و CIE هستند. انواع خاصی از رنگ‌ها به عنوان ویژگی‌های مختلف مدل‌سازی می‌شوند: رنگ‌های نقطه‌ای، نقشه‌برداری رنگ، حتی سایه‌زنی و تکرار الگوها.

**متن:** به طور کامل با گرافیک یکپارچه شده است. علاوه بر این، مدل تصویربرداری adobe به کاراکترهای متن اجازه می دهد تا به صورت اشکال گرافیکی نمایش داده شوند که ممکن است توسط هر اپراتور گرافیکی معمولی اجرا شود.

**تصاویر نمونه**: استخراج شده از منابع اصلی (عکس های اسکن شده) یا ممکن است به صورت مصنوعی تولید شوند. زبان PostScript ابزارهای متنوعی برای بازسازی تصاویر در هر وضوح و با توجه به مدل های رنگی مختلف در یک دستگاه خروجی ارائه می دهد.

یک زبان برنامه نویسی همه منظوره می تواند از قابلیت های گرافیکی زبان PostScript با تعبیه Ps در چارچوب خود استفاده کند. انواع داده های اولیه، مانند اعداد، کاراکترها، آرایه ها و رشته ها. کنترل اولیه، مانند حلقه ها، رویه ها و شرطی ها. و برخی از ویژگی های غیر متعارف، مانند فرهنگ لغت در زبان مشخص شده است. این ویژگی ها برنامه نویسان را برای نوشتن دستوراتی برای فراخوانی عملیات سطح بالاتر تسهیل می کند. این عملیات سطح بالا نیازهای برنامه های پیچیده را برآورده می کند. چنین عملی به جای استفاده از مجموعه ای ثابت از عملیات اساسی، فشرده تر و کارآمدتر است.

برنامه های نوشته شده در پست اسکریپت را می توان در قالب متن منبع ASCII تولید، ارتباط و تفسیر کرد. کل زبان را می توان در قالب کاراکترهای قابل چاپ و فضای سفید تعریف کرد. این نمایش از برنامه نویسان برای ایجاد، دستکاری و درک آسان زبان پشتیبانی می کند. علاوه بر این، ذخیره‌سازی و انتقال فایل در میان رایانه‌ها و سیستم‌های عامل مختلف از طریق استقلال ماشین راحت بود.

اشکال کدگذاری شده باینری از زبان، زمانی امکان پذیر است که برنامه یک مسیر ارتباطی کاملاً شفاف به مترجم PostScript تضمین شود. Adobe برای تبادل اسناد یا ذخیره سازی آرشیو، انسجام دقیق با نمایش ASCII برنامه های PS را توصیه می کند.

## نسخه ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. هر نسخه نظرات ساختاری مهمی را تعریف می کند. فایل پست اسکریپت محصور شده (EPS) یک نوع فرعی خاص از فایل پست اسکریپت است که از زبانی برای تعیین یک گرافیک مستطیلی استفاده می کند. راهنمای مرجع زبان پست اسکریپت EPS را اینگونه توصیف می کند: فایل پست اسکریپت (EPS) محصور شده یک برنامه پست اسکریپت است که حداکثر یک صفحه را به شکلی توصیف می کند که می تواند توسط برنامه های کاربردی دیگر وارد شود تا در یک سند حاوی جاسازی شود. یک فایل سند PostScript می تواند یک فایل EPS را در آن کپسوله کند. استفاده اضافی از PostScript به عنوان Display PostScript (DPS) ذکر شده است. DPS از طریق یک موتور گرافیکی که از مدل و زبان تصویربرداری PostScript استفاده می کند، گرافیک های روی صفحه را تولید می کند.

## منابع ##

* [خانواده قالب پست اسکریپت] (https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


