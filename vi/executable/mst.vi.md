{
  "date" : "2021-06-30",
  "keywords" :[ "tệp mst", "định dạng tệp mst", "tệp mst là gì", "tệp", "ví dụ mst", "phần mở rộng tệp mst","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp MST và API có thể tạo và mở tệp MST.",
  "title" :"MST - Tệp gói cài đặt Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Tệp MST là gì?
Các tệp có phần mở rộng .mst được sử dụng để chuyển đổi nội dung của gói MSI. Chúng thường được quản trị viên hệ thống sử dụng để áp dụng cài đặt tùy chỉnh cho tệp MSI hiện có. Các tệp MST được sử dụng cùng với gói MSI ban đầu trong hệ thống phân phối phần mềm của họ, chẳng hạn như chính sách nhóm. Các tệp MST thường được sử dụng trong quá trình phát triển và thử nghiệm phần mềm để định cấu hình các phiên bản phần mềm đang phát triển của chúng.

## Định dạng tệp MST
Tệp MST hoặc Transform được sử dụng để thu thập các tùy chọn cài đặt cho các chương trình sử dụng Microsoft Windows Installer trong một tệp. Các tệp này thường được sử dụng trên dòng lệnh Trình cài đặt (MSIEXEC.EXE) hoặc được sử dụng trong Chính sách nhóm cài đặt phần mềm; trong miền Microsoft Active Directory. Các tệp MST cũng có thể được sử dụng với các trình cài đặt thực thi được bao bọc. Một trường hợp chung là ai đó muốn chuyển tham số dòng lệnh cho trình cài đặt được bao bọc. Để làm điều đó, bạn cần có tệp MST bổ sung thuộc tính WRAPPED_ARGUMENTS vào bảng thuộc tính. Không thể tạo hoặc chỉnh sửa các tệp này bằng trình chỉnh sửa chung. Các công cụ cụ thể có sẵn cho mục đích này.

### Làm cách nào để sử dụng tệp MST?
Các tệp MST có thể được tạo bằng cách sử dụng nhiều công cụ khác nhau và Ocra thường được sử dụng để tạo tệp MST. Sau đó, các cài đặt có thể được tùy chỉnh theo nhu cầu và lưu chúng tại một vị trí cụ thể. Sau đó, các tệp MST có thể được sử dụng cùng với các tệp MSI. Nếu bạn muốn kiểm tra tệp này; sử dụng cú pháp sau trên dòng lệnh

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Thuộc tính TRANSFORMS

Bạn cũng có thể sử dụng thuộc tính **TRANSFORMS** của trình cài đặt Windows, đây thực sự là danh sách các biến đổi mà trình cài đặt áp dụng khi cài đặt gói. Trình cài đặt thực thi các phép biến đổi theo thứ tự giống như chúng được liệt kê trong thuộc tính TRANSFORM. Các biến đổi có thể được chỉ định theo tên tệp có phần mở rộng .mst hoặc đường dẫn đầy đủ. Để chỉ định nhiều hơn một biến đổi, hãy tách từng tên tệp hoặc dấu chấm phẩy như ví dụ sau.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Người giới thiệu

* [Tệp chuyển đổi MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [Thuộc tính TRANSFORMS](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


