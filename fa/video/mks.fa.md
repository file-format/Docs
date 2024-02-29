{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل MKS",
  "keywords": [
"mks",
"ویدیوی matroska",
"فرمت mkv",
"فایل",
"قالب",
"ویدئو"
],
  "description": "درباره فرمت فایل MKS برای زیرنویس‌هایی که فقط توسط Matroska و APIهایی ایجاد شده‌اند که می‌توانند فایل‌های MKS را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-fas"
}
},
  "lastmod": "2021-25-02"
}

## فایل MKS چیست؟

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- .mks. پسوند توسط فایل Matroska (که فقط شامل زیرنویس است) استفاده خواهد شد.
- **CodecPrivate** برای ذخیره تمام اطلاعات مربوط به کدک ها که برای کل یک جریان جهانی است استفاده می شود.
- مُهرهای زمان شروع و توقف را که در قالب ذخیره‌سازی بومی مهر زمانی استفاده می‌شوند، حذف کنید. در عوض، از مهر زمانی و مدت زمان بلوک ها استفاده کنید.
- می توانید از هر چیزی با یک لایه شفاف استفاده کنید، از جمله ویدیو.

## فرمت های رایج زیرنویس

Here are some brief notes about more common subtitle formats stored in Matroska:

### زیرنویس تصاویر
فرمت زیرنویس VobSub اولین فرمت زیرنویس تصویری است که به Matroska وارد شده است. این فرمت با صادرات زیرنویس ها از یک DVD تولید می شود. اگر VobSub از مجموعه‌ای از جریان‌های متعدد تشکیل شده باشد، باید هنگام ذخیره در Matroska، آهنگ‌ها از هم جدا شوند.

### زیرنویس SRT
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. عددی که دنباله زیرنویس را نشان می دهد.
 2. زمان ظاهر شدن و ناپدید شدن زیرنویس روی صفحه نمایش.
 3. خود زیرنویس.
 4. یک خط خالی برای نشان دادن شروع زیرنویس بعدی.
 
### زیرنویس SSA/ASS
Sub Station Alpha (SSA) یک فرمت فایل است که توسط ویرایشگر محبوب زیرنویس SubStation Alpha استفاده می شود. زیرنویس SSA به طور گسترده توسط fansubbers استفاده می شود. قابلیت نمایش ویژگی های مدرن مانند کارائوکه، موقعیت یابی، استایل و غیره را دارد.
 
### زیرنویس WebVTT
کنسرسیوم وب جهانی (W3C) WebVTT را توسعه داد که به اختصار «فرمت تراک‌های متن ویدیوی وب» نامیده می‌شود. این فرمت برای علامت‌گذاری منابع مسیر متن خارجی در ارتباط با عنصر HTML استفاده می‌شود.

### زیرنویس گرافیکی ارائه HDMV
فرمت زیرنویس گرافیکی ارائه HDMV (HDMV PGS) یک سری بیت مپ است و اصلاً نمی توانیم آن را متن بگوییم. به عبارت دیگر، می توان گفت که این فقط یک توالی زمان بندی شده از تصاویر گرافیکی است. برای استخراج اطلاعات، تبدیل PGS به SRT یک فرآیند ضروری است.

### زیرنویس متنی HDMV
متن HDMV به عنوان فرمت زیرنویس متنی مورد استفاده در Blu-ray شناخته می شود. Matroska فقط به مجموعه کاراکترهای UTF-8 اجازه می دهد وقتی زیرنویس TextST را ذخیره می کند.

زیرنویس ### Digital Video Broadcasting (DVB).
فرمت زیرنویس DVB برای تنظیم انتقال و نمایش چندین زبان زیرنویس در سیگنال های تلویزیون معرفی شد. یک فرمت معمولی زیرنویس همچنین به هر بیننده ای اجازه می دهد تا پیام های زیرنویس DVB را تماشا کند، صرف نظر از اینکه سازنده سیستم های انتقال کدام است.


## منابع ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

