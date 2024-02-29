{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل OBML - فایل صفحه وب ذخیره شده Opera Mini",
  "description": "درباره اینکه فایل OBML چیست و APIهایی که می توانند فایل OBML را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-fal"
}
}،
  "lastmod": "2022-05-19"
}

## فایل OBML چیست؟

فایل OBML (Opera Binary Markup Language) یک نسخه آفلاین از یک صفحه وب است که توسط مرورگر وب موبایل Opera Mini ذخیره شده است. این یک نسخه فشرده و مستقل از فایل‌های [HTML](/web/html/) است که حاوی تمام عناصر صفحه برای نمایش در دستگاه‌های خاص در حالت آفلاین است. فرمت فایل OBML به چندین نسخه با OBML15 و OBML16 ارتقا یافته است. نکته مهمی که باید در نظر داشت این است که هر نسخه Opera Mini فقط با یک فرمت OBML سازگار است. بنابراین، ارتقاء Opera Mini صفحات ذخیره شده قبلی را خوانا می کند. فایل های OBML را می توان به HTML و [PDF](/pdf/) تبدیل کرد.

## فرمت فایل OBML

فرمت فایل OBML در فرمت فایل اختصاصی Opera ذخیره شده است و مشخصات فرمت فایل آن به صورت عمومی در دسترس نیست. با این حال، [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) برای رمزگشایی ساختار خود به صورت زیر مهندسی معکوس شد.

### انواع داده های OBML

طبق نتایج مهندسی معکوس، OBML از انواع اولیه زیر استفاده می کند:

 * بایت - عدد صحیح بدون علامت (1 بایت)
 * «کوتاه» – عدد صحیح امضا شده (2 بایت، big-endian)
 * متوسط - عدد صحیح امضا شده (3 بایت، big-endian)
 * `blob` – { طول: کوتاه، داده: بایت[طول]}
 * char - یک بایت حاوی یک کاراکتر ASCII
 * رشته - یک حباب حاوی متن کدگذاری شده UTF-8

### سربرگ OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## منابع

* [قالب OMBL] (https://github.com/grawity/obml-parser/blob/master/obml.md)


