{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Tệp tài nguyên Visual C++",
  "description":"Tìm hiểu về định dạng tệp APS với ví dụ về APS và các API có thể tạo và mở tệp APS.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Định dạng tệp APS là gì?
Tệp APS được tạo bởi Visual C++, một ứng dụng phát triển phần mềm của Microsoft. Nó lưu biểu diễn nhị phân của tài nguyên được kết hợp với dự án và nó cho phép ứng dụng tải tài nguyên nhanh hơn. Bạn có thể dễ dàng tìm thấy các tệp này với phần mở rộng tệp .aps. Trên thực tế, các trình soạn thảo tài nguyên không đọc trực tiếp các tệp resource.h, đó là lý do tại sao trình biên dịch tài nguyên biên dịch chúng thành các tệp .aps được các trình soạn thảo tài nguyên sử dụng.

## Định dạng tệp APS
Định dạng tệp APS chỉ là một bước biên dịch và chỉ lưu trữ dữ liệu tượng trưng. Thông tin phi biểu tượng như nhận xét sẽ bị loại bỏ trong quá trình biên dịch. Ví dụ: khi bạn Lưu, trình chỉnh sửa tài nguyên sẽ ghi đè lên tệp tập lệnh tài nguyên và tệp resource.h. Mọi thay đổi đối với bản thân các tài nguyên vẫn được kết hợp trong tệp tập lệnh tài nguyên, nhưng các nhận xét sẽ luôn bị mất sau khi tệp tập lệnh tài nguyên bị ghi đè.


## Người giới thiệu

* [Tệp tài nguyên (C++)](https://docs.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


