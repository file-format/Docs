{
"ngày": "2023-02-02",
  "keywords": [
"tệp ứng dụng",
"tệp ứng dụng là gì",
"tài liệu",
"cách mở tệp ứng dụng",
"phần mở rộng tệp ứng dụng",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Tìm hiểu về định dạng tệp APP và các API có thể tạo và mở tệp APP.",
"title": "Định dạng tệp APP - Gói ứng dụng macOS",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Tệp ứng dụng là gì?

Tệp .app trên macOS là một loại thư mục đặc biệt chứa tất cả các tệp cần thiết để chạy một ứng dụng cụ thể, bao gồm mã thực thi, tài nguyên và siêu dữ liệu. Tiện ích mở rộng .app báo hiệu cho hệ điều hành rằng thư mục này phải được coi là một đơn vị duy nhất, thay vì một tập hợp các tệp riêng biệt và nó có thể được khởi chạy trực tiếp từ Finder hoặc Dock.

Finder là ứng dụng quản lý file mặc định trên macOS. Nó cho phép bạn duyệt và sắp xếp các tập tin và thư mục trên máy tính của bạn. Dock là một tính năng của macOS giúp truy cập nhanh vào các ứng dụng và tài liệu được sử dụng thường xuyên. Cả Finder và Dock đều cho phép bạn khởi chạy ứng dụng bằng cách nhấp vào tệp .app của chúng, thao tác này sẽ mở gói ứng dụng tương ứng. Khi bạn khởi chạy một ứng dụng, mã thực thi trong gói .app sẽ được chạy, giúp ứng dụng có sẵn để sử dụng. Tệp .app là sự thể hiện của ứng dụng trên hệ thống tệp và cung cấp cách để người dùng truy cập và khởi chạy ứng dụng.

Khi bạn nhấp chuột phải vào tệp .app trong Finder trên hệ thống macOS và chọn "Hiển thị nội dung gói", bạn sẽ có thể xem cấu trúc bên trong của gói ứng dụng. Điều này hữu ích nếu bạn muốn truy cập các tài nguyên hoặc tệp được ứng dụng sử dụng hoặc nếu bạn muốn kiểm tra nội dung của ứng dụng nhằm mục đích khắc phục sự cố. Nội dung gói của tệp .app thường bao gồm các thư mục dành cho các tài nguyên như hình ảnh và âm thanh, cũng như mã thực thi cho ứng dụng. Bằng cách khám phá nội dung của tệp .app, bạn có thể hiểu sâu hơn về cách ứng dụng được kết hợp với nhau và chức năng của nó.

## Làm cách nào để mở tệp APP?

Để mở tệp .app trên macOS, chỉ cần bấm đúp vào tệp trong Finder. Thao tác này sẽ khởi chạy ứng dụng có trong gói .app. Nếu ứng dụng được cài đặt trên hệ thống của bạn và được liên kết với loại tệp .app, việc bấm đúp vào tệp sẽ tự động khởi động ứng dụng. Nếu ứng dụng không được liên kết với loại tệp .app, bạn có thể cần phải nhấp chuột phải vào tệp và chọn "Mở bằng" để chọn ứng dụng thích hợp để mở tệp.

Bạn có thể mở tệp .app trên Terminal trong macOS bằng cách sử dụng lệnh "open". Để thực hiện việc này, hãy điều hướng đến thư mục chứa tệp .app bằng lệnh "cd", rồi chạy lệnh sau:

```
open <AppName>.app 
```

Ở đâu<AppName> là tên của ứng dụng bạn muốn khởi chạy. Thao tác này sẽ khởi động ứng dụng như thể bạn đã nhấp đúp vào ứng dụng đó trong Finder. Lệnh "mở" là một tiện ích đa năng có thể được sử dụng để mở nhiều loại tệp khác nhau, bao gồm ứng dụng, tài liệu và thư mục. Khi bạn sử dụng lệnh "mở" trên tệp .app, nó sẽ khởi chạy ứng dụng có trong gói.

## Người giới thiệu
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
