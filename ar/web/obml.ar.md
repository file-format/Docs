{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف OBML - ملف Opera Mini المحفوظ لصفحة الويب" ,
  "description" :"تعرف على ما هو ملف OBML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف OBML وفتحه." ,
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2022-05-19"
}

## ما هو ملف OBML؟

ملف OBML (Opera Binary Markup Language) هو نسخة غير متصلة بالإنترنت من صفحة ويب محفوظة بواسطة متصفح الويب Opera Mini للجوال. إنها نسخة مضغوطة قائمة بذاتها من ملفات [HTML] (/ar/ web / html /) التي تحتوي على جميع عناصر الصفحة للعرض على أجهزة معينة أثناء عدم الاتصال بالإنترنت. تمت ترقية تنسيق ملف OBML إلى عدة إصدارات مع استخدام OBML15 و OBML16 بشكل عام. هناك نقطة مهمة يجب مراعاتها وهي أن كل إصدار من Opera Mini متوافق فقط مع تنسيق OBML واحد. وبالتالي ، فإن ترقية Opera Mini ستجعل الصفحات المحفوظة مسبقًا قابلة للقراءة. يمكن تحويل ملفات OBML إلى HTML و [PDF] (/ar/ pdf /).

## تنسيق ملف OBML

يتم حفظ تنسيق ملف OBML بتنسيق ملف خاص بـ Opera ولا تتوفر مواصفات تنسيق الملف الخاصة به للجمهور. ومع ذلك ، تم إجراء هندسة عكسية [تنسيق OMBL] (https://github.com/grawity/obml-parser/blob/master/obml.md) لفك تشفير هيكلها على النحو التالي.

### أنواع بيانات OBML

وفقًا لنتائج الهندسة العكسية ، يستخدم OBML الأنواع الأولية التالية:

* "بايت" - عدد صحيح بدون إشارة (1 بايت)
* "قصير" - عدد صحيح بإشارة (2 بايت ، ذو قيمة كبيرة)
* "متوسط" - عدد صحيح بإشارة (3 بايت ، كبير Endian)
 * `blob` – { length: short, data: byte[length] }
* `char` - بايت يحتوي على حرف ASCII
* `سلسلة` - blob يحتوي على نص مُرمّز UTF-8

### رأس OBML

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
## مراجع

* [تنسيق OMBL] (https://github.com/grawity/obml-parser/blob/master/obml.md)

