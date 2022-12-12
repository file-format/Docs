{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Tệp tham chiếu vĩ mô Microsoft Office",
  "description":"Tìm hiểu về tệp MSO và các API có thể tạo và mở tệp MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Tệp MSO là gì?

Tệp MSO là định dạng tệp chứa dữ liệu được tạo khi gửi thư HTML bằng Microsoft Outlook. Điều này xảy ra chủ yếu với các ứng dụng Microsoft Office 2000. Trong hầu hết các trường hợp, thông báo email được đính kèm với tên tệp **Oledata.mso**. Người nhận email, khi mở một email như vậy, có thể xem tệp một cách chính xác ngay cả khi họ không cài đặt cùng một phần mềm. Các tệp MSO tham khảo [Định dạng tệp tài liệu tổng hợp của Microsoft (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Định dạng tệp MSO của Microsoft

Các tệp MSO được lưu ở Định dạng tệp tài liệu tổng hợp của Microsoft (MCDF), còn được gọi là định dạng tệp nhị phân triển khai tệp hỗn hợp lưu trữ có cấu trúc và liên kết đối tượng (OLE) hoặc Mô hình đối tượng thành phần (COM).

### Cấu trúc định dạng tệp MSO

Cấu trúc định dạng tệp nội bộ của định dạng tệp MSO được xác định rõ trong [Cấu trúc](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) phần của tài liệu MCDF. Bảng phân bổ tệp (FAT) quản lý phân bổ ngành và chuỗi ngành. Nó chứa một mảng các số cung 32 bit. Mỗi chỉ mục trong mảng đại diện cho một số khu vực trong khi giá trị của nó đại diện cho khu vực tiếp theo trong chuỗi hoặc một giá trị đặc biệt.

## Người giới thiệu

* [Bộ lưu trữ có cấu trúc COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Định dạng tệp tài liệu tổng hợp của Microsoft (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

