{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Tệp tủ Windows",
  "description":"Tìm hiểu về định dạng tệp CAB và API có thể tạo và mở tệp CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp CAB là gì? ##

Tệp có phần mở rộng .cab thuộc về tệp tủ cửa sổ thuộc danh mục tệp hệ thống. Đây là tệp được lưu ở định dạng tệp lưu trữ trong các phiên bản Microsoft Windows hỗ trợ thuật toán dữ liệu nén, chẳng hạn như [LZX](/vi/compression/lzx/), Quantum và [ZIP](/vi/compression/zip/ ). Tệp được sử dụng quan trọng khi người dùng hoặc nhà phát triển muốn chứa và chia sẻ tệp và dữ liệu cài đặt phần mềm. Các tính năng nén dữ liệu không mất dữ liệu và chứng nhận kỹ thuật số có trong các tệp này làm cho tệp này trở nên hoàn hảo để lưu trữ và chia sẻ các tệp đó. Nó hỗ trợ các trình cài đặt khác nhau của Microsoft như Trình cài đặt thiết bị, API SetUp và AdvPak.

## Lược Sử ##

Tệp CAB là loại tệp nén dữ liệu được phát triển bởi Microsoft. Ban đầu nó được gọi là "Diamond", nhưng sau đó nó được gọi phổ biến là tệp CAB, viết tắt của từ "Cabinet"

## Đặc điểm kỹ thuật ##

Một tệp CAB thường có thể chứa tối đa 65535 thư mục, do đó, mỗi thư mục có thể chứa tối đa 65536 tệp. Cơ chế lưu trữ tệp CAB tiết kiệm thời gian và không gian vì nó lưu từng thư mục dưới dạng một khối nén thay vì nén và lưu trữ từng tệp riêng biệt. Các thư mục trống không thể được lưu trữ trong các thư mục lưu trữ CAB. Tệp CAB được Microsoft phát triển lần đầu tiên và được sử dụng trong nhiều trình cài đặt khác nhau, chẳng hạn như InstallShield với định dạng hơi khác. Các tệp CAB thường được kết nối với các chương trình tự giải nén. Các tệp Microsoft CAB có thể dễ dàng nhận ra do điểm đánh dấu duy nhất của chúng giúp xác định định dạng. Điểm đánh dấu duy nhất cho tất cả các tệp Microsoft CAB là tiền tố bốn từ, MSCF. Nhìn thấy mã này, người dùng có thể dễ dàng phân biệt tệp Microsoft CAB với các tệp khác và sử dụng nó cho phù hợp trong các máy nén hoặc phiên bản. Các tệp có thể được nén với nhiều dữ liệu cài đặt phần mềm hơn hoặc dữ liệu hiện tại có thể được giải nén bằng phần mềm phù hợp.


## Ví dụ CAB ##

Ví dụ sau minh họa mối quan hệ giữa các tệp và thư mục trong cấu trúc tệp CAB:

{{< figure src="../cab.png" alt="Định dạng tệp CAB" >}}

## Tài liệu tham khảo ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
