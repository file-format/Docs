{
"date" :  "2023-07-20",
   "keywords":[
"THÙNG RÁC",
"Tệp BIN",
"tài liệu",
"Phần mở rộng tệp BIN",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp BIN - Tệp được mã hóa MacBinary",
   "description":"Tìm hiểu về định dạng BIN và các API có thể tạo và mở tệp BIN.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Tệp BIN là gì?

Tệp BIN, trong ngữ cảnh của máy tính Macintosh, có thể đề cập đến tệp được lưu ở định dạng MacBinary. MacBinary là định dạng tệp được thiết kế đặc biệt để truyền tệp Macintosh qua internet, email, FTP hoặc phương tiện di động. Mục đích của MacBinary là duy trì cấu trúc tệp hoàn chỉnh và các thuộc tính của tệp Macintosh, bao gồm cả nhánh dữ liệu và nhánh tài nguyên, trong một tệp duy nhất.

Định dạng MacBinary đạt được điều này bằng cách đóng gói nhánh tài nguyên và nhánh dữ liệu của Hệ thống tệp phân cấp Macintosh (HFS) vào một tệp nén. Nó cũng bao gồm tiêu đề công cụ tìm chứa siêu dữ liệu quan trọng về tệp. Bằng cách kết hợp tất cả các thành phần này vào một tệp, MacBinary đảm bảo rằng tệp vẫn giữ được tính toàn vẹn và có thể dễ dàng chuyển và chia sẻ trên các nền tảng khác nhau.

Với những tiến bộ trong hệ thống tệp và giao thức truyền tệp của Apple, việc sử dụng tệp BIN và định dạng MacBinary đã trở nên ít phổ biến hơn. Việc giới thiệu các định dạng tệp như ZIP và chuyển đổi sang các hệ thống tệp hiện đại hơn, chẳng hạn như HFS+ và APFS, đã làm giảm nhu cầu về các tệp được mã hóa MacBinary. Các hệ thống tệp mới hơn này cung cấp các cách xử lý thuộc tính tệp, phân nhánh tài nguyên và phân nhánh dữ liệu hiệu quả hơn, làm cho định dạng MacBinary ít cần thiết hơn trong bối cảnh điện toán ngày nay.

## Định dạng tệp BIN - Thông tin thêm

Trong những ngày đầu của máy tính Macintosh, các tệp được lưu trữ ở hai "nhánh" riêng biệt do hạn chế về dữ liệu. "Ngã ba tài nguyên" chứa dữ liệu có cấu trúc, trong khi "ngã ba dữ liệu" chứa dữ liệu phi cấu trúc. Mặc dù Classic Mac OS coi các nhánh này là một tệp duy nhất, nhưng việc chuyển tệp sang các hệ thống không phải máy Mac sẽ dẫn đến mất dữ liệu vì chúng không nhận ra các nhánh này là một thực thể duy nhất. Để giải quyết vấn đề này, định dạng MacBinary được tạo ra bởi các cá nhân như Dennis Brothers, Harry Chesley và Yves Lempereur. MacBinary đã nén và kết hợp các nhánh thành một tệp duy nhất, được gọi là tệp BIN, để chuyển sang các hệ thống không phải máy Mac. Khi quay trở lại Mac OS, các nhánh sẽ lại được tách ra. Với quá trình chuyển đổi khỏi HFS dựa trên ngã ba vào những năm 2000, việc sử dụng định dạng MacBinary đã giảm đáng kể. Ngày nay, việc gặp phải tệp BIN được mã hóa MacBinary là rất hiếm trừ khi bạn gặp một tệp cũ trên hệ thống không phải máy Mac hoặc tải xuống một tệp từ internet.

Định dạng MacBinary đã trải qua nhiều phiên bản theo thời gian để phù hợp với những thay đổi trong hệ thống Macintosh và xử lý tệp. Dưới đây là một số phiên bản khác nhau của định dạng MacBinary:

- **MacBinary I:** Phiên bản đầu tiên của MacBinary, được giới thiệu vào cuối những năm 1980. Nó kết hợp phân nhánh tài nguyên và phân nhánh dữ liệu thành một tệp nhị phân duy nhất, cho phép truyền các tệp Macintosh đa nền tảng.

- **MacBinary II:** Phiên bản này, được phát hành vào đầu những năm 1990, đã cải thiện định dạng MacBinary ban đầu bằng cách thêm thông tin bổ sung, chẳng hạn như loại tệp và mã người tạo, vào tiêu đề của tệp nhị phân. Các mã này giúp duy trì tính toàn vẹn và nhận dạng các tệp Macintosh trong quá trình truyền.

- **MacBinary III:** Định dạng MacBinary III, được giới thiệu vào giữa những năm 1990, đã nâng cao hơn nữa các phiên bản trước đó bằng cách đưa siêu dữ liệu bổ sung, chẳng hạn như tên tệp, ngày tạo và sửa đổi tệp vào tiêu đề của tệp nhị phân. Điều này cho phép bảo toàn toàn diện hơn các thuộc tính tệp Macintosh trong quá trình truyền.

- **MacBinary IV:** MacBinary IV được phát triển để giải quyết các vấn đề tương thích với hệ điều hành Mac OS X mới nổi vào đầu những năm 2000. Nó kết hợp các thay đổi để thích ứng với cấu trúc và thuộc tính hệ thống tệp mới được giới thiệu trong Mac OS X.

## Làm cách nào để mở tệp BIN?

Các tệp BIN được mã hóa MacBinary có thể được mở bằng nhiều tiện ích nén khác nhau. Đối với người dùng macOS, **Tiện ích lưu trữ của Apple** là một lựa chọn phù hợp. Người dùng Windows có thể sử dụng phần mềm như **Smith Micro StuffIt Deluxe** để trích xuất nội dung của tệp BIN được mã hóa MacBinary. Một tùy chọn khác dành cho người dùng macOS là **The Unarchiver**, đây là một công cụ đa năng có khả năng xử lý nhiều định dạng tệp, bao gồm cả MacBinary.

Điều quan trọng cần lưu ý là phần mở rộng tệp .bin được sử dụng bởi nhiều định dạng tệp khác nhau, không chỉ MacBinary. Do đó, nếu bạn gặp phải tệp BIN không thể mở được bằng các tiện ích nói trên, nó có thể được lưu ở định dạng khác. Trong những trường hợp như vậy, bạn có thể cần xác định định dạng tệp cụ thể và sử dụng phần mềm hoặc tiện ích thích hợp được thiết kế cho định dạng đó để truy cập nội dung tệp.

## Các tập tin BIN khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.bin**.

- [BIN - Tệp ảnh đĩa nhị phân](/vi/disc-and-media/bin/)
- [BIN - Tệp thực thi Unix](/vi/executable/bin/)
- [BIN - Tệp chính sách CNTT của BlackBerry](/vi/settings/bin/)
- [BIN - ROM trò chơi Sega Genesis](/vi/game/bin/)
- [BIN - Hình ảnh BIOS PSX PlayStation](/vi/game/bin-pcsx/)

## Người giới thiệu

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

