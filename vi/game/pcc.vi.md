{
  "date" : "2021-09-08",
  "keywords" :[ "tệp pcc", "định dạng tệp pcc", "tệp pcc là gì", "tệp", "ví dụ pcc", "phần mở rộng tệp pcc","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PCC của Mass Effect và các API có thể tạo và mở tệp PCC.",
  "title" :"PCC - Tệp Gói Hiệu ứng Khối lượng",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Tệp PCC là gì?

Tệp có đuôi .pcc là tệp [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) chứa dữ liệu trò chơi để sửa đổi nội dung trò chơi, chẳng hạn như mô hình, kết cấu và phòng. Mass Effect 2 và 3 là những game bắn súng đầu tiên dựa trên công cụ chơi game Unreal Engine 3. Trò chơi ban đầu được phát triển bởi [Bioware](https://www.bioware.com/about/), người đã giữ phần lớn tài nguyên trò chơi ở định dạng tệp PCC độc quyền của họ. Bioware đã được mua lại bởi Electronic Arts, một nhà xuất bản giải trí tương tác toàn cầu hàng đầu.

## Định dạng tệp PCC - Thông tin khác

Các tệp PCC chứa các cấu trúc nén và/hoặc không nén đóng góp vào tổ chức tệp tổng thể.

### Cấu trúc PCC nén

Tệp PCC được nén bao gồm các bảng và dữ liệu được phân đoạn thành các phần. Mỗi đoạn chứa một số khối nén khác nhau.

* `Tiêu đề khối` - Tiêu đề chung 16 byte, chứa thông tin về các khối.
* `Tiêu đề khối` - Tiêu đề 16 byte chứa thông tin về dữ liệu nén thô chứa trong biểu mẫu khối.

### Cấu trúc PCC không nén

Các tệp PCC không nén được chia thành năm phần sau.

* `Header` - chứa thông tin cơ bản về cấu trúc của tệp PCC.
* `Bảng tên` - chứa tên được tìm thấy bên trong gói bao gồm các lớp nhập, xuất và thuộc tính xuất.
* `Bảng nhập` - chứa tất cả các lớp và đối tượng được nhập bởi PCC.
* `Bảng xuất` - chứa tất cả các đối tượng được lưu trữ trong gói. Mỗi xuất khẩu có thể khác nhau về kích thước.

## Người giới thiệu

* [Me3Explorer - Định dạng tệp PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Trò chơi hiệu ứng hàng loạt](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Phần mềm sinh học](https://www.bioware.com/about/)

