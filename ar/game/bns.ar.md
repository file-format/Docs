{
  "date" : "2021-10-20",
  "keywords" :["ملف bns" , "تنسيق ملف bns" , "ما هو ملف bns" , "ملف" , "مثال bns" , "ملحق ملف برنامج نصي لخريطة موقع البوابة" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف ortal Bonus Map Script BNS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات BNS وفتحها." ,
  "title" :"BNS - ملف البرنامج النصي لخريطة موقع المكافأة" ,
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
} ,
  "lastmod" : "2021-10-20"
}

## ما هو ملف BNS؟

الملف ذو الامتداد .bns هو ملف نصي للعبة تم إنشاؤه باستخدام لعبة حل ألغاز Portal Map التي تم تطويرها بواسطة Valve. يحتوي على برنامج نصي لتعريف المعلومات حول مخطط المدخل المخزن كملف .bsp. تُستخدم ملفات BNS كمرجع إلى ملف الخريطة الفعلي هذا وتحتوي على قائمة من التحديات التي يتعين إكمالها. بالإضافة إلى ذلك ، فهو يحتوي على اسم الخريطة وتعليقات حول الخريطة ومراجع ملف الصورة المصغرة. يمكن فتح ملف BNS في أي محرر نصوص مثل Notepad ++ و textEdit و Notepad.

## تنسيق ملف BNS

يتم حفظ ملفات BNS كملفات نصية عادية يمكن للبشر قراءتها. يمكن فتحها في برامج تحرير النصوص وتحريرها أيضًا. ومع ذلك ، يجب تحريرها بعناية لتجنب أي أخطاء في البرنامج النصي.

## مثال على تنسيق ملف BNS

قد يبدو ملف BNS مشابهًا لما يلي عند فتحه في محرر نصي مثل Notepad ++.

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

## أجزاء من ملف BNS

في المثال أعلاه ،

* "# Bonus_Map_Challenges" - يمثل اسم الخريطة.
* "الخريطة" - تمثل اسم الخريطة التي سيتم وضعها في مجلد خرائط اللعبة
* "الفصل" - يمثل الفصل الذي تنتمي إليه الخريطة. توجد جميع ملفات الفصل في ملف VPK عن طريق إضافة اسم الخريطة بالتنسيق `map your_map_name`
* `صورة` - تحتوي على الصورة المصغرة للخريطة ويتم تخزينها في مسار الجذر steam \ steamapps \ common \ portal \ portal \ materials \ VGUI.
* `تعليق` - نص وصفي حول الخريطة التي تم إنشاؤها.

## مراجع

* [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

