{
  "date" : "2021-26-08",
  "keywords" :[ "tệp dcr", "định dạng tệp dcr", "tệp dcr là gì", "tệp", "ví dụ dcr", "phần mở rộng tệp dcr","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Tệp ảnh RAW của máy ảnh kỹ thuật số",
  "description":"Tìm hiểu về định dạng tệp DCR và các API có thể tạo và mở tệp DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Tập tin DCR là gì? ##
Một tệp có phần mở rộng dcr chứa nội dung của ảnh kỹ thuật số được lưu ở định dạng RAW (DCR) của Máy ảnh kỹ thuật số Kodak. DCR là viết tắt của **Digital Camera Raw**; chứa phiên bản không nén và không mất dữ liệu của dữ liệu hình ảnh được chụp bởi máy ảnh kỹ thuật số Kodak. Các nhiếp ảnh gia chuyên nghiệp thích sử dụng các tệp này vì chúng lưu trữ hình ảnh với chất lượng cao hơn các định dạng hình ảnh nén chất lượng thấp.

## Định dạng tệp DCR
DCR là một định dạng độc quyền được phát triển bởi Công ty Eastman Kodak; được gọi đơn giản là Kodak. Tệp hình ảnh Digital Camera Raw (DCR) chứa dữ liệu được xử lý tối thiểu từ cảm biến hình ảnh của máy ảnh kỹ thuật số. Các tệp này chưa được xử lý và do đó chưa sẵn sàng để in hoặc chỉnh sửa bằng trình chỉnh sửa đồ họa bitmap.
Thông thường, bộ chuyển đổi thô xử lý hình ảnh trong không gian màu bên trong có gam màu rộng, nơi có thể thực hiện độ chính xác và tinh chỉnh trước khi chuyển đổi sang định dạng tệp raster, chẳng hạn như TIFF hoặc JPEG để lưu trữ, in hoặc thao tác thêm.
### Nội dung tệp
Cấu trúc của các tệp thô thường tuân theo một mẫu chung:
- Một tiêu đề tệp ngắn chứa chỉ báo về thứ tự byte của tệp.
- Siêu dữ liệu của cảm biến máy ảnh được yêu cầu để giải thích dữ liệu hình ảnh của cảm biến, bao gồm các thuộc tính của CFA, kích thước của cảm biến và cấu hình màu của cảm biến.
- Siêu dữ liệu hình ảnh có thể hữu ích để đưa vào bất kỳ môi trường hoặc cơ sở dữ liệu CMS nào. Một số tệp thô chứa phần siêu dữ liệu được chuẩn hóa với dữ liệu ở định dạng Exif.
- Một hình thu nhỏ hình ảnh.
- Chuyển đổi JPEG kích thước đầy đủ của hình ảnh, được sử dụng để xem trước tệp trên bảng điều khiển LCD của máy ảnh.
- Trong trường hợp quét phim điện ảnh, mã thời gian, mã khóa hoặc số khung trong chuỗi tệp đại diện cho chuỗi khung trong cuộn được quét.
- Dữ liệu hình ảnh cảm biến
### Dữ liệu hình ảnh cảm biến
Tệp thô đóng vai trò trong nhiếp ảnh kỹ thuật số tương tự như phim chụp ảnh đóng vai trò trong chụp ảnh phim. Do đó, các tệp thô chứa dữ liệu có độ phân giải đầy đủ khi được đọc từ mỗi pixel cảm biến hình ảnh của máy ảnh. Cảm biến của máy ảnh gần như liên tục được phủ một CFA (Mảng bộ lọc màu. Nó có thể được sử dụng trong chuyển đổi hình ảnh dải động cao khi có sẵn dữ liệu định dạng thô; như một giải pháp thay thế đơn giản hơn cho phương pháp HDI đa phơi sáng để chụp ba hình ảnh riêng biệt.


## Người giới thiệu ##

* [Định dạng ảnh thô - Theo Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [Tệp DCR là gì](https://expertphotography.com/dcr-file/)

