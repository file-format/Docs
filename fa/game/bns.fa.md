{
  "date": "2021-10-20",
  "keywords": [
"فایل bns",
"فرمت فایل bns",
"فایل bns چیست",
"فایل",
"bns مثال",
"پسوند فایل نقشه اسکریپت پورتال پاداش",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "در مورد فرمت فایل BNS اسکریپت نقشه پاداش ortal و APIهایی که می‌توانند فایل‌های BNS را ایجاد و باز کنند، بیاموزید.",
  "title": "BNS - فایل اسکریپت نقشه پاداش پورتال",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-fas"
}
}،
  "lastmod": "2021-10-20"
}

## فایل BNS چیست؟

یک فایل با پسوند bns یک فایل اسکریپت بازی است که با بازی حل پازل Portal Map ساخته شده است که توسط Valve ساخته شده است. این شامل اسکریپت متنی برای تعریف اطلاعات در مورد نقشه پورتال است که به صورت فایل bsp. ذخیره می شود. فایل های BNS به عنوان مرجع برای این فایل نقشه واقعی استفاده می شود و شامل لیستی از چالش هایی است که باید تکمیل شوند. علاوه بر این، حاوی نام نقشه، نظرات درباره نقشه، و منابع فایل تصویر بند انگشتی است. یک فایل BNS را می توان در هر ویرایشگر متنی مانند Notepad++، textEdit و Notepad باز کرد.

## فرمت فایل BNS

فایل‌های BNS به‌عنوان فایل‌های متنی ساده و قابل خواندن توسط انسان ذخیره می‌شوند. اینها را می توان در ویرایشگرهای متن باز کرد و همچنین ویرایش کرد. با این حال، این موارد باید با دقت ویرایش شوند تا از هرگونه خطا در اسکریپت جلوگیری شود.

## نمونه فرمت فایل BNS

هنگامی که یک فایل BNS در یک ویرایشگر متنی مانند Notepad++ باز می شود، ممکن است چیزی شبیه به شکل زیر باشد.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## بخش هایی از یک فایل BNS

در مثال بالا،

 * #چالش_نقشه_پاداش - نشان دهنده نام نقشه است.
 * نقشه - نشان دهنده نام نقشه ای است که در پوشه نقشه های بازی قرار می گیرد
 * «فصل» - نمایانگر فصلی است که نقشه به آن تعلق دارد. همه فایل‌های فصل با اضافه کردن نام نقشه در قالب «map your_map_name» در فایل VPK قرار می‌گیرند.
 * «تصویر» - حاوی تصویر کوچک نقشه است و در مسیر اصلی steam\steamapps\common\portal\portal\materials\VGUI ذخیره می‌شود.
 * نظر - متن توصیفی در مورد نقشه ایجاد شده.

## منابع

 * [اسکریپت چالش پورتال](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

