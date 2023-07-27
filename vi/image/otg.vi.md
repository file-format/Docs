{
  "date" : "2020-01-10",
  "keywords" :[ "tệp otg", "định dạng tệp otg", "tệp otg là gì", "tệp", "ví dụ otg", "phần mở rộng tệp otg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Định dạng tệp mẫu bản vẽ OpenDocument",
  "description":"Tìm hiểu về định dạng tệp OTG và các API có thể tạo và mở tệp OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Tệp OTG là gì?

Tệp OTG là mẫu bản vẽ được tạo bằng tiêu chuẩn OpenDocument tuân theo Ứng dụng Office OASIS [đặc điểm kỹ thuật 1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Nó đại diện cho tổ chức mặc định của các thành phần vẽ cho một hình ảnh vector có thể được sử dụng để nâng cao hơn nữa nội dung của tệp. Các tệp OTF giống như bất kỳ tệp dựa trên định dạng OpenDocument nào khác dựa trên định dạng XML để thể hiện nội dung của tài liệu. Có thể xem các tệp OTF bằng cách mở chúng trong bất kỳ trình soạn thảo văn bản hoặc XML tiêu chuẩn nào.

## Thông số kỹ thuật định dạng tệp OTG ##

Định dạng tệp OTG dựa trên định dạng OpenDocument XML có lược đồ được thiết lập tốt. Cấu trúc của từng thành phần của định dạng OpenDocument được biểu thị bằng một phần tử có các thuộc tính liên quan và chung cho tất cả các loại tài liệu như tài liệu văn bản, bảng tính hoặc tệp bản vẽ. OTG, là một mẫu bản vẽ, sử dụng rộng rãi các thông số kỹ thuật Nội dung đồ họa bao gồm:

* Tính năng trang nâng cao cho ứng dụng đồ họa
* Vẽ hình
* Khung
* Hình dạng 3D
* Hình dạng tùy chỉnh
* Hình dạng trình bày
* Hoạt ảnh trình bày
* Hoạt ảnh trình bày SMIL
* Sự kiện trình bày
* Trình bày các trường văn bản
* Nội dung tài liệu trình bày

### Tính năng trang nâng cao dành cho ứng dụng đồ họa ###
#### Handout Master ####

Phần tử Handout Master là một mẫu để tự động tạo các trang tài liệu phát cho các ứng dụng hỗ trợ in các trang đó.
Các thuộc tính có thể được liên kết với `<style:handout-master> phần tử ` là:

|Bố cục|Thuộc tính|Mô tả
---|---|---|
|Bố cục trang thuyết trình|bản trình bày:tên-bố cục trang thuyết trình|Liên kết đến `<style:presentation-page-layout> ` thuộc tính
|Bố cục trang|`kiểu:tên-bố cục trang` | Chỉ định bố cục trang chứa kích thước, đường viền và hướng của trang chính của tài liệu phân phát.
|Kiểu trang|`draw:style-name`|Gán thuộc tính định dạng bổ sung cho trang chính bản phân phát bằng cách gán kiểu trang vẽ.|
|Khai báo tiêu đề| `bản trình bày: tên-tiêu đề sử dụng`| Chỉ định tên của khai báo trường tiêu đề được sử dụng cho tất cả các trường tiêu đề được hiển thị trên trang chính của tài liệu phân phát.
|Chân trang Khai báo| presentation:use-footer-name|Chỉ định tên của khai báo trường chân trang được sử dụng cho tất cả các trường chân trang được hiển thị trên trang chính của tài liệu phân phát.
|Khai báo Ngày và Giờ|sử dụng tên-ngày-giờ|Chỉ định tên của khai báo trường ngày-giờ được sử dụng cho tất cả các trường ngày-giờ được hiển thị trên trang chính của tài liệu phát.

### Vẽ Hình ###
Định dạng OpenDocument hỗ trợ một số hình vẽ có thể được sử dụng bởi bất kỳ loại tài liệu nào.

|Hình dạng|Thuộc tính được liên kết| yếu tố
---|---|---|
Hình chữ nhật - `<draw:rect> `|Vị trí, Kích thước, Kiểu, Lớp, Chỉ mục Z, ID, ID chú thích, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Góc tròn|Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm keo, Văn bản
Dòng `<draw:line> `|Kiểu, Lớp, Chỉ mục Z, ID, ID chú thích và Chuyển đổi, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Điểm bắt đầu, Điểm kết thúc|Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm keo, Văn bản
Đa tuyến `<draw:polyline> `| Vị trí, Kích thước, Hộp xem, Kiểu, Lớp, Chỉ mục Z, ID, ID Phụ đề và Chuyển đổi, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Điểm| Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm kết dính, Văn bản
Đa giác `<draw:polygon> `|Vị trí, Kích thước, Hộp xem, Kiểu, Lớp, Chỉ mục Z, ID, ID chú thích và Chuyển đổi, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Điểm|Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm keo, Văn bản
|Đa giác đều `<draw:regular-polygon> `|Vị trí, Kích thước, Kiểu, Lớp, Chỉ mục Z, ID, ID chú thích và Chuyển đổi, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Lõm, Góc, Độ sắc nét|Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm keo, Văn bản
|Paht `<draw:path> `|Vị trí, Kích thước, Hộp xem, Kiểu, Lớp, Chỉ mục Z, ID, ID Chú thích và Chuyển đổi, Neo văn bản, nền bảng, vị trí kết thúc vẽ, Dữ liệu đường dẫn| Tiêu đề, Mô tả dài, Trình xử lý sự kiện, Điểm kết dính, Văn bản

### Khung hình ###
Khung, trong tài liệu bản vẽ là một vùng chứa hình chữ nhật chứa các hộp văn bản, hình ảnh hoặc đối tượng. Các khung hỗ trợ các tính năng bổ sung như đường viền, bản đồ hình ảnh và siêu liên kết. Một khung có thể chứa một đối tượng cũng như một hình ảnh, do đó cho phép có nhiều phiên bản của một đối tượng. Các ứng dụng hiển thị phần tử tương ứng dựa trên sự hỗ trợ tốt nhất.

Khung có thể chứa:
* Hộp văn bản
* Các đối tượng được biểu thị ở định dạng OpenDocument hoặc ở định dạng nhị phân dành riêng cho đối tượng
* Hình ảnh
* Applet
* Bổ sung
* Khung nổi

Một khung được chứa trong một tài liệu như hình bên dưới.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Người giới thiệu ##
* [Định dạng Tài liệu Mở OASIS dành cho Ứng dụng Office](https://www.oasis-open.org/committees/tc_home.php?wg_abrev=office)
* [Định dạng Tài liệu Mở - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

