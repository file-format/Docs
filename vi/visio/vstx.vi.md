{
  "date" : "2019-10-11",
  "keywords" :[ "tệp vstx", "định dạng tệp vstx", "tệp vstx là gì", "tệp", "ví dụ vstx", "phần mở rộng tệp vstx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Định dạng tệp Microsoft Visio",
  "description":"Tìm hiểu về định dạng tệp VSTX và các API có thể tạo và mở tệp VSTX.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VSTX là gì?

Các tệp có phần mở rộng .vstx là các tệp mẫu vẽ được tạo bằng Microsoft Visio 2013 trở lên. Các tệp VSTX này cung cấp điểm bắt đầu để tạo bản vẽ Visio, được lưu dưới dạng tệp [.VSDX](/vi/image/vsdx/), với bố cục và cài đặt mặc định. Nói chung, các tệp Visio được sử dụng để tạo các bản vẽ có chứa các đối tượng trực quan, lưu đồ, sơ đồ UML, luồng thông tin, sơ đồ tổ chức, sơ đồ phần mềm, bố cục mạng, mô hình cơ sở dữ liệu, ánh xạ đối tượng và các thông tin tương tự khác. Các tệp được tạo bằng Visio cũng có thể được xuất sang các định dạng tệp khác nhau, chẳng hạn như [PNG](/vi/Image/PNG/), [BMP](/vi/Image/BMP/), [PDF](/vi/pdf/) và các định dạng khác. Các chương trình mở tệp VSTX bao gồm Microsoft Visio cho Windows và Mac cho phép bạn mở các tệp này để xem và chỉnh sửa. Nó cũng cho phép chuyển đổi định dạng tệp Visio sang một số định dạng khác.

# Định dạng tệp VSTX #

"X" trong phần mở rộng tệp đề cập đến định dạng tệp OpenOffice được Microsoft giới thiệu dưới dạng định dạng tệp lưu trữ [ZIP](/vi/compression/zip/) để thay thế các định dạng tệp nhị phân được hỗ trợ trước đó. Do đó, các tệp VSTX dựa trên định dạng tệp XML của các thông số kỹ thuật của OpenOffice không giống như định dạng tệp [.VST](/vi/image/vst/) ở định dạng nhị phân.

Các tệp VSDX dựa trên Quy ước đóng gói mở và XML và các nhà phát triển có thể hưởng lợi từ định dạng này bằng cách tìm hiểu cách làm việc với các tệp này theo chương trình. Định dạng kế thừa nhiều cấu trúc XML giống như các phần của nó từ định dạng tệp Bản vẽ Visio XML (.vdx). Khả năng tương tác với các tệp Visio được tăng lên đáng kể do phần mềm bên thứ ba có thể thao tác với các tệp Visio ở cấp độ định dạng tệp.

Một số loại tệp khác bao gồm định dạng tệp Visio 2013 bao gồm:

* .vsdm (Bản vẽ hỗ trợ macro Visio)
* .vssx (khuôn in Visio)
* .vssm (Sprint hỗ trợ macro Visio)
* .vstx (mẫu Visio)
* .vstm (mẫu hỗ trợ macro Visio)

Về cơ bản, định dạng tệp Visio 2013 sử dụng một phương tiện có cấu trúc để lưu trữ dữ liệu ứng dụng cùng với các tài nguyên liên quan trong một kho lưu trữ chẳng hạn như [ZIP](/vi/Compression/ZIP/). Tệp ZIP có thể được trích xuất bằng bất kỳ tiện ích trích xuất tiêu chuẩn nào có chứa các loại tệp khác. Bạn chỉ có thể thay thế phần mở rộng tệp .VSTX bằng .ZIP trong cửa sổ khám phá để xem nội dung bên trong tệp VSTX.

Mỗi tệp Visio được gọi là gói chứa các tệp hoặc phần khác. Một phần của gói có thể là một tệp XML, một hình ảnh hoặc thậm chí là một giải pháp VBA. Các phần bên trong gói có thể được chia thành các phần "tài liệu" và "mối quan hệ".

### Tài liệu ###

Các phần tài liệu chứa nội dung và siêu dữ liệu thực tế của tệp Visio, chẳng hạn như tên của tệp, trang đầu tiên và tất cả các hình có trong tệp, thậm chí cả các kết nối dữ liệu cho các hình. Các tệp hình ảnh và văn bản trong gói được coi là các phần tài liệu.

### Các mối quan hệ ###

Các phần mối quan hệ của tệp Visio được lưu trữ trong thư mục "_rels" và mô tả cách các phần trong gói có liên quan đến từng phần. Nó cũng cung cấp cấu trúc của tập tin. Một tài liệu XML độc lập sử dụng mối quan hệ cha/con của các phần tử để xác định mối quan hệ của các thực thể với nhau. Định dạng tệp Visio 2013 hợp lệ chứa đúng bộ phần và gói chứa mối quan hệ giữa các phần.

Các phần quan hệ là các tài liệu XML mô tả các mối quan hệ giữa các phần tài liệu khác nhau trong gói. Chúng xác định mối liên kết giữa hai mục: một nguồn được chỉ định (được xác định bởi tên và vị trí của tệp mối quan hệ) và một phần tài liệu đích được chỉ định. Ví dụ: các phần quan hệ được sử dụng để mô tả các hình dạng chính được liên kết với tệp, cách các trang liên quan đến tệp và với nhau hoặc cách hình ảnh và đối tượng liên quan đến một trang cụ thể.

## Người giới thiệu ##

* [Giới thiệu về Định dạng tệp Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

