{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "file", "extension", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về tệp GLTF và API có thể tạo và mở tệp GLTF.",
  "title" :"GLTF - Định dạng tệp truyền GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GLTF là gì?

glTF (Định dạng truyền GL) là định dạng tệp 3D lưu trữ thông tin mô hình 3D ở định dạng JSON. Việc sử dụng JSON giảm thiểu cả kích thước của nội dung 3D và quá trình xử lý thời gian chạy cần thiết để giải nén và sử dụng các nội dung đó. Nó đã được sử dụng để truyền và tải hiệu quả các cảnh và mô hình 3D bằng các ứng dụng. glTF được phát triển bởi Nhóm làm việc về định dạng 3D của Khronos Group và cũng được những người tạo ra nó mô tả là [JPEG](/vi/image/jpeg/) của 3D.

Định dạng tệp GLTF xác định định dạng xuất bản phổ biến, có thể mở rộng cho các công cụ và dịch vụ nội dung 3D giúp hợp lý hóa quy trình tác giả và cho phép sử dụng nội dung có thể tương tác trong toàn ngành. Mục đích đằng sau việc tạo định dạng tệp glTF là để xác định định dạng xuất bản phổ biến, có thể mở rộng cho các công cụ và dịch vụ nội dung 3D sẽ hợp lý hóa quy trình tác giả và cho phép sử dụng nội dung có thể tương tác trong toàn ngành. Nó giảm thiểu quá trình xử lý thời gian chạy của các ứng dụng sử dụng WebGL và các API khác.

## Lịch sử tóm tắt của tệp GLTF

Thông số kỹ thuật đầu tiên cho định dạng tệp glTF 1.0 được công bố vào tháng 10 năm 2015. Đây là một loạt nỗ lực bắt đầu từ tháng 3 năm 2012 của Khronos. Mục đích của những nỗ lực này là để đánh giá các cơ hội xung quanh lực kéo WebGL. Kết quả là, bản demo đầu tiên của định dạng glTF, dựa trên định dạng JSON đã được trình bày tại buổi họp mặt WebGl vào năm 2012. Định dạng này đã được một số công ty áp dụng theo thời gian bao gồm Caesium, 3D Tiles, Oculus, Microsoft, Archilogic và các công ty khác.

glTF 2.0 đã được xuất bản vào ngày 5 tháng 6 năm 2017 tại Hội nghị Web3D 2017. Có một danh sách dài các công ty đã sử dụng định dạng tệp glTF sau đó.

## Định dạng tệp GLTF

Thông số định dạng tệp cho glTF 2.0 có sẵn [trực tuyến](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) để tham khảo và nên được tư vấn trong mọi triển khai liên quan đến đọc/ghi để được hỗ trợ định dạng tệp glTF.

glTF xác định nội dung dưới dạng tệp JSON có hỗ trợ dữ liệu bên ngoài. Nó đại diện cho các mô hình 3D với sự trợ giúp của:

* Mô tả cảnh đầy đủ có trong tệp .glTF có định dạng JSON bao gồm thông tin về phân cấp nút, vật liệu, máy ảnh, cũng như thông tin mô tả cho mắt lưới, hoạt ảnh và các cấu trúc khác
* Tệp nhị phân (.bin) chứa dữ liệu hình học và hoạt hình cũng như dữ liệu dựa trên bộ đệm khác
* Tệp hình ảnh ([.jpg](/vi/image/jpeg/), [.png](/vi/image/png/)) cho họa tiết

Mọi nội dung bên ngoài như hình ảnh được lưu trữ trong các tệp bên ngoài được tham chiếu qua URI. Các URI này được lưu trữ cùng với bộ chứa GLB hoặc được nhúng trực tiếp vào JSON bằng URI dữ liệu. Mỗi glTF hợp lệ phải chỉ định phiên bản của nó.

glTF đã được thiết kế để đạt được kích thước tệp nhỏ, tải nhanh, thể hiện cảnh 3D hoàn chỉnh và khả năng mở rộng. Những mục tiêu thiết kế độc đáo này là lý do chính cho sự phổ biến của định dạng tệp glTF trong miền 3D. Sau đây là các loại mime được định dạng tệp glTF hỗ trợ cho các loại tệp khác nhau:

* Các tệp .gltf sử dụng model/gltf+json
* Tệp .bin sử dụng ứng dụng/octet-stream
* Các tệp kết cấu sử dụng loại hình ảnh/* chính thức dựa trên định dạng hình ảnh cụ thể. Để tương thích với các trình duyệt web hiện đại, các định dạng hình ảnh sau được hỗ trợ: image/jpeg, image/png.

### Mã hóa JSON

glTF áp đặt các hạn chế bổ sung sau đối với định dạng tệp JSON

Để đơn giản hóa việc triển khai phía máy khách, glTF có thêm các hạn chế đối với định dạng và mã hóa JSON.

1. JSON phải sử dụng mã hóa UTF-8 không có BOM.
1. Tất cả các chuỗi được xác định trong thông số kỹ thuật này (tên thuộc tính, enum) chỉ sử dụng bộ ký tự ASCII và phải được viết dưới dạng văn bản thuần túy, ví dụ: "bộ đệm" thay vì `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Tên (khóa) trong đối tượng JSON phải là duy nhất, tức là không được phép trùng lặp khóa.

### URI

Bộ đệm và tài nguyên hình ảnh được tham chiếu qua URI. Hai loại URI sau đây phải được máy khách hỗ trợ.

**URI dữ liệu:** URI dữ liệu được xác định theo RFC 2397 và được glTF sử dụng để nhúng tài nguyên vào JSON.

**Đường dẫn URI tương đối:** hoặc đường dẫn-noscheme như được định nghĩa bởi RFC 3986, [Phần 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — không có lược đồ, quyền hoặc tham số. Các ký tự dành riêng phải được mã hóa theo phần trăm, theo RFC 3986, [Mục 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Người giới thiệu ##

* [Thông số kỹ thuật glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Định dạng tệp glTF - Theo Wikipedia](https://en.wikipedia.org/wiki/GlTF)

