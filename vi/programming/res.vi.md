{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Tập lệnh tài nguyên được biên dịch C++",
  "description":"Tìm hiểu về định dạng tệp RES với ví dụ về RES và các API có thể tạo và mở tệp RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Tệp RES là gì?
Tệp có hậu tố hoặc phần mở rộng .res có thể thuộc nhiều loại định dạng tệp. Ở đây chúng ta đang thảo luận về định dạng tệp RES là Tập lệnh tài nguyên được biên dịch C++; một tệp nhị phân được tạo bởi Trình biên dịch tài nguyên Microsoft (rc) có chứa dữ liệu tài nguyên; dựa trên nội dung của tệp định nghĩa tài nguyên; liên quan đến dự án phần mềm mẹ của nó. Tệp .res thường được định dạng lại thành tệp đối tượng tài nguyên để liên kết tệp đó với tệp thực thi của ứng dụng.

## Định dạng tệp RES
Định dạng tệp RES thuộc về Trình biên dịch tài nguyên Microsoft (rc). Trình biên dịch tài nguyên là một công cụ biên dịch các tài nguyên như con trỏ, biểu tượng, menu và hộp thoại mà ứng dụng của bạn sử dụng. Các tệp tài nguyên thường có phần mở rộng .res; chứa các tài nguyên, chẳng hạn như con trỏ, hình ảnh và thông tin phiên bản. Tệp RES có thể là tệp tài nguyên 16 hoặc 32 bit.
## Cấu trúc tệp tài nguyên
Tệp tài nguyên chứa một loạt các mục nhập tài nguyên khác nhau. Mỗi mục chứa tiêu đề tài nguyên và dữ liệu liên quan. Tiêu đề tài nguyên thường được căn chỉnh theo kiểu DWORD trong tệp và chứa các nội dung sau:

- Một **DWORD** để chỉ định kích thước của tiêu đề tài nguyên
- Một **DWORD** để chỉ định kích thước của dữ liệu tài nguyên
- Loại tài nguyên
- Tên tài nguyên
- Thông tin tài nguyên bổ sung

Cấu trúc tiêu đề tài nguyên xác định định dạng của tệp RES. Dữ liệu cho tài nguyên theo sau tiêu đề tài nguyên. Một số tài nguyên cũng thêm mẫu tiêu đề nhóm dành riêng cho tài nguyên để cung cấp thông tin về một nhóm tài nguyên. Sau đây là một số loại mục nhập tài nguyên và mô tả của chúng:

### Tài nguyên bảng máy gia tốc
Bảng tăng tốc là mục nhập tài nguyên trong tệp RES không có tiêu đề nhóm. Mẫu **ACCELTABLEENTRY** xác định từng mục nhập trong bảng gia tốc. Tệp RES có thể có nhiều bảng tăng tốc.

### Tài nguyên con trỏ và biểu tượng
Mặc dù, hệ thống coi mỗi biểu tượng và con trỏ là một tệp duy nhất nhưng chúng được lưu trữ trong tệp RES dưới dạng một nhóm tài nguyên biểu tượng hoặc một nhóm tài nguyên con trỏ. Các định dạng tệp của tài nguyên biểu tượng và con trỏ giống nhau. Tiêu đề nhóm tài nguyên theo sau tất cả các thành phần nhóm con trỏ hoặc biểu tượng riêng lẻ trong tệp .res.

### Tài nguyên hộp thoại
Một hộp thoại cũng được hiện thực hóa dưới dạng mục nhập tài nguyên trong tệp RES. Nó chứa một mẫu tiêu đề hộp thoại **DLGTEMPLATE** và một mẫu **DLGITEMPLATE** cho từng điều khiển cụ thể trong hộp thoại. Các mẫu **DLGTEMPLATEEX** và **DLGITEMTEMPLATEEX** giải thích định dạng của tài nguyên hộp thoại mở rộng.

### Tài nguyên phông chữ
Tài nguyên menu chứa mẫu **MENUHEADER** sau đó là một hoặc nhiều mẫu **NORMALMENUITEM** hoặc **POPUPMENUITEM**, một mẫu cho mỗi mục menu trong mẫu menu. Các mẫu **MENUEX_TEMPLATE_HEADER** và **MENUEX_TEMPLATE_ITEM** giải thích định dạng của tài nguyên menu mở rộng.

### Tài nguyên Bảng Thông báo
Bảng thông báo bao gồm văn bản được định dạng để hiển thị dưới dạng thông báo lỗi hoặc trong hộp thông báo. Mẫu chính trong tài nguyên bảng thông báo là cấu trúc **MESSAGE_RESOURCE_DATA**.

### Phiên bản Tài nguyên
Mẫu chính trong tài nguyên phiên bản là **VS_FIXEDFILEINFO**. Các mẫu bổ sung bao gồm **VarFileInfo** để lưu trữ dữ liệu liên quan đến thông tin ngôn ngữ và **StringFileInfo** cho thông tin chuỗi tùy chỉnh.




## Người giới thiệu

* [Định dạng tệp tài nguyên](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



