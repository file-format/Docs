{
  "date": "2021-10-20",
  "keywords": [
"bns faylı",
"bns fayl formatı",
"bns faylı nədir",
"fayl",
"bns misal",
"Portal Bonus Xəritə Skripti fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "BNS faylları yarada və aça bilən orta Bonus Map Script BNS fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "BNS - Portal Bonus Xəritə Skript Faylı",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-azs"
}
},
  "lastmod": "2021-10-20"
}

## BNS faylı nədir?

.bns uzantılı fayl Valve tərəfindən hazırlanmış Portal Xəritə tapmacalarının həlli oyunu ilə yaradılmış oyun skript faylıdır. O, .bsp faylı kimi saxlanılan Portal xəritəsi haqqında məlumatı müəyyən etmək üçün mətn skriptini ehtiva edir. BNS faylları bu faktiki xəritə faylına istinad kimi istifadə olunur və tamamlanmalı olan problemlərin siyahısını ehtiva edir. Bundan əlavə, xəritə adı, xəritə haqqında şərhlər və kiçik şəkil faylı istinadlarını ehtiva edir. BNS faylı Notepad++, textEdit və Notepad kimi istənilən mətn redaktorunda aça bilər.

## BNS fayl formatı

BNS faylları insanların oxuna biləcəyi düz mətn faylları kimi saxlanılır. Bunlar mətn redaktorlarında açıla və redaktə edilə bilər. Bununla belə, skriptdə səhvlərin qarşısını almaq üçün bunlar diqqətlə redaktə edilməlidir.

## BNS fayl formatı nümunəsi

BNS faylı Notepad++ kimi mətn redaktorunda açıldıqda aşağıdakı kimi görünə bilər.

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

## BNS faylının hissələri

Yuxarıdakı misalda,

 * `#Bonus_Map_Challenges` - Xəritənin adını təmsil edir.
 * `xəritə` - Oyunun xəritələr qovluğuna qoyulacaq xəritənin adını təmsil edir
 * `fəsil` - Xəritənin aid olduğu fəsli təmsil edir. Bütün fəsil faylları xəritənin adını `map your_map_name` formatında əlavə etməklə VPK faylında yerləşdirilir.
 * `Şəkil` - O, xəritənin miniatürünü ehtiva edir və steam\steamapps\common\portal\portal\materials\VGUI kök yolunda saxlanılır.
 * `Şərh` - Yaradılmış xəritə haqqında təsviri mətn.

## İstinadlar

 * [Portal Çağırış Skripti](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

