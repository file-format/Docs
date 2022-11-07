{
  "date" : "2021-10-20",
  "keywords" :[ "bns ファイル","bns ファイル形式","bns ファイルとは","ファイル","bns の例","Portal Bonus Map Script ファイルの拡張子","拡張子","形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"ortal Bonus Map Script BNS ファイル形式と,BNS ファイルを作成して開くことができる API について学びます。",
  "title" :"BNS - ポータル ボーナス マップ スクリプト ファイル",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .BNS オプション番号

拡張子が .bns のファイルは、Valve が開発したポータル マップ パズル解決ゲームで作成されたゲーム スクリプト ファイルです。これには、.bsp ファイルとして保存されるポータル マップに関する情報を定義するためのテキスト スクリプトが含まれています。 BNS ファイルは、この実際のマップ ファイルへの参照として使用され、完了する必要のある課題のリストが含まれています。さらに、マップ名、マップに関するコメント、およびサムネイル画像ファイルの参照が含まれています。 BNS ファイルは、Notepad++、textEdit、Notepad などの任意のテキスト エディターで開くことができます。

## BNS ファイル形式

BNS ファイルは、人間が判読できるプレーン テキスト ファイルとして保存されます。これらは、テキスト エディターで開いて編集することもできます。ただし、スクリプトでエラーが発生しないように、これらは慎重に編集する必要があります。

## BNS ファイル形式の例

BNS ファイルを Notepad++ などのテキスト エディタで開くと、次のようになります。

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

## BNS ファイルの一部

上記の例では、

* `#Bonus_Map_Challenges` - マップの名前を表します。
* `map` - ゲームのマップ フォルダに入れるマップの名前を表します
* `chapter` - マップが属する章を表します。すべてのチャプター ファイルは、マップの名前を `map your_map_name` の形式で追加することにより、VPK ファイルに配置されます。
* `Image` - マップのサムネイルを含み、ルート パス steam\steamapps\common\portal\portal\materials\VGUI に保存されます。
* `Comment` - 作成されたマップに関する説明テキスト。

## 参考文献

* [ポータル チャレンジ スクリプト](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

