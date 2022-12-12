{
  "date" : "2019-10-11",
  "keywords" :[ "tệp vrml", "định dạng tệp vrml", "tệp vrml là gì", "tệp", "ví dụ vrml", "phần mở rộng tệp vrml","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp VRML",
  "description":"Tìm hiểu về định dạng tệp VRML và API có thể mở và tạo tệp VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VRML là gì?
Ngôn ngữ lập mô hình thực tế ảo (VRML) là một định dạng tệp để biểu diễn các đối tượng thế giới [3D](/vi/3d/) tương tác trên World Wide Web (www). Nó được sử dụng trong việc tạo các biểu diễn ba chiều của các cảnh phức tạp như hình minh họa, định nghĩa và bản trình bày thực tế ảo. Định dạng này đã được thay thế bởi [X3D](/vi/3d/x3d/). Nhiều ứng dụng mô hình 3D có thể lưu các đối tượng và cảnh ở định dạng VRML.

## Định dạng tệp VRML

VRML là định dạng tệp văn bản chỉ định thông tin như đỉnh và cạnh của đa giác 3D cùng với thông tin như màu bề mặt, kết cấu ánh xạ UV, độ bóng, độ trong suốt, v.v. Nó có khả năng biểu diễn các đối tượng tĩnh và động ngoài việc có các siêu liên kết đến các phương tiện khác như âm thanh, phim và hình ảnh. Điều này cho phép mở các phần tử siêu liên kết khi người dùng nhấp vào các đối tượng này.

Các tệp TVRML theo thuật ngữ phổ biến được gọi là "thế giới" và có phần mở rộng .wrl. Bản chất văn bản của các tệp này cho phép giảm kích thước tệp bằng cách sử dụng các định dạng nén như gzip, khiến chúng thuận lợi hơn để truyền qua internet một cách nhanh chóng. Thông số định dạng tệp cho [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) đóng vai trò là tài liệu tham khảo của nhà phát triển để tạo các ứng dụng tương thích để đọc/ghi các tệp này.

## Tiêu chí thiết kế ##

Mục đích và thiết kế của VRML xoay quanh các yêu cầu sau.

* **Khả năng ủy quyền** - Cho phép phát triển trình tạo và trình chỉnh sửa ứng dụng cũng như nhập dữ liệu từ các định dạng công nghiệp khác
* **Tính đầy đủ** - Cung cấp tất cả thông tin cần thiết để triển khai và giải quyết một bộ tính năng hoàn chỉnh để được chấp nhận rộng rãi trong ngành
* **Khả năng kết hợp** - Khả năng sử dụng kết hợp các thành phần của VRML và do đó cho phép tái sử dụng.
* **Khả năng mở rộng** - Khả năng thêm các yếu tố mới.
* **Khả năng triển khai** -Có khả năng triển khai trên nhiều hệ thống.
* **Tiềm năng nhiều người dùng** - Không nên ngăn cản việc triển khai môi trường nhiều người dùng.
* **Tính trực giao** - Các phần tử của VRML phải độc lập với nhau hoặc bất kỳ phần phụ thuộc nào cũng phải được cấu trúc và xác định rõ ràng.
* **Hiệu suất** - Các yếu tố nên được thiết kế với điểm nhấn là hiệu suất tương tác trên nhiều nền tảng điện toán khác nhau.
* **Khả năng mở rộng** - Các thành phần của VRML nên được thiết kế cho các tác phẩm có kích thước vô cùng lớn.
* **Thông lệ tiêu chuẩn** - Chỉ những yếu tố phản ánh thông lệ hiện có, cần thiết để hỗ trợ thông lệ hiện có hoặc cần thiết để hỗ trợ các tiêu chuẩn được đề xuất mới được tiêu chuẩn hóa.
* **Cấu trúc tốt** - Một phần tử phải có giao diện được xác định rõ ràng và mục đích vô điều kiện được nêu đơn giản. Nên tránh các yếu tố đa năng và tác dụng phụ.

## Người giới thiệu ##

* [VRML - Theo Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [Thông tin cụ thể về định dạng tệp VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

