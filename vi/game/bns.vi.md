{
  "date" : "2021-10-20",
  "keywords" :[ "tệp bns", "định dạng tệp bns", "tệp bns là gì", "tệp", "ví dụ bns", "phần mở rộng tệp Script Map Bonus Portal","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp BNS của Bonus Map Script bằng miệng và các API có thể tạo và mở tệp BNS.",
  "title" :"BNS - Tệp tập lệnh bản đồ phần thưởng cổng thông tin",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Tệp BNS là gì?

Tệp có phần mở rộng .bns là tệp kịch bản trò chơi được tạo bằng trò chơi giải câu đố Portal Map do Valve phát triển. Nó chứa tập lệnh văn bản để xác định thông tin về bản đồ Cổng thông tin được lưu trữ dưới dạng tệp .bsp. Các tệp BNS được sử dụng làm tài liệu tham khảo cho tệp bản đồ thực tế này và chứa danh sách các thử thách sẽ được hoàn thành. Ngoài ra, nó chứa tên bản đồ, nhận xét về bản đồ và tham chiếu tệp hình ảnh thu nhỏ. Có thể mở tệp BNS trong bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Notepad ++, textEdit và Notepad.

## Định dạng tệp BNS

Các tệp BNS được lưu dưới dạng tệp văn bản thuần túy mà con người có thể đọc được. Chúng có thể được mở trong trình soạn thảo văn bản và chỉnh sửa. Tuy nhiên, những điều này nên được chỉnh sửa cẩn thận để tránh bất kỳ sai sót nào trong kịch bản.

## Ví dụ về định dạng tệp BNS

Tệp BNS có thể trông giống như sau khi được mở trong trình soạn thảo văn bản, chẳng hạn như Notepad++.

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

## Các phần của tệp BNS

Trong ví dụ trên,

* `#Bonus_Map_Challenges` - Thể hiện tên của bản đồ.
* `map` - Đại diện cho tên của bản đồ sẽ được đưa vào thư mục bản đồ của trò chơi
* `chương` - Biểu thị chương mà bản đồ thuộc về. Tất cả các tệp chương được đặt trong tệp VPK bằng cách thêm tên của bản đồ ở định dạng `map your_map_name`
* `Hình ảnh` - Nó chứa hình thu nhỏ của bản đồ và được lưu trữ tại đường dẫn gốc steam\steamapps\common\portal\portal\materials\VGUI.
* `Nhận xét` - Đoạn văn miêu tả về bản đồ đã tạo.

## Người giới thiệu

* [Tập lệnh thử thách cổng thông tin](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

