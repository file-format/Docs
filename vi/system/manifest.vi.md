{
"ngày": "2023-03-07",
  "keywords": [
"tệp kê khai",
"tệp kê khai là gì",
"tài liệu",
"phần mở rộng tệp kê khai",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp MANIFEST - Tệp kê khai ứng dụng Windows",
  "description":"Tìm hiểu về định dạng MANIFEST và các API có thể tạo và mở tệp MANIFEST.",
"linktitle":"TỔNG HỢP",
  "menu": {
    "docs": {
      "identifier": "system-manifest",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Tệp MANIFEST là gì?

Tệp kê khai là tệp chứa thông tin về ứng dụng hoặc gói phần mềm. Tệp thường được đặt tên bằng phần mở rộng tệp .manifest. Tệp kê khai cung cấp thông tin về các tệp được bao gồm trong gói, số phiên bản của chúng và mọi phụ thuộc mà gói có trên các thành phần phần mềm khác.

Các tệp kê khai thường được sử dụng trên nền tảng Windows để đảm bảo rằng các ứng dụng phần mềm được cài đặt và định cấu hình đúng cách. Chúng có thể được sử dụng để chỉ định những thứ như nên sử dụng phiên bản nào của thư viện dùng chung, nên đưa vào tệp cấu hình nào và khóa đăng ký nào sẽ được sửa đổi trong quá trình cài đặt.

Ngoài Windows, các tệp kê khai cũng có thể được sử dụng trong các ngữ cảnh khác, chẳng hạn như cho các ứng dụng web hoặc ứng dụng Android. Định dạng và nội dung cụ thể của tệp kê khai sẽ phụ thuộc vào nền tảng và ứng dụng được đóng gói.

## Thêm thông tin

Các tệp kê khai có định dạng XML. XML là ngôn ngữ đánh dấu được sử dụng rộng rãi để tạo tài liệu và dữ liệu có cấu trúc và thường được sử dụng trong phát triển phần mềm để mô tả cấu hình, cài đặt và siêu dữ liệu khác.

Trong ngữ cảnh của các ứng dụng phần mềm, tệp XML kê khai thường chứa thông tin về các phần phụ thuộc của ứng dụng, thông tin phiên bản và các cài đặt cấu hình khác. Tệp này được sử dụng để đảm bảo rằng ứng dụng được cài đặt chính xác và có tất cả các thành phần cũng như tài nguyên cần thiết để chạy đúng cách.

Tệp XML kê khai có thể được bao gồm trong gói ứng dụng hoặc dưới dạng tệp riêng biệt được tải xuống trong quá trình cài đặt. Nó thường được đặt tên bằng phần mở rộng tệp ".manifest" và tuân theo định dạng cụ thể được xác định bởi nền tảng hoặc khung mà ứng dụng được xây dựng trên đó.

Ví dụ: trong Microsoft .NET Framework, tệp XML kê khai được sử dụng để mô tả các phần phụ thuộc và thông tin phiên bản cho một ứng dụng và tệp này thường được đưa vào như một phần của tập hợp ứng dụng. Tệp được Common Language Runtime (CLR) sử dụng để xác định phiên bản chính xác của tập hợp cần tải và để đảm bảo ứng dụng chạy chính xác.

## Người giới thiệu
* [Tệp kê khai](https://en.wikipedia.org/wiki/Manifest_file)

