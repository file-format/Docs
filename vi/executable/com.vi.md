{
  "date" : "2021-06-29",
  "keywords" :[ "tệp com", "tệp com là gì", "tệp", "ví dụ com", "phần mở rộng tệp com","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp COM và API có thể tạo và mở tệp COM.",
  "title" :"Định dạng tệp lệnh COM - DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp COM là gì?
Các tệp COM chỉ được sử dụng để thực hiện một tập hợp các lệnh hoặc hướng dẫn. Tệp COM bao gồm một chương trình thực thi có khả năng chạy từ Windows hoặc MS-DOS. Tương tự như tệp EXE, tệp COM cũng được lưu ở định dạng nhị phân nhưng nó khác với tệp EXE vì nó không có tiêu đề hoặc siêu dữ liệu và nó cũng có kích thước tối đa khoảng 64KB. Khi tệp COM chạy lần đầu trên hệ thống 32-bit, nó sẽ nhắc cài đặt cấu phần Máy ảo DOS NT (NTVDM). Tệp COM có thể chạy trên phiên bản 64 bit của Microsoft Windows với máy ảo hỗ trợ môi trường MS-DOS.

## định dạng tệp COM
Định dạng tệp COM là định dạng thực thi nhị phân được sử dụng trong Microsoft Windows hoặc MS-DOS. Cấu trúc của nó chỉ bao gồm một tập hợp các hướng dẫn; nó không có tiêu đề và không chứa siêu dữ liệu tiêu chuẩn. Nó chỉ lưu trữ tất cả dữ liệu và mã của nó trong một phân đoạn và tệp nhị phân của nó có kích thước tối đa 64KB. Định dạng tệp này không tự di chuyển khi thử chạy lại. Vì vậy, hệ điều hành tải nó tại một địa chỉ được đặt trước. Ngoài ra, có thể tạo tệp COM để thực thi trong cả hai hệ điều hành ở dạng **nhị phân béo**. Không có bất kỳ khả năng tương thích thực tế nào ở cấp độ hướng dẫn. Các hướng dẫn tại điểm nhập được chọn để giống nhau về chức năng nhưng khác nhau trong cả hai hệ điều hành và làm cho chương trình đang chạy, chuyển đến phần của hệ điều hành đang sử dụng. Về cơ bản, đây là hai chương trình khác nhau có cùng quy trình trong một tệp duy nhất, trước mã chọn chương trình sẽ sử dụng.
### Ví dụ về tệp COM
Khi thực thi tệp COM, các hướng dẫn được đọc từ byte đầu tiên và được theo dõi liên tục cho đến khi tìm thấy hướng dẫn cuối cùng. Đây là một ví dụ mã ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Người giới thiệu

* [Tệp COM - của Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

