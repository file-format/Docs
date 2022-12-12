{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "tệp", "phần mở rộng", "định dạng tệp", "ngôn ngữ lập trình NUT", "Hướng dẫn lập trình", "ví dụ NUT", "định dạng tệp NUT", "ngôn ngữ sóc", "tệp mở rộng .nut ", "Tệp NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Tệp ngôn ngữ sóc",
  "description":"Tìm hiểu về định dạng tệp NUT và API có thể tạo và mở tệp NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Tệp NUT là gì?

NUT đề cập đến tệp Định dạng vùng chứa mở NUT. Định dạng tệp NUT này thuộc về ngôn ngữ lập trình được gọi là Squirrel. Nó là một ngôn ngữ lập trình hướng đối tượng, cấp cao và bắt buộc, được sử dụng chủ yếu trong các hệ thống nhúng và trò chơi điện tử.

Ngôn ngữ con sóc được coi là ngôn ngữ kịch bản nhẹ, có thể dễ dàng điều chỉnh theo kích thước và băng thông. Nó liên quan đến lợi thế của việc đếm tham chiếu tự động và quản lý rác trong bộ nhớ.

Cú pháp của ngôn ngữ con sóc thu hút các nhà phát triển vì nó giống C và có tính năng của ngôn ngữ kịch bản. Tuy nhiên, nó vẫn có ít lợi thế hơn so với các ngôn ngữ lập trình phổ biến khác cho mục đích này.



## Lược Sử ##

Nó được thiết kế bởi Alberto Demichelis vào năm 2003. Tuy nhiên, một phiên bản ổn định của ngôn ngữ này đã được phát hành vào năm 2016. Nó được thiết kế theo giấy phép của zlib/libpng. Năm 2010, giấy phép đã được thay đổi và chuyển giao cho MIT. Ngôn ngữ này được coi là phiên bản lấy cảm hứng từ [LUA](/vi/programming/lua/) (Ngôn ngữ lập trình). Có một danh sách các đề xuất cho ngôn ngữ cũ trên trang web do Alberto thiết kế để làm cho nó thuận lợi hơn.


## Thông số kỹ thuật ##

Tính năng và thông số kỹ thuật của ngôn ngữ sóc là nhiều. Nó cung cấp cơ sở của Dynamic typing, thuộc tính của ủy quyền, một số cách sử dụng các lớp và giao diện. Cú pháp của ngôn ngữ này có sự tương đồng với cú pháp của ngôn ngữ C. Các ứng dụng như Enduro/X (máy chủ ứng dụng cụm) sử dụng ngôn ngữ này. Vì Squirrel cũng được sử dụng cho các trò chơi điện tử, một số trong số đó là OpenTTD, GTA IV, v.v.

Bản phát hành ổn định của ngôn ngữ là 3.0.7. Bộ công cụ được gọi là MirthKit sử dụng ngôn ngữ lập trình Squirrel để cung cấp mã nguồn mở và đa nền tảng cho các trò chơi hai chiều. Bản chất của ngôn ngữ này là động và hầu hết các tính năng tương tự như [Python](/vi/programming/py/), LUA, v.v. Nó cũng liên quan đến việc triển khai máy ảo dựa trên đăng ký. Hiệu suất của Squirrel chậm hơn so với LUA.

Ngoài ra còn có một loại tệp mở rộng ".nut" khác, đó là lý do tại sao bạn nên xem kích thước của tệp để biết bạn có tệp NUT nào. Các tệp NUT của tập lệnh Squirrel hầu hết nhỏ hơn 1 MB trong khi các tệp NUT video thường có kích thước lớn hơn 1 MB.


## Ví dụ về định dạng tệp NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Tài liệu tham khảo ##

* [NUT - theo Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



