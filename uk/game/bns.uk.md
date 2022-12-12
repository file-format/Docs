{
  "date" : "2021-10-20",
  "keywords" :[ "файл bns", "формат файлу bns", "що таке файл bns", "файл", "приклад bns", "розширення файлу сценарію бонусної карти порталу", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу BNS сценарію бонусної карти ortal та API, які можуть створювати та відкривати файли BNS.",
  "title" :"BNS - файл сценарію бонусної карти порталу",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Що таке файл BNS?

Файл із розширенням .bns — це файл сценарію гри, створений за допомогою гри-головоломки Portal Map, розробленої Valve. Він містить текстовий сценарій для визначення інформації про карту порталу, яка зберігається як файл .bsp. Файли BNS використовуються як посилання на цей фактичний файл карти та містять список завдань, які потрібно виконати. Крім того, він містить назву карти, коментарі до карти та посилання на файл мініатюр. Файл BNS можна відкрити в будь-якому текстовому редакторі, наприклад Notepad++, textEdit і Notepad.

## Формат файлу BNS

Файли BNS зберігаються як звичайні текстові файли, які легко читаються людиною. Їх можна відкривати в текстових редакторах і також редагувати. Однак їх слід ретельно відредагувати, щоб уникнути помилок у сценарії.

## Приклад формату файлу BNS

Файл BNS може виглядати приблизно так, коли його відкривають у текстовому редакторі, наприклад Notepad++.

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

## Частини файлу BNS

У наведеному вище прикладі

* `#Bonus_Map_Challenges` - представляє назву карти.
* `map` - представляє назву карти, яка буде розміщена в папці карт гри
* `chapter` - представляє розділ, до якого належить карта. Усі файли розділів розміщуються у файлі VPK шляхом додавання назви карти у форматі `map your_map_name`
* `Зображення` – містить мініатюру карти та зберігається в кореневому шляху steam\steamapps\common\portal\portal\materials\VGUI.
* `Коментар` - текст опису створеної карти.

## Список літератури

* [Сценарій виклику порталу](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

