{
  "date" : "2019-10-11",
  "keywords" :[ "tệp vsdx", "định dạng tệp vsdx", "tệp vsdx là gì", "tệp", "ví dụ vsdx", "phần mở rộng tệp vsdx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Tìm hiểu về định dạng tệp VSDX và các API có thể tạo và mở tệp VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VSDX là gì?

Các tệp có phần mở rộng .vsdx đại diện cho định dạng tệp Microsoft Visio được giới thiệu từ Microsoft Office 2013 trở đi. Nó được phát triển để thay thế định dạng tệp nhị phân, [.VSD](/vi/image/vsd/), được hỗ trợ bởi các phiên bản trước của Microsoft Visio. Nó cũng được hỗ trợ trên Dịch vụ Visio trong Microsoft SharePoint Server 2013 và không yêu cầu định dạng tệp trung gian để xuất bản lên SharePoint Server. Các tệp Visio được sử dụng để tạo các bản vẽ có chứa các đối tượng trực quan, sơ đồ luồng, sơ đồ UML, luồng thông tin, sơ đồ tổ chức, sơ đồ phần mềm, bố cục mạng, mô hình cơ sở dữ liệu, ánh xạ đối tượng và các thông tin tương tự khác. Các tệp được tạo bằng Visio cũng có thể được xuất sang các định dạng tệp khác nhau, chẳng hạn như [PNG](/vi/image/png/), [BMP](/vi/image/bmp/), [PDF](/vi/pdf/) và các định dạng khác.

## Định dạng tệp ##

Các tệp VSDX dựa trên Quy ước đóng gói mở và XML và các nhà phát triển có thể hưởng lợi từ định dạng này bằng cách tìm hiểu cách làm việc với các tệp này theo chương trình. Định dạng kế thừa nhiều cấu trúc XML giống như các phần của nó từ định dạng tệp Bản vẽ Visio XML (.vdx). Khả năng tương tác với các tệp Visio được tăng lên đáng kể do phần mềm bên thứ ba có thể thao tác với các tệp Visio ở cấp độ định dạng tệp.

Một số loại tệp khác bao gồm định dạng tệp Visio 2013 bao gồm:

* .vsdm (Bản vẽ hỗ trợ macro Visio)
* .vssx (khuôn in Visio)
* .vssm (Sprint hỗ trợ macro Visio)
* .vstx (mẫu Visio)
* .vstm (mẫu hỗ trợ macro Visio)

Về cơ bản, định dạng tệp Visio 2013 sử dụng một phương tiện có cấu trúc để lưu trữ dữ liệu ứng dụng cùng với các tài nguyên liên quan trong một kho lưu trữ chẳng hạn như [ZIP](/vi/compression/zip/). Tệp ZIP có thể được trích xuất bằng bất kỳ tiện ích trích xuất tiêu chuẩn nào có chứa các loại tệp khác. Bạn chỉ có thể thay thế phần mở rộng tệp .vsdx bằng .zip trong cửa sổ khám phá để xem nội dung bên trong tệp VSDX.

Mỗi tệp Visio được gọi là gói chứa các tệp hoặc phần khác. Một phần của gói có thể là một tệp XML, một hình ảnh hoặc thậm chí là một giải pháp VBA. Các phần bên trong gói có thể được chia thành các phần "tài liệu" và "mối quan hệ".

### Tài liệu ###

Các phần tài liệu chứa nội dung và siêu dữ liệu thực tế của tệp Visio, chẳng hạn như tên của tệp, trang đầu tiên và tất cả các hình có trong tệp, thậm chí cả các kết nối dữ liệu cho các hình. Các tệp hình ảnh và văn bản trong gói được coi là các phần tài liệu.

### Các mối quan hệ ###

Các phần mối quan hệ của tệp Visio được lưu trữ trong thư mục "\_rels" và mô tả cách các phần trong gói có liên quan đến từng phần. Nó cũng cung cấp cấu trúc của tập tin. Một tài liệu XML độc lập sử dụng mối quan hệ cha/con của các phần tử để xác định mối quan hệ của các thực thể với nhau. Định dạng tệp Visio 2013 hợp lệ chứa đúng bộ phần và gói chứa mối quan hệ giữa các phần.

Các phần quan hệ là các tài liệu XML mô tả các mối quan hệ giữa các phần tài liệu khác nhau trong gói. Chúng xác định mối liên kết giữa hai mục: một nguồn được chỉ định (được xác định bởi tên và vị trí của tệp mối quan hệ) và một phần tài liệu đích được chỉ định. Ví dụ: các phần quan hệ được sử dụng để mô tả các hình dạng chính được liên kết với tệp, cách các trang liên quan đến tệp và với nhau hoặc cách hình ảnh và đối tượng liên quan đến một trang cụ thể.

## Người giới thiệu ##

* [Giới thiệu về Định dạng tệp Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

