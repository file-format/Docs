
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp ADS - Định dạng tệp đặc tả Ada",
  "description":"Tìm hiểu về định dạng tệp ADS với ví dụ và các API có thể tạo và mở tệp ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Tệp ADS là gì?

Tệp ADS là tệp đặc tả cho dự án lập trình Ada. Nó tương tự như một lớp cho Java, hoặc cặp tiêu đề và triển khai trong trường hợp của C++. Thông số kỹ thuật công khai và riêng tư của gói Ada được lưu trữ trong tệp .ads. Ngược lại, tệp .adb chứa phần triển khai hoặc phần thân Ada. Giống như [C++](/vi/programming/cpp/), Ada cung cấp sự tách biệt giữa đặc tả và triển khai độc lập với OOP.

Các tệp ADS có thể được mở trong bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Microsoft Notepad, Notepad ++ và Atom.

## Định dạng tệp QUẢNG CÁO

Các tệp ADS ở định dạng tệp văn bản thuần túy đơn giản và có thể được mở/chỉnh sửa bằng bất kỳ trình soạn thảo văn bản nào. Các gói Ada có thể được tổ chức thành các hệ thống phân cấp. Một đơn vị con có thể được khai báo theo cách sau:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Người giới thiệu

* [Gói Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

