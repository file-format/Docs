{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Tệp", "Định dạng", "Mở", "Đọc", "API", "MicroStation", "Hệ thống thiết kế đồ họa tương tác Intergraph" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Định dạng tệp thiết kế CAD của MicroStation",
  "description" :"Tìm hiểu về định dạng tệp DGN và API có thể tạo và mở tệp DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Tệp DGN là gì?

Tệp có phần mở rộng .dgn (Thiết kế) là tệp bản vẽ được tạo và hỗ trợ bởi các ứng dụng CAD như MicroStation và Hệ thống thiết kế đồ họa tương tác Intergraph. Nó được sử dụng để tạo và lưu các thiết kế cho các dự án xây dựng như đường cao tốc, cầu và các tòa nhà. Định dạng này tương tự như định dạng tệp [DWG](/vi/cad/dwg/) của Autodesk và được coi là đối thủ cạnh tranh của nó. Các tệp DNG có thể được lưu dưới dạng Định dạng tệp tiêu chuẩn của Intergraph hoặc V8 DGN. DGN có thể được chuyển đổi sang một số định dạng khác như DWG, [BMP](/vi/image/bmp/), [JPEG](/vi/image/jpeg/), [PDF](/vi/pdf/), [GIF](/vi/image/ gif/) và những thứ khác. Nó có thể được mở bằng Autodesk AutoCAD, Bentley View và Bentley Systems MicroStation ngoài các ứng dụng phần mềm khác như Corel PaintShop Photo Pro và các phiên bản IMSI TurboCAD Deluxe.

## Định dạng tệp V8 DGN

Tệp MicroStation V8 DGN bao gồm một hoặc nhiều kiểu máy. Một mô hình là một thùng chứa các phần tử. V8 DGN loại bỏ tất cả các ràng buộc dựa trên định dạng tệp đã có trong các phiên bản trước của MicroStation. Sau đây là danh sách các cải tiến trong định dạng tệp DGN.

* Giới hạn về số lượng cấp độ trong tệp DGN đã bị xóa và mỗi cấp độ được đặt tên và lưu trữ dưới dạng một phần tử.
* Kích thước vật lý tối đa của tệp DGN không có bất kỳ giới hạn nào và chỉ bị giới hạn bởi hệ điều hành (chẳng hạn như giới hạn NT là 4 GB)
* Kích thước tối đa của một phần tử là 128 KB.
* Không có giới hạn về kích thước tối đa của một ô.
* Tên ô được giới hạn trong khoảng 500 ký tự.
* Không có giới hạn về số lượng tài liệu tham khảo có thể được đính kèm vào tệp DGN.
* Một chuỗi đường, hình hoặc đường cong điểm có thể có tối đa 5000 đỉnh.
* Không có giới hạn về số lượng thành phần trong một chuỗi phức tạp hoặc hình dạng phức tạp.
* Không có giới hạn về số lượng nhóm đồ họa trong tệp DGN.
* Hàng rào song song với khung nhìn mà nó được đặt.
* Một dòng văn bản có thể chứa 65.535 ký tự.
* Không có giới hạn về kích thước tối đa của nút văn bản.
* Không có giới hạn về số nút văn bản trong tệp DGN.
* Mỗi phần tử có một mã định danh 64 bit duy nhất không thay đổi trong suốt vòng đời của phần tử.
* Mỗi phần tử có một dấu thời gian cho biết thời điểm thay đổi gần đây nhất.

## Người giới thiệu

* [DNG - Theo Wikipedia](https://vi.wikipedia.org/wiki/DGN)
* [Định dạng tệp DGN của MicroStation V8](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

