{
  "date" : "2021-10-20",
  "keywords" :["plik bns", "format pliku bns", "co to jest plik bns", "plik", "przykład bns", "Rozszerzenie pliku skryptu mapy bonusowej portalu", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku Ortal Bonus Map Script BNS i interfejsach API, które mogą tworzyć i otwierać pliki BNS.",
  "title" :"BNS - plik skryptu mapy bonusowej portalu",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Czym jest plik BNS?

Plik z rozszerzeniem .bns to plik skryptu gry utworzony za pomocą gry polegającej na rozwiązywaniu łamigłówek mapy portalu opracowanej przez firmę Valve. Zawiera skrypt tekstowy służący do definiowania informacji o mapie Portalu, który jest przechowywany jako plik .bsp. Pliki BNS są używane jako odniesienie do tego rzeczywistego pliku mapy i zawierają listę wyzwań, które należy wykonać. Ponadto zawiera nazwę mapy, komentarze dotyczące mapy i odniesienia do plików miniatur. Plik BNS można otworzyć w dowolnym edytorze tekstu, takim jak Notepad ++, textEdit i Notatnik.

## Format pliku BNS

Pliki BNS są zapisywane jako zwykłe pliki tekstowe, które są czytelne dla człowieka. Można je otwierać w edytorach tekstu i edytować. Należy je jednak starannie edytować, aby uniknąć błędów w skrypcie.

## Przykład formatu pliku BNS

Plik BNS może wyglądać podobnie do poniższego, gdy zostanie otwarty w edytorze tekstu, takim jak Notepad ++.

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

## Części pliku BNS

W powyższym przykładzie

* `#Bonus_Map_Challenges` - Reprezentuje nazwę mapy.
* `map` - Reprezentuje nazwę mapy, która ma zostać umieszczona w folderze map gry
* `rozdział` — reprezentuje rozdział, do którego należy mapa. Wszystkie pliki rozdziałów znajdują się w pliku VPK poprzez dodanie nazwy mapy w formacie `map your_map_name`
* `Obraz` — zawiera miniaturę mapy i jest przechowywany w ścieżce głównej steam\steamapps\common\portal\portal\materials\VGUI.
* `Komentarz` - Tekst opisujący stworzoną mapę.

## Bibliografia

* [Skrypt wyzwania portalu](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

