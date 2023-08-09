{
  "date" : "2019-12-09",
  "keywords" :[ "tệp 3mf", "định dạng tệp 3mf", "tệp 3mf là gì", "tệp", "ví dụ 3mf", "phần mở rộng tệp 3mf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Tìm hiểu về định dạng tệp 3MF và các API có thể mở và tạo tệp 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Tập tin 3MF là gì?

3MF, Định dạng Sản xuất 3D, được các ứng dụng sử dụng để hiển thị các mô hình đối tượng 3D cho nhiều ứng dụng, nền tảng, dịch vụ và máy in khác. Nó được xây dựng để tránh các giới hạn và sự cố trong các định dạng tệp 3D khác, như [STL](/vi/cad/stl/), để làm việc với các phiên bản mới nhất của máy in 3D. 3MF tương đối là một định dạng tệp mới đã được phát triển và xuất bản bởi tập đoàn 3MF. Nó đủ phong phú để mô tả đầy đủ một mô hình, giữ lại thông tin bên trong, màu sắc và các đặc điểm khác giúp nó có thể mở rộng để hỗ trợ các cải tiến mới trong in 3D. Định dạng này có thể mở rộng, có thể được áp dụng rộng rãi và không có vấn đề cản trở các định dạng tệp được sử dụng rộng rãi khác.

## Lịch sử tóm tắt về định dạng tệp 3MF

Những hạn chế hiện có trong các định dạng tệp mô tả mô hình có sẵn, chẳng hạn như STL và các định dạng khác, khiến các thương hiệu hàng đầu phải tập hợp lại và tạo ra một định dạng tệp có thể mở rộng hơn cho in 3D. Một cân nhắc quan trọng là cách các ứng dụng truyền dữ liệu mô hình tới máy in 3D. Do đó, tập đoàn 3MF đã ra đời để hỗ trợ một định dạng tệp 3D mới có tên là 3MF với mục đích làm cho nó đủ khả năng mở rộng để đáp ứng nhu cầu in 3D. Một số công ty là một phần của tập đoàn này bao gồm Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP và những công ty khác. Microsoft đã tặng định dạng tệp 3D đang thực hiện để làm điểm khởi đầu cho sự hợp tác phát triển hơn nữa đặc tả kỹ thuật của Hiệp hội 3MF.

## Định dạng tệp 3MF - Thông tin khác

3MF là một định dạng dữ liệu dựa trên XML - XML nén mà con người có thể đọc được - bao gồm các định nghĩa cho dữ liệu liên quan đến sản xuất 3D, bao gồm khả năng mở rộng của bên thứ ba cho dữ liệu tùy chỉnh. Định dạng tệp 3MF được thiết kế có tính đến những hạn chế và vấn đề mà các định dạng tệp 3D khác gặp phải. Điều này dẫn đến việc xây dựng định dạng tệp 3MF đó là:

* **Hoàn thành:** Chứa tất cả thông tin về mô hình, vật liệu và thuộc tính cần thiết trong một kho lưu trữ duy nhất
* **Con người có thể đọc được:** Sử dụng các cấu trúc phổ biến như OPC, [ZIP](/vi/compression/zip/) và XML để dễ dàng phát triển
* **Đơn giản:** Một đặc tả ngắn gọn, rõ ràng, giúp cho việc phát triển trở nên dễ dàng và xác nhận nhanh chóng
* **Có thể mở rộng:** Tận dụng không gian tên XML cho phép cả phần mở rộng công khai và riêng tư trong khi vẫn duy trì khả năng tương thích
* **Rõ ràng:** Các bài kiểm tra tuân thủ và ngôn ngữ rõ ràng đảm bảo tệp luôn nhất quán từ kỹ thuật số đến vật lý
* **Miễn phí:** Truy cập và triển khai thông số kỹ thuật 3MF đang và sẽ luôn miễn phí tiền bản quyền, bằng sáng chế và giấy phép

Thông số kỹ thuật cho định dạng tệp 3MF được lưu trữ trên [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) để truy cập công khai và cập nhật liên tục. Phiên bản được xuất bản hiện tại là 1.2.3 mô tả tập hợp các quy ước sử dụng XML và các công nghệ sẵn có rộng rãi khác để mô tả nội dung và hình thức của một hoặc nhiều mô hình 3D. Các nhà phát triển, những người muốn xây dựng hệ thống để xử lý các định dạng tệp 3MF, có thể tham khảo các thông số kỹ thuật này cho mục đích triển khai.

## Thông số kỹ thuật định dạng tệp 3MF

Định dạng tệp 3MF sử dụng thông số kỹ thuật Đóng gói Mở ở dạng lưu trữ ZIP cho kiểu máy vật lý của nó. Nó bao gồm một tập hợp các phần và mối quan hệ được xác định rõ ràng nhằm đáp ứng đầy đủ mục đích cụ thể trong tài liệu. Điều này cũng làm cho định dạng tuân theo tính năng gói bao gồm chữ ký điện tử và hình thu nhỏ.

### Tài liệu 3MF - Tổng quan

Một tài liệu 3MF điển hình trông như sau:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Tải trọng bao gồm toàn bộ bộ phận cần thiết để xử lý phần Mô hình 3D. Tất cả nội dung được sử dụng để sản xuất một đối tượng được mô tả trong tải trọng 3D PHẢI có trong Tài liệu 3MF. Mô tả của từng phần tài liệu cùng với trạng thái của nó theo yêu cầu hoặc tùy chọn được đưa ra trong bảng sau.


|**Tên**|**Mô tả**|**Nguồn mối quan hệ**|**Bắt buộc/Tùy chọn**
--- | --- | --- | ---
|Mô hình 3D|Chứa mô tả của một hoặc nhiều đối tượng 3D để sản xuất.|Gói|BẮT BUỘC
|Thuộc tính cốt lõi|Phần OPC chứa các thuộc tính tài liệu khác nhau.|Gói|TÙY CHỌN
|Nguồn gốc chữ ký số|Phần OPC là gốc của chữ ký số trong gói.|Gói|TÙY CHỌN
|Chữ ký số|Các phần OPC mà mỗi phần chứa một chữ ký số.|Nguồn gốc chữ ký số|TÙY CHỌN
|Chứng chỉ chữ ký số|Các bộ phận OPC có chứa chứng chỉ chữ ký số.|Chữ ký số|TÙY CHỌN
|PrintTicket|Cung cấp cài đặt sẽ được sử dụng khi xuất (các) đối tượng 3D trong phần Mô hình 3D.|Mô hình 3D|TÙY CHỌN
|Hình thu nhỏ|Chứa hình ảnh JPEG hoặc PNG nhỏ đại diện cho các đối tượng 3D trong gói hoặc toàn bộ gói.|Gói|TÙY CHỌN
|Kết cấu 3D|Chứa họa tiết được sử dụng để áp dụng màu cho đối tượng 3D trong phần Mô hình 3D (có sẵn cho các phần mở rộng)|Mô hình 3D|TÙY CHỌN
|Các bộ phận tùy chỉnh|Các bộ phận OPC được liên kết với siêu dữ liệu|Gói hàng|TÙY CHỌN

[Các bộ phận và mối quan hệ](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Mô hình 3D](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Tài nguyên đối tượng](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Tài nguyên vật liệu](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) và [Tính năng của gói](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) của thông số kỹ thuật tài liệu cung cấp thông tin chi tiết về tài liệu 3MF.

## Người giới thiệu ##

* [Thông số định dạng tệp 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Theo Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

