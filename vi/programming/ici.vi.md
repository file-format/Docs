{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "tệp", "phần mở rộng", "định dạng tệp", "Thực hiện ICI", "Hướng dẫn lập trình", "ví dụ ici", "ngôn ngữ lập trình ICI", "các mô-đun của ICI", "mô hình dữ liệu của ICI ", "tài liệu của ICI", "ngôn ngữ ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Tệp ngôn ngữ lập trình",
  "description":"Tìm hiểu về định dạng tệp ICI và các API có thể tạo và mở tệp ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Tệp ICI là gì?

Ngôn ngữ lập trình có mục đích chung được diễn giải và chứa một số tính năng như nhập động cùng với các loại dữ liệu linh hoạt được gọi là ngôn ngữ lập trình ICI (không phải từ viết tắt). Nó được coi là tương tự như ngôn ngữ [Perl](/vi/programming/pl/). Ngôn ngữ ICI này bao gồm các cấu trúc điều khiển luồng và cũng chứa một số toán tử của ngôn ngữ C. Nó không phải là ngôn ngữ hướng đối tượng nhưng một số tính năng của OOP có thể đạt được bằng một phương thức kế thừa cụ thể được gọi là cấu trúc thượng tầng. Tương tự như [C](/vi/programming/c), ngôn ngữ lập trình ICI này có cùng giao diện hệ thống và một thư viện chuẩn cho các chức năng tích hợp.


## Lược Sử ##

Vào cuối những năm 1980, nó được Tim Long phát triển như một ngôn ngữ lập trình thông dịch cho mục đích chung. Hầu hết các tính năng của ngôn ngữ này tương tự như C và nó cũng có thể đạt được một số tính năng bằng cách áp dụng một số phương pháp đặc biệt. Ngôn ngữ này được sở hữu dưới dạng miền công cộng và có sẵn dưới dạng ngôn ngữ có thể bán lại và không ai có thể đề cập đến việc anh ta lấy mã nguồn từ đâu. Tài liệu về ICI thuộc bản quyền của Canon Information System Research Australia.

## Đặc điểm kỹ thuật ##

Có hai loại dữ liệu khác nhau được sử dụng trong ngôn ngữ này. Hai loại này là loại dữ liệu Nguyên thủy và Tổng hợp. Cả hai điều này bao gồm các biểu thức khác nhau theo thành phần được xác định trước của chúng trong ngôn ngữ. Các mô-đun khác nhau như lồng nhau và chương trình con được hỗ trợ bởi ngôn ngữ này. Vì một số thuộc tính của nó tương tự như Perl nên nó có sự tích hợp chặt chẽ với các biểu thức chính quy.

Các bộ được giới hạn là không đồng nhất và lồng vào nhau. Các tập hợp này cung cấp hỗ trợ cho các hoạt động tập hợp thường được sử dụng như Liên minh và Giao lộ, v.v. Nó chủ yếu được sử dụng làm ngôn ngữ vì mục đích triển khai cốt lõi cho các ứng dụng thuộc sở hữu của các tổ chức đa quốc gia.

Hầu như tất cả các loại chương trình đều có thể được viết bằng ngôn ngữ này và hầu hết các chương trình cụ thể liên quan đến cấu trúc dữ liệu phức tạp đều được viết bằng ngôn ngữ lập trình ICI. Các ứng dụng có thể liên quan đến việc triển khai ICI theo cách mà chúng nên được viết trong đó. Các phần chức năng của ứng dụng có thể được thực hiện bởi các mô-đun của ICI. Ngôn ngữ của ICI hơi giống ngôn ngữ C nhưng mô hình dữ liệu của ICI ở mức cao hơn và khác với các loại như từ điển (cấu trúc), tập hợp, mảng động, biểu thức chính quy và chuỗi (thực).


## Ví dụ về định dạng tệp ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Tài liệu tham khảo ##

* [Ngôn ngữ lập trình ICI](http://atrn.org/ici/doc/ici.html)



