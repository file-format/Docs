{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "file", "extension", "format", "video format","Tệp SWF là gì", "định dạng tệp swf", "trình phát tệp swf","cách mở tệp swf"] ,
  "title" :"Tệp SWF - Định dạng tệp phim Shockwave Flash",
  "description":"Tìm hiểu về tệp SWF là gì và các API có thể tạo cũng như hiển thị cách mở tệp SWF.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp SWF là gì?

Tệp SWF là tệp hoạt hình được tạo bằng Adobe Flash. Nó có thể chứa các loại phần tử khác nhau như văn bản, hình ảnh vector, hình ảnh raster, mô tả hành động, các đối tượng như hình tròn, đường thẳng, hình vuông và hình chữ nhật để tạo hoạt ảnh. Các tệp SWF sắp xếp các mục đa phương tiện này trong các khung hình có thể phát trên các khung hình khác nhau trên giây (khung hình/giây). SWF có nghĩa là Tệp web ngắn nhưng còn được biết là có Định dạng Shockwave.

Các ứng dụng có thể *mở tệp SWF** bao gồm Adobe Flash Player (hiện đã ngừng hoạt động) và Eltima Elmedia Player.

## Định dạng tệp SWF - Thông tin khác

Các tệp SWF đã được sử dụng để lưu trữ dưới dạng tệp nhị phân vào đĩa. Định dạng tệp SWF được sử dụng để phát triển hoạt ảnh và trò chơi có thể được nhúng vào các trang web và cũng có thể chơi độc lập. Nó cũng hỗ trợ video và âm thanh giúp các nhà phát triển có nhiều lựa chọn để tạo các ứng dụng đa phương tiện tương tác. Các tệp SWF có thể được phát trong các trình duyệt web đã cài đặt Adobe Shockwave. Adobe Flash đã ngừng hoạt động vào tháng 12 năm 2020 do thời gian sử dụng ngắn và các vấn đề bảo mật.

## Lịch sử tóm tắt về định dạng tệp SWF

Định dạng tệp SWF ban đầu được thiết kế bởi FutureWave Software, để hiển thị hoạt ảnh với ý định chạy trên phần mềm trình phát trên bất kỳ hệ thống nào có kết nối mạng chậm hơn, trong khi vẫn giữ kích thước tệp nhỏ. Vào tháng 12 năm 1996, Macromedia sở hữu FutureWave và chuyển đổi thành Macromedia Flash 1.0.

Năm 2005, Adobe mua lại Macromedia, hãng đã công bố SWF là một phần của dự án nguồn mở của mình vào năm 2008. Trong cùng năm đó, Adobe đã phát hành mã cho các công cụ web phổ biến trên thế giới để cho phép chúng thu thập thông tin và lập chỉ mục các tệp SWF. Tuy nhiên, khi các tệp SWF dường như trở thành một định dạng tiêu chuẩn để xuất bản nội dung Flash trên internet, SWF đã được sửa đổi thành Định dạng Web Nhỏ.

## Cấu trúc tệp SWF

Đường dẫn là thành phần đồ họa cơ bản trong SWF, là một chuỗi các phân đoạn của các thành phần cơ bản, từ các đường đơn giản đến các đường cong Bezier. Những yếu tố đơn giản này cũng giúp tạo ra các nguyên hàm bổ sung khác như hình khối, hình elip và thậm chí cả văn bản. Các nguyên mẫu đồ họa trong SWF có sự tương đồng với các yếu tố đồ họa của các định dạng khác như SVG và MPEG-4 BIFS.

Hiển thị danh sách và sử dụng lại/đổi tên các phần tử đã được xác định cũng được định dạng cho phép. Định dạng luồng nhị phân của SWF có thể được so sánh với các nguyên tử QuickTime tương tự về thẻ, kích thước và tải trọng. Định dạng luồng nhị phân cho phép người chơi cũ bỏ qua nội dung không được hỗ trợ. Mặc dù các phiên bản gốc của SWF bị giới hạn trong việc cung cấp đồ họa và hình ảnh vector, do đó các phiên bản mới cũng cho phép cả nội dung âm thanh và video.

Một API 3D cấp thấp mới của Flash Player có tên là “Stage3D” đã được giới thiệu trong phiên bản 11. API này được hình dung là bản sao của OpenGL hoặc Direct3D. Stage3D xác định màu sắc trong một ngôn ngữ cấp thấp gọi là Adobe Graphics Assembly Language (AGAL). Sau đây là một vài kiểu dữ liệu cơ bản của định dạng tệp SWF.

### Tọa độ

Tọa độ XY ở định dạng tệp SWF được lưu dưới dạng số nguyên và được đo bằng đơn vị gọi là twip. Một twip bao gồm 1/20 pixel logic. Pixel logic và pixel màn hình giống nhau khi tệp được phát mà không chia tỷ lệ ở mức 100%.

### Các kiểu số nguyên và thứ tự byte

Các loại số nguyên có dấu và không dấu 8, 16, 32 và 64 bit được cho phép ở định dạng tệp SWF. Thứ tự byte cuối nhỏ được sử dụng để lưu trữ các giá trị số nguyên. Mặc dù trong phạm vi byte, thứ tự bit được lưu trữ trong big-endian. Tất cả các giá trị số nguyên phải được căn chỉnh theo byte. Các số nguyên đã ký được biểu diễn bằng cách sử dụng các mẫu bit -complement của 2 truyền thống.

### Số điểm cố định

Hai loại số điểm cố định được hỗ trợ bởi định dạng tệp SWF tức là 32 và 16 bit.

### Số dấu phẩy động

SWF 8 và phiên bản mới hơn sử dụng ba loại số dấu phẩy động (FLOAT, FLOAT 16, DOUBLE) tương thích với Tiêu chuẩn IEEE 754 của các loại dấu phẩy động.

### Số nguyên được mã hóa

Một loại số nguyên được mã hóa được hỗ trợ bởi SWF 9 trở lên với số lượng byte thay đổi.

## Người giới thiệu

* [Định dạng tệp SWF](https://vi.wikipedia.org/wiki/Swf)

