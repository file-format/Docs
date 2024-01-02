
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp thứ 4 - Định dạng tệp ngôn ngữ thứ tư",
  "description":"Tìm hiểu về định dạng tệp .4 bằng ví dụ và các API có thể tạo và mở tệp thứ 4.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Tập tin thứ 4 là gì?

Tệp có phần mở rộng tệp .4th là tệp lập trình được tạo cho **Ngôn ngữ lập trình thứ tư**. Nó chứa mã nguồn của các chương trình được viết bằng ngôn ngữ lập trình Forth và tạo đầu ra khi chương trình được thực thi. Nó chỉ là một tệp ngôn ngữ lập trình khác tương tự như tệp nguồn [C](/vi/programming/c/) và [C++](/vi/programming/cpp/).

## Định dạng tệp thứ 4 - Thông tin thêm


### Ví dụ về mã ngôn ngữ lập trình thứ 4

Đây là một ví dụ về một chương trình đơn giản được viết bằng Forth để tính giai thừa của một số đã cho:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Trong ví dụ này, từ giai thừa nhận một đối số duy nhất n và trả về giai thừa của nó. Từ trùng lặp sẽ nhân đôi giá trị ở đầu ngăn xếp, thả sẽ loại bỏ giá trị ở đầu ngăn xếp và * nhân hai giá trị ở đầu ngăn xếp. Các cấu trúc if và started/until kiểm soát luồng của chương trình.

Để sử dụng chương trình này, bạn phải nhập định nghĩa vào trình thông dịch Forth, sau đó gọi từ giai thừa bằng số bạn muốn tìm giai thừa của:

```
10 factorial .
```
Điều này sẽ dẫn đến kết quả là 3628800, là giai thừa của 10.

## Người giới thiệu

* [Ngôn ngữ lập trình Forth](https://en.wikipedia.org/wiki/Forth_(programming_language))

