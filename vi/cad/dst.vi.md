{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "file", "format", "extension", "API", "AutoCAD Sheet Set" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - Tập tin bảng tính AutoCAD",
  "description" :"Tìm hiểu về tệp .dst và các API có thể tạo và mở tệp DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Tệp DST là gì?

Tệp DST là tệp AutoCAD chứa các liên kết và thông tin để xác định các tập hợp trang tính. Chúng được lưu trữ trong thư mục lưu trữ bộ trang tính mặc định, AutoCAD Sheet Sets. Các tệp DST không chứa bố cục bản vẽ thực tế nhưng tham khảo các bố cục này từ các tệp [DWG](/vi/cad/dwg/) và [DWT](/vi/cad/dwt/) đã chọn được liên kết với các bộ trang tính này. Trong môi trường mạng, tất cả các thành viên trong nhóm phải có quyền truy cập mạng vào các tệp được liên kết này. Các tệp DST được lưu vào đĩa ở định dạng tệp [XML](/vi/web/xml/).

## Định dạng tệp DST - Thông tin khác

Các tệp DST được tạo bằng công cụ AutoDesk Sheet Set Manager (SSM). Khi ai đó trong nhóm truy cập tệp, tệp DST sẽ được mở trong thời gian ngắn và sau đó được lưu trữ trở lại với thông tin được cập nhật. Truy cập đồng thời vào cùng một tệp DST được quản lý bởi công cụ SSM hiển thị biểu tượng khóa khi tệp đang được truy cập.

Tại bất kỳ thời điểm cụ thể nào, trạng thái trang tính có thể ở bất kỳ trạng thái nào sau đây.

* Trang tính có sẵn để chỉnh sửa.
* Trang tính đã bị khóa.
* Trang tính bị thiếu hoặc được tìm thấy ở một vị trí thư mục không mong muốn.

## Người giới thiệu

* [Giới thiệu về cách sử dụng Bộ trang tính DST](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Tìm hiểu về Sheet Sets](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Làm chủ bộ trang tính AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

