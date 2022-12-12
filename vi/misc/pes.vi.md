{
  "date" : "2021-07-29",
  "keywords" :[ "tệp pes", "định dạng tệp pes", "tệp pes là gì", "tệp", "ví dụ pes", "phần mở rộng tệp pes","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PES - Định dạng thêu Brother PE",
  "description":"Tìm hiểu về định dạng tệp PES và API có thể tạo và mở tệp PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Tệp Thêu PES là gì?

Tệp thêu PES là một tệp thiết kế có chứa hướng dẫn cho máy thêu/máy may. Nó được Brother Industries phát triển cho các máy thêu của họ nhưng sau đó được chính thức hóa thành định dạng tệp chung. Các tệp PES được máy may sử dụng để đọc hướng dẫn khâu mẫu trên vải. Các tệp này phục vụ hai mục đích; đầu tiên cung cấp thông tin thiết kế cho ứng dụng PE-Design do Brother Industries phát triển và thứ hai, cung cấp tên thiết kế, màu sắc và mã máy thêu như "dừng", "nhảy" và "cắt".

## Định dạng tệp PES - Thông tin khác

Tệp PES được lưu vào đĩa ở định dạng tệp nhị phân. Nó chứa nhiều phần có thông tin may được lưu trữ bằng phương pháp được xác định trước. Định dạng tệp PES như sau.

* Dữ liệu phiên bản - Cung cấp thông tin phiên bản và có thể là bất kỳ giá trị nào `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Giá trị tìm kiếm PEC - Một số nguyên cuối nhỏ 4 byte ngay sau dữ liệu phiên bản và biểu thị giá trị tìm kiếm cho phần PEC có chứa thông tin chi tiết thiết kế
* Phần PSE - Chứa thông tin thiết kế liên quan đến Brother PE-Design và có thể là các ứng dụng may khác
* Phần PCE - Có thể ở bất kỳ đâu trong tệp PSE nhưng được tham chiếu bởi Giá trị tìm kiếm PEC.

## Loại máy may sử dụng tệp PES

Các tệp PES chủ yếu được tạo bởi Phần mềm thiết kế PE được sử dụng với máy may Brother. Một số máy khác có thể hỗ trợ tệp PES bao gồm máy thêu gia đình Babylock và Bernina.

## Làm cách nào để chuyển đổi tệp PSE?

Ứng dụng phần mềm PE-Design có thể [chuyển đổi tệp PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) sang các định dạng khác như .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd hoặc .xxx. Có thể thực hiện bằng ứng dụng PE-Design bằng cách mở tệp và chọn Định dạng chuyển đổi.

## Người giới thiệu

* [Thiết kế PE - Sổ tay hướng dẫn](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

