{
"ngày": "27-09-2023",
  "keywords": [
"cfg",
"tệp cfg",
"tệp ngôn ngữ đánh dấu cfg wesnoth",
"tập tin cfg là gì",
"cách mở tệp cfg",
"tài liệu",
"phần mở rộng tập tin cfg",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CFG - Tệp ngôn ngữ đánh dấu Wesnoth",
  "description":"Tìm hiểu về định dạng Tệp Ngôn ngữ Đánh dấu CFG Wesnoth và các API có thể tạo và mở tệp CFG.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Tập tin CFG là gì?

Tệp CFG còn được gọi là **"Ngôn ngữ đánh dấu Wesnoth" (WML)**. Đây là ngôn ngữ đánh dấu tùy chỉnh được sử dụng chủ yếu trong trò chơi "Battle for Wesnoth", một trò chơi chiến lược theo lượt. WML được sử dụng để xác định và tùy chỉnh các khía cạnh khác nhau của trò chơi, bao gồm các kịch bản, chiến dịch, đơn vị, v.v. Đó là một cách để các modder và nhà phát triển tạo ra nội dung cho trò chơi.

Nó được viết ở định dạng giống như sự kết hợp giữa XML và tập lệnh đơn giản. Dưới đây là tổng quan về một số thành phần và cấu trúc phổ biến mà bạn có thể tìm thấy trong tệp WML:

1. **Thẻ:** WML sử dụng thẻ để xác định các thành phần khác nhau trong trò chơi. Thẻ được đặt trong dấu ngoặc nhọn. Ví dụ:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Thuộc tính:** Trong thẻ, bạn có thể xác định các thuộc tính để chỉ định các thuộc tính hoặc giá trị được liên kết với phần tử. Trong ví dụ trên, "loại" và "điểm nhấn" là các thuộc tính.
    










3. **Mảng và mảng mảng:** Bạn có thể tạo mảng dữ liệu và thậm chí cả mảng mảng để xác định danh sách đơn vị, loại địa hình hoặc các thành phần trò chơi khác.
    










4. **Câu lệnh có điều kiện:** WML hỗ trợ các câu lệnh có điều kiện để kiểm soát luồng trò chơi. Ví dụ:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Vòng lặp:** Bạn có thể sử dụng vòng lặp để lặp qua danh sách các mục hoặc thực hiện các hành động lặp đi lặp lại.
    










6. **Bao gồm:** Bạn có thể bao gồm các tệp WML khác trong tệp WML chính để sắp xếp và mô-đun hóa nội dung của mình.
    










7. **Trình xử lý sự kiện:** Bạn có thể xác định trình xử lý sự kiện để kích hoạt các hành động khi các sự kiện cụ thể xảy ra trong trò chơi.
    











Dưới đây là ví dụ đơn giản về tệp WML xác định đơn vị tùy chỉnh:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Trận chiến Wesnoth

"The Battle for Wesnoth" là một trò chơi chiến lược theo lượt mã nguồn mở và phổ biến. Nó có sẵn cho nhiều nền tảng, bao gồm Mac, Windows, Linux, v.v. Được phát triển bởi một cộng đồng tình nguyện viên tận tâm, trò chơi này nổi tiếng với lối chơi sâu sắc và hấp dẫn cũng như thế giới giả tưởng phong phú.

Các tính năng chính của "Trận chiến vì Wesnoth" bao gồm:

1. **Bối cảnh giả tưởng:** Trò chơi lấy bối cảnh trong một thế giới giả tưởng với nhiều chủng tộc khác nhau, bao gồm con người, yêu tinh, người lùn, Orc, v.v. Truyền thuyết và cách kể chuyện của trò chơi là một phần không thể thiếu tạo nên sự hấp dẫn của nó.
    










2. **Chiến lược theo lượt:** Lối chơi theo lượt, trong đó người chơi dành thời gian để lên kế hoạch và thực hiện các bước di chuyển của mình trên các lưới lục giác. Nó kết hợp chiến đấu chiến thuật với việc ra quyết định chiến lược.
    










3. **Chiến dịch:** Trò chơi cung cấp nhiều chiến dịch chơi đơn, mỗi chiến dịch có cốt truyện, nhân vật và thử thách riêng. Người chơi có thể khám phá các câu chuyện và kịch bản khác nhau.
    










4. **Nhiều người chơi:** "Wesnoth" hỗ trợ nhiều người chơi trực tuyến, cho phép người chơi cạnh tranh với nhau trong các trận chiến chiến lược. Chế độ nhiều người chơi bao gồm chơi hợp tác và các trận đấu cạnh tranh.

## Làm cách nào để mở tập tin CFG?

Các tệp CFG, thường được liên kết với Ngôn ngữ đánh dấu Wesnoth (WML) được sử dụng trong trò chơi "Trận chiến vì Wesnoth", có thể dễ dàng chỉnh sửa bằng bất kỳ trình soạn thảo văn bản tiêu chuẩn nào. Các tệp này chứa mã mà con người có thể đọc được được viết bằng WML, mã này xác định các khía cạnh khác nhau của trò chơi, bao gồm các kịch bản, đơn vị và chiến dịch.

Mặc dù bạn có thể sử dụng bất kỳ trình soạn thảo văn bản nào để sửa đổi các tệp CFG, nhưng một số trình soạn thảo văn bản nâng cao như Emacs và Vi có sẵn các plugin tô sáng cú pháp WML. Các plugin này cung cấp mã hóa màu và định dạng hữu ích để giúp người dùng dễ dàng phân biệt các thành phần và cấu trúc khác nhau trong mã WML.

Các chương trình mở hoặc tham chiếu tệp CFG bao gồm

- Trận chiến vì Wesnoth (Miễn phí) cho (Windows, MAC, Linux)
- Microsoft Notepad

## Các tập tin CFG khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.cfg**.

**Cài đặt**
- [CFG - Tệp cấu hình Celestia](/vi/settings/cfg-celestia/)
- [CFG - Tệp kết nối máy chủ Citrix](/vi/settings/cfg-citrix/)
- [CFG - Tệp cấu hình MAME](/vi/settings/cfg-mame/)
- [CFG - Tệp cấu hình LightWave](/vi/settings/cfg-lightwave/)

**Trò chơi**
- [CFG - Tệp ngôn ngữ đánh dấu Wesnoth](/vi/game/cfg-wesnoth/)
- [CFG - Tệp cấu hình MUGEN](/vi/game/cfg-mugen/)
- [CFG - Tệp cấu hình công cụ nguồn](/vi/game/cfg-sourceengine/)

**Hệ thống & Linh tinh**
- [Tệp CFG - CFG](/vi/system/cfg/)
- [CFG - Tệp cấu hình mô hình Cal3D](/vi/misc/cfg-cal3d/)

## Người giới thiệu
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
