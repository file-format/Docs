{
  "date" : "2021-10-20",
  "keywords" :[ "файл bns", "формат файла bns", "что такое файл bns", "файл", "пример bns", "расширение файла скрипта бонусной карты портала", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла BNS ortal Bonus Map Script и API, которые могут создавать и открывать файлы BNS.",
  "title" :"BNS - Файл скрипта бонусной карты портала",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .BNS вариант №

Файл с расширением .bns представляет собой файл сценария игры, созданный с помощью игры-головоломки Portal Map, разработанной Valve. Он содержит текстовый скрипт для определения информации о карте портала, которая хранится в виде файла .bsp. Файлы BNS используются в качестве ссылки на этот фактический файл карты и содержат список задач, которые необходимо выполнить. Кроме того, он содержит название карты, комментарии к карте и ссылки на файлы эскизов изображений. Файл BNS можно открыть в любом текстовом редакторе, таком как Notepad++, textEdit и Notepad.

## Формат файла BNS

Файлы BNS сохраняются в виде простых текстовых файлов, понятных человеку. Их можно открывать в текстовых редакторах и редактировать. Однако их следует тщательно редактировать, чтобы избежать ошибок в сценарии.

## Пример формата файла BNS

Файл BNS может выглядеть примерно так, когда он открыт в текстовом редакторе, таком как Notepad++.

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

## Части файла BNS

В приведенном выше примере

* `#Bonus_Map_Challenges` — представляет название карты.
* `map` - Представляет имя карты, которую нужно поместить в папку с картами игры.
* `chapter` — представляет главу, к которой принадлежит карта. Все файлы глав находятся в файле VPK путем добавления имени карты в формате `map your_map_name`
* `Изображение` — содержит миниатюру карты и хранится в корневом каталоге steam\steamapps\common\portal\portal\materials\VGUI.
* `Комментарий` - Описательный текст о созданной карте.

## использованная литература

* [Сценарий испытания портала](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

