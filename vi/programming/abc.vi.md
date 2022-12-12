
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - Tệp mã byte ActionScript",
  "description":"Tìm hiểu về định dạng tệp ABC với ví dụ và các API có thể tạo và mở tệp ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Tệp ABC là gì?

Một tệp có phần mở rộng .abc là một Tệp mã Byte ActionScript được tạo bởi trình biên dịch Flash là kết quả của việc biên dịch các tệp script ActionScript. Mã byte chứa trong tệp ABC được thực thi bởi Máy ảo ActionScript (AVM và AVM2). Mã byte bao gồm dữ liệu không đổi, hướng dẫn từ tập lệnh AVM2 và các loại siêu dữ liệu khác nhau. Khi tệp ABC được tải vào AVM hoặc AVM2, nó sẽ được xác minh. Nếu nó không phù hợp với Tổng quan về AVM2, nó sẽ bị từ chối. Các tệp ABC có thể được mở trong Adobe Flash Player đã ngừng hoạt động từ lâu.

## Định dạng tệp ABC - Thông tin khác

Các tệp ABC được lưu vào đĩa ở định dạng tệp nhị phân mà máy ảo AVM hoặc AVM2 có thể đọc được. Cấu trúc tệp bên trong của nó đại diện cho khối mã thực thi với tất cả dữ liệu không đổi, bộ mô tả kiểu, mã và siêu dữ liệu.

## Cấu trúc tệp ABC

Cấu trúc tệp ABC như hình bên dưới.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Trường Tệp ABC

|Tên trường|Mô tả|
---|---|
|minor_version, major_version|Các giá trị của major_version và minor_version là số phiên bản chính và phụ của định dạng abcFile.|
|constant_pool|Hằng_pool là một cấu trúc có độ dài thay đổi bao gồm các số nguyên, số đôi, chuỗi, không gian tên, bộ không gian tên và nhiều tên.|
|method_count, method|Giá trị củamethod_count là số mục nhập trong mảng phương thức. Mỗi mục trong mảng phương thức là một cấu trúc method_info có độ dài thay đổi.|
|metadata_count, metadata|Giá trị của metadata_count là số mục nhập trong mảng siêu dữ liệu. Mỗi mục nhập siêu dữ liệu là một cấu trúc siêu dữ liệu_thông tin ánh xạ tên thành một tập hợp các giá trị chuỗi. |
|class_count, instance, class|Giá trị của class_count là số mục nhập trong mảng instance và class. |
|script_count, script|Giá trị của script_count là số mục trong mảng script. Mỗi mục nhập tập lệnh là một cấu trúc script_info xác định các đặc điểm của một tập lệnh trong tệp này. |
|method_body_count, method_body|Giá trị của method_body_count là số mục trong mảng method_body. Mỗi method_bodyentry bao gồm một cấu trúc method_body_info có độ dài thay đổi chứa các hướng dẫn cho một phương thức hoặc chức năng riêng lẻ.|

## Người giới thiệu

* [ABC mạnh mẽ (Mã byte ActionScript) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

