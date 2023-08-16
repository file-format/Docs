{
  "date" : "2021-08-27",
  "keywords" :[ "tệp wsh", "định dạng tệp wsh", "tệp wsh là gì", "tệp", "ví dụ wsh", "phần mở rộng tệp wsh","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp WSH và API có thể tạo và mở tệp WSH.",
  "title" :"WSH - Tệp tập lệnh Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Tệp WSH là gì?
Một tệp có phần mở rộng .wsh chứa các thuộc tính và tham số cho một tập lệnh ngôn ngữ lập trình nhất định, chẳng hạn như VB hoặc VBS, v.v. Nhu cầu thực tế của WSH là sử dụng chúng để tùy chỉnh việc thực thi các tập lệnh nhất định. Cần có WScript hoặc CScript để chạy và cả hai thứ này đều được bao gồm trong hệ điều hành Windows. Các tệp WSH ban đầu được cung cấp trên Windows 95 trên đĩa cài đặt dưới dạng tùy chọn có thể định cấu hình và cài đặt cho Bảng điều khiển, sau đó là thành phần mặc định của Windows 98.

## Định dạng tệp WSH
WSH (Windows Script Host) có thể được sử dụng cho nhiều mục đích khác nhau, bao gồm quản trị, tập lệnh đăng nhập và tự động hóa chung. WSH thiết lập một môi trường để các tập lệnh chạy. nó gọi công cụ tập lệnh phù hợp và phân bổ một tập hợp các dịch vụ và đối tượng để tập lệnh hoạt động. Các tập lệnh này có thể chạy trong chế độ GUI, từ đối tượng COM hoặc chế độ dòng lệnh, mang lại sự linh hoạt cho người dùng đối với cả tập lệnh tương tác hoặc không tương tác.

### Ví dụ
Đây là một ví dụ rất đơn giản cho thấy một số VBScript sử dụng đối tượng WSH COM gốc "WScript" để hiển thị thông báo có nút 'OK'. Khi tập lệnh này được khởi chạy, công cụ CScript hoặc WScript sẽ được gọi và môi trường thời gian chạy sẽ được thiết lập.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Người giới thiệu

* [Máy chủ Windows Script - theo Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



