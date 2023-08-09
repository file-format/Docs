{
  "date" : "2019-10-11",
  "keywords" :[ ".swf", "SWF", "Apple swift", "tệp", "tiện ích mở rộng", "định dạng tệp", "hướng dẫn apple swift", "hướng dẫn lập trình" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SWIFT - Tệp mã nguồn của Apple",
  "description":"Tìm hiểu về định dạng tệp SWIFT và API có thể tạo và mở tệp SWIFT.",
  "linktitle" : "SWIFT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp Swift là gì?

Tệp có phần mở rộng .swift đề cập đến ngôn ngữ lập trình SWIFT do Apple giới thiệu để viết các ứng dụng và ứng dụng phần mềm cho macOS, iOS, tvOS, v.v. Trước SWIFT, Objective-C là ngôn ngữ lập trình chính để viết ứng dụng. Nó có thể được sử dụng với Xcode, một bộ công cụ dành cho nhà phát triển hoàn chỉnh để tạo ứng dụng cho Mac, iPhone, iPad, Apple Watch và Apple TV. SWIFT mạnh mẽ hơn, có tính tương tác, biểu cảm hơn và mang lại sự an toàn hơn theo thiết kế mà không ảnh hưởng đến hiệu suất. Các tệp Swift có thể được mở để chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào ngoài Apple Xcode. Nó hỗ trợ các hệ điều hành của Apple, Linux, Windows và Android.

## Tóm tắt lịch sử

* Bắt đầu phát triển vào giữa năm 2010 bởi Chris Lattner với sự đóng góp của các lập trình viên khác từ Apple
* Ứng dụng chính thức đầu tiên được viết bằng SWIFT đã được phát hành vào ngày 02 tháng 6 năm 2014 tại Hội nghị Nhà phát triển Toàn cầu của Apple (WWDC) và phiên bản Beta của ngôn ngữ này đã được phát hành cho các nhà phát triển đã đăng ký của Apple
* Swift 1.0 được phát hành vào ngày 9 tháng 9 năm 2014 với Xcode của iOS
* Swift 1.1 được phát hành vào ngày 22 tháng 10 năm 2014, cùng với sự ra mắt của Xcode 6.1
* Swift 1.2 được phát hành vào ngày 8 tháng 4 năm 2015, cùng với Xcode 6.3
* Swift 2.0 đã được công bố tại WWDC 2015 và được cung cấp để phát hành ứng dụng trong App Store vào ngày 21 tháng 9 năm 2015.
* Swift 3.0 được phát hành vào ngày 13 tháng 9 năm 2016.
* Swift 4.0 được phát hành vào ngày 19 tháng 9 năm 2017.
* Swift 4.1 được phát hành vào ngày 29 tháng 3 năm 2018.
* Ngôn ngữ Swift được mã nguồn mở vào ngày 3 tháng 12 năm 2015 cùng với các thư viện hỗ trợ, trình gỡ lỗi và trình quản lý gói theo giấy phép Apache 2.0. Dự án được lưu trữ tại [Swift.org](https://swift.org/) và mã nguồn của nó được lưu trữ trên [GitHub](https://github.com/apple/swift).
* Trong WWDC 2019, Apple đã công bố khung SwiftUI cho thiết kế cấu trúc giao diện người dùng trên tất cả các nền tảng của Apple

## Định dạng tệp Swift - Thông tin khác

Các tệp Swift là các tệp văn bản thuần túy có thể được mở bằng bất kỳ trình soạn thảo văn bản nào. Trình soạn thảo văn bản chính được sử dụng để mở và chỉnh sửa các tệp Swift là Xcode của Apple. Nhiều phần của Swift quen thuộc với việc phát triển ứng dụng bằng C và Objective-C. Tài liệu Swift cung cấp [hướng dẫn phát triển ứng dụng](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/) chi tiết để viết mã bằng Swift.

## Tính năng ngôn ngữ Swift

Swift được phân biệt với các ngôn ngữ chương trình khác dựa trên các tính năng sau.

`Modern` - Các tham số được đặt tên được thể hiện bằng một cú pháp rõ ràng giúp các API trong Swift thậm chí còn dễ đọc và dễ bảo trì hơn. Thậm chí tốt hơn, bạn thậm chí không cần gõ dấu chấm phẩy.

`An toàn` - Các biến luôn được khởi tạo trước khi sử dụng, các mảng và số nguyên được kiểm tra xem có tràn không, bộ nhớ được quản lý tự động và việc thực thi quyền truy cập độc quyền vào bộ nhớ bảo vệ chống lại nhiều lỗi lập trình.

`Nhanh và mạnh mẽ` - Sử dụng công nghệ trình biên dịch LLVM hiệu suất cực cao, mã Swift được chuyển đổi thành mã gốc được tối ưu hóa để tận dụng tối đa phần cứng hiện đại.

`Khả năng tương thích nguồn và nhị phân` - Các ứng dụng được phát triển với phiên bản trước của Swift tương thích với các bản phát hành mới và mã nguồn không cần phải biên dịch lại. Với sự ra mắt của Swift 5, các thư viện Swift được bao gồm trong mọi bản phát hành hệ điều hành trong tương lai. Điều này tránh đưa các thư viện Swift vào các ứng dụng nhắm mục tiêu các bản phát hành hệ điều hành hiện tại và tương lai.

`Open Source` - Swift là mã nguồn mở với hàng trăm đóng góp từ các thành viên Cộng đồng Swift. Nó được hỗ trợ bởi trình theo dõi lỗi mạnh mẽ, diễn đàn và các bản dựng phát triển thường xuyên được cung cấp công khai cho mọi người.

## Người giới thiệu
* [Swift - GitHub](https://github.com/apple/swift)
* [Swift - Wikipedia](https://en.wikipedia.org/wiki/Swift_(programming_language))

