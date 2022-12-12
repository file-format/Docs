{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "phần mở rộng", "tệp", "định dạng", "hình ảnh", "Bitmap độc lập với thiết bị", "Định dạng tệp con trỏ", "Con trỏ", "Windows", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Định dạng tệp con trỏ",
  "description":"Tìm hiểu về định dạng tệp CUR và các API có thể tạo và mở tệp CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp CUR là gì? ##

Tệp CUR là định dạng tệp con trỏ tĩnh của Microsoft Windows. Về cơ bản, chúng là những hình ảnh tĩnh giống hệt với các tệp ICO (biểu tượng) về mọi mặt ngoại trừ phần mở rộng. Cả CUR và [ICO](/vi/image/ico/) đều được thiết lập trên cơ sở đặc tả Bitmap độc lập với thiết bị [DIB](/vi/image/dib/) (Sơ đồ bit độc lập với thiết bị). Mặc định, cũng như con trỏ tùy chỉnh như con trỏ chuột Windows cho hệ điều hành Windows, được lưu trữ trong các tệp CUR. Nó có thể là một mũi tên để sử dụng bình thường, một đồng hồ cát quay tròn để biểu thị thời gian chờ đợi hoặc một thanh I-bar để chỉnh sửa văn bản. Các tệp CUR đi kèm với gói cài đặt chủ đề màn hình nền tùy chỉnh để đảm bảo rằng con trỏ Windows khớp với chủ đề màn hình nền tùy chỉnh.

## Thông số kỹ thuật ##

Tệp CUR là tệp hệ thống nhị phân có thể tìm thấy trên các thiết bị hoạt động trên hệ điều hành Microsoft Windows. Hình ảnh con trỏ CUR có các kích thước tiêu chuẩn khác nhau như 16×16, 32×32, v.v. Các tệp CUR rất giống với các tệp ICO; cả hai đều bao gồm các hình ảnh tĩnh nhỏ. Chỉ có phần mở rộng của tệp CUR và ICO là khác nhau. Hơn nữa, phần giải thích về điểm phát sóng trong tiêu đề của tệp CUR khác với tệp ICO. Điểm phát sóng diễn giải độ lệch pixel từ góc trên cùng bên trái sang vị trí bạn đang trỏ chuột. Các hệ thống Windows vẫn đang sử dụng các tệp CUR, nhưng giờ đây, các con trỏ động thường có phần mở rộng tệp là ANI thay vì CUR.

## Lược Sử ##

Tệp CUR được tạo từ tệp ICO. Định dạng tệp CUR đầu tiên được tích hợp vào hệ điều hành Windows 1.0 của Microsoft vào năm 1981 để tạo thuận lợi cho việc sử dụng thương mại. Ngay sau đó, nhiều con trỏ tương tác hơn đã được giới thiệu cho phép người dùng sửa đổi tùy chọn con trỏ của họ từ các tùy chọn được cài đặt sẵn. Tuy nhiên, bạn có thể dễ dàng tự chỉnh sửa tệp CUR ngay cả khi bạn không đủ kiến thức kỹ thuật.


## Ví dụ CUR ##

Các tệp CUR có thể được tìm thấy tại *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Định dạng tệp CUR" >}}

