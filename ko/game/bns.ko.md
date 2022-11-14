{
  "date" : "2021-10-20",
  "keywords" :[ "bns 파일", "bns 파일 형식", "bns 파일이란", "파일", "bns 예제", "포털 보너스 맵 스크립트 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"BNS 파일을 만들고 열 수 있는 ortal Bonus Map Script BNS 파일 형식과 API에 대해 알아보세요.",
  "title" :"BNS - 포털 보너스 맵 스크립트 파일",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .BNS 파일이란?

확장자가 .bns인 파일은 밸브에서 개발한 Portal Map 퍼즐 풀기 게임으로 만든 게임 스크립트 파일입니다. 여기에는 .bsp 파일로 저장된 포털 맵에 대한 정보를 정의하기 위한 텍스트 스크립트가 포함되어 있습니다. BNS 파일은 이 실제 지도 파일에 대한 참조로 사용되며 완료해야 하는 챌린지 목록이 포함되어 있습니다. 또한 지도 이름, 지도에 대한 설명 및 썸네일 이미지 파일 참조가 포함됩니다. BNS 파일은 메모장++, textEdit 및 메모장과 같은 모든 텍스트 편집기에서 열 수 있습니다.

## BNS 파일 형식

BNS 파일은 사람이 읽을 수 있는 일반 텍스트 파일로 저장됩니다. 텍스트 편집기에서 열고 편집할 수도 있습니다. 그러나 스크립트에 오류가 발생하지 않도록 주의 깊게 편집해야 합니다.

## BNS 파일 형식 예

BNS 파일을 메모장++과 같은 텍스트 편집기에서 열면 다음과 같이 보일 수 있습니다.

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

## BNS 파일의 일부

위의 예에서,

* `#Bonus_Map_Challenges` - 지도의 이름을 나타냅니다.
* `map` - 게임의 지도 폴더에 넣을 지도의 이름을 나타냅니다.
* `챕터` - 맵이 속한 챕터를 나타냅니다. 모든 챕터 파일은 `map your_map_name` 형식으로 지도 이름을 추가하여 VPK 파일에 있습니다.
* `이미지` - 맵의 썸네일을 포함하며 루트 경로 steam\steamapps\common\portal\portal\materials\VGUI에 저장됩니다.
* `설명` - 생성된 지도에 대한 설명 텍스트입니다.

## 참고문헌

* [포털 챌린지 스크립트](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

