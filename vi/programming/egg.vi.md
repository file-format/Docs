{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp EGG - Tệp phân phối Python",
  "description":"Tìm hiểu về định dạng tệp EGG và các API có thể tạo và mở tệp EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Tệp TRỨNG là gì?

Tệp EGG, còn được gọi là trứng Python, là một định dạng phân phối cũ hơn của các bản phân phối Python. Đó là kho lưu trữ nén [ZIP](/vi/compression/zip/) với phần mở rộng .egg và chứa các tệp nguồn của ứng dụng Python cùng với thông tin meta về bản phân phối. Các tệp EGG thay thế cho tệp Windows Executable [EXE](/vi/executable/exe/) nhưng đa nền tảng. Định dạng cũ hơn này cho các bản phân phối Python đã được thay thế bằng định dạng tệp Wheel (WHL) mới hơn vào đầu năm 2010.

## Định dạng tệp TRỨNG

Các tệp EGG được lưu dưới dạng kho lưu trữ ZIP được nén. Điều đó có nghĩa là nếu bạn thay phần mở rộng .egg bằng .zip, bạn sẽ có thể mở nó bằng các tiện ích giải nén tiêu chuẩn như Corel WinZIP, Microsoft Explorer hoặc RARLAB WinRAR.

Các tệp EGG có thể được tạo bằng gói **distutils** có sẵn của Python. Một công cụ khác có thể tạo và mở tệp EGG là **SetupTools**. Các tệp EGG có thể được cài đặt dưới dạng gói bằng cách sử dụng **easy_install**.

`LƯU Ý - Định dạng tệp EGG đã lỗi thời để thay thế cho định dạng tệp WHL bánh xe mới.`

## Tài liệu tham khảo ##

* [Trứng trăn](https://python101.pythonlibrary.org/chapter38_eggs.html)

