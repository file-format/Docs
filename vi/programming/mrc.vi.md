{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "file", "extension", "file format", "mrc implementation", "Programming Guide", "mrc example", "mIRC", "mIRC scripting language", "files of INI", " mSL scripting language", "mIRC language", "mIRC scripts", "scripting language" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - Tệp ngôn ngữ tập lệnh mIRC",
  "description":"Tìm hiểu về định dạng tệp MRC và các API có thể tạo và mở tệp MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Tệp MRC là gì?

mIRC là ngôn ngữ kịch bản được nhúng dưới dạng ứng dụng khách IRC (Trò chuyện chuyển tiếp qua Internet) trong hệ điều hành Windows. Nó cung cấp một cơ sở bảo vệ khỏi gửi thư rác cho mục đích sử dụng cá nhân và kênh. Để cung cấp trải nghiệm tốt hơn về khả năng tương thích của người dùng, ngôn ngữ kịch bản mIRC này cho phép tạo các cửa sổ hội thoại. Các tệp chứa tập lệnh, hầu hết ở định dạng văn bản thuần túy được lưu trữ với phần mở rộng là MRC hoặc dưới dạng tệp của [INI](/vi/system/ini/). Các chức năng của ngôn ngữ này được gọi là lệnh và mã định danh (khi chúng trả về giá trị).

Ngôn ngữ mIRC cung cấp khả năng tải nhiều tệp tập lệnh cùng một lúc. Mặt khác, một tệp có thể khiến tệp kia không còn được sử dụng khi được tải đồng thời. Các lệnh được lưu và chúng có thể tự động tồn tại trong IRC. Các lệnh và bí danh được sử dụng trong ngôn ngữ này không bao gồm quyền ưu tiên của bất kỳ ký tự nào.

mIRC được sử dụng rộng rãi để làm cho các bot tự động quản lý kênh nhưng nó cũng có thể được sửa đổi bằng ngôn ngữ kịch bản mSL. Nó có thể giới thiệu nhiều tính năng mới như macro, khả năng phát nhạc, macro và chức năng nhỏ, trò chơi cơ bản hoặc vận hành các ứng dụng nhỏ.


## Lược Sử ##

Ngôn ngữ kịch bản này được phát triển lần đầu tiên vào năm 1995 bởi Khaled Adam Bey. Thiết kế của ngôn ngữ kịch bản cũng được tạo ra bởi Khalid. Mục tiêu của ngôn ngữ này là lập trình hướng sự kiện. Ban đầu, phần mở rộng tệp được sử dụng cho các tệp của ngôn ngữ lập trình này là .mrc và .ini. Hơn nữa, nó được phát triển theo giấy phép của phần mềm độc quyền.

## Đặc điểm kỹ thuật ##

Một số chức năng được viết kịch bản tùy chỉnh thông qua ngôn ngữ mIRC này và được gọi là bí danh. Khi những bí danh này trả về giá trị, chúng được gọi là số nhận dạng tùy chỉnh. Tất cả các biến có trong ngôn ngữ mIRC này đều được nhập động. Dấu hiệu được sử dụng bởi các tập lệnh mIRC. Một tính năng khác của ngôn ngữ kịch bản này là cửa sổ bật lên. Người dùng có thể gọi cửa sổ bật lên bằng cách chọn chúng. Điều khiển từ xa được chỉ định cho các sự kiện nhất định. Điều khiển từ xa được gọi khi sự kiện tương đối xảy ra.

Các mã thông báo được phân cách bằng dấu cách được sử dụng để ngắt từng dòng mã của ngôn ngữ này. Có một số phần mở rộng phổ biến khác được sử dụng cho các tệp mIRC như MDX (Phần mở rộng hộp thoại mIRC) và DCX (Phần mở rộng điều khiển hộp thoại). Cả hai đều là phần mở rộng đối thoại và tương đối phổ biến hơn. Các cấu trúc ngôn ngữ được gọi bằng danh pháp của ngôn ngữ kịch bản này. Ngôn ngữ mIRC liên quan đến các khía cạnh khác nhau của ngôn ngữ kịch bản chẳng hạn như biến cục bộ và biến toàn cục, biến nhị phân, bảng băm và xử lý tệp.


## Ví dụ về định dạng tệp MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/vi/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Tài liệu tham khảo ##

* [MIRC - theo Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



