{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp AML - Tệp ngôn ngữ máy ACPI",
  "description":"Tìm hiểu về định dạng tệp ACPI AML và các API có thể tạo và mở tệp AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Tệp AML là gì?

Tệp AML là một tệp hệ thống được tạo bằng ngôn ngữ Cấu hình nâng cao và Giao diện nguồn (ACPI) được sử dụng để định cấu hình các thuộc tính phần cứng. Nó chứa mã byte độc lập với máy được sử dụng để định cấu hình phần cứng ngay cả đối với các thao tác đơn giản như tắt máy tính. Các tệp AML có thể chứa các hướng dẫn tùy thuộc vào mục đích mà nó được cài đặt trên máy. Việc triển khai các tiêu chuẩn ACPI cho phép bạn tăng cường chức năng quản lý điện năng và giao diện mạnh mẽ để cấu hình các thiết bị bo mạch chủ chẳng hạn như bo mạch chủ P55.

## Định dạng tệp ACPI AML

Các tệp AML được lưu dưới dạng tệp nhị phân vào đĩa với nội dung được ghi bằng mã byte. Thông số định dạng tệp của tiêu chuẩn ACPI hiện có trên [uefi](https://uefi.org/node/735). Ngôn ngữ đã được thiết kế để mang lại sự ổn định và khả năng tương thích ngược, yêu cầu ít phải viết lại hoặc xây dựng lại ngăn xếp ứng dụng.

## Thông số kỹ thuật định dạng tệp AML

Một tệp AML bao gồm các bảng DSDT và SSDT. Mã byte AML được đọc và phân tích cú pháp từ đầu mỗi bảng này. Điều này cung cấp thông tin về các định nghĩa của thiết bị và đối tượng trong không gian tên ACPI. Sử dụng thông tin này, trình thông dịch AML có thể tạo danh sách tất cả các thiết bị có sẵn trong hệ thống cũng như các thuộc tính và chức năng được hỗ trợ của chúng.

### Mã ASL Ví dụ cho DSDT

Một ví dụ về mã ASL cho DSDT như sau.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Người giới thiệu

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

