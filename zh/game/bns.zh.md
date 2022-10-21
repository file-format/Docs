{
  "date" : "2021-10-20",
  "keywords" :["bns 文件","bns 文件格式","什么是 bns 文件","文件","bns 示例","门户奖励地图脚本文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 ortal Bonus Map Script BNS 文件格式和可以创建和打开 BNS 文件的 API。",
  "title" :"BNS - 门户奖励地图脚本文件",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## 什么是一 .bns 文件？

扩展名为 .bns 的文件是由 Valve 开发的 Portal Map 解谜游戏创建的游戏脚本文件。它包含用于定义存储为 .bsp 文件的门户地图信息的文本脚本。 BNS 文件用作此实际地图文件的参考，并包含要完成的挑战列表。此外，它还包含地图名称、有关地图的注释和缩略图文件引用。 BNS 文件可以在任何文本编辑器中打开，例如 Notepad++、textEdit 和 Notepad。

## BNS 文件格式

BNS 文件保存为人类可读的纯文本文件。这些可以在文本编辑器中打开并进行编辑。但是，应仔细编辑这些内容以避免脚本中的任何错误。

## BNS 文件格式示例

BNS 文件在 Notepad++ 等文本编辑器中打开时可能如下所示。

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

## BNS 文件的一部分

在上面的例子中，

* `#Bonus_Map_Challenges` - 代表地图的名称。
* `map` - 表示要放入游戏地图文件夹中的地图名称
* `chapter` - 表示地图所属的章节。通过以`map your_map_name`格式添加地图名称，所有章节文件都位于VPK文件中
* `Image` - 它包含地图的缩略图并存储在根路径 steam\steamapps\common\portal\portal\materials\VGUI。
* `Comment` - 关于创建的地图的描述性文本。

## 参考

* [传送门挑战脚本](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

