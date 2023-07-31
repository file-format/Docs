{
  "date" : "2019-10-11",
  "keywords" :[ "tệp vsdm", "định dạng tệp vsdm", "tệp vsdm là gì", "tệp", "ví dụ vsdm", "phần mở rộng tệp vsdm","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Định dạng tệp bản vẽ Microsoft Visio",
  "description":"Tìm hiểu về định dạng tệp VSDM và API có thể tạo và mở tệp VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VSDM là gì?

Các tệp có phần mở rộng .vsdm là các tệp vẽ được tạo bằng ứng dụng Microsoft Visio hỗ trợ macro. Các tệp VSDM là các bản vẽ OPC/XML tương tự như VSDX nhưng cũng cung cấp khả năng chạy macro khi tệp được mở. Macro là các hành động/bước do người dùng xác định được phát triển trong Visual Basic for Applications (VBA) và có thể được sử dụng để thực hiện các tác vụ lặp đi lặp lại. Định dạng tệp VSDM được giới thiệu cùng với sự ra mắt của Microsoft Visio 2013. Các tệp Visio được sử dụng để tạo các bản vẽ chứa các đối tượng trực quan, lưu đồ, sơ đồ UML, luồng thông tin, sơ đồ tổ chức, sơ đồ phần mềm, bố cục mạng, mô hình cơ sở dữ liệu, ánh xạ đối tượng, v.v. thông tin tương tự. Các tệp được tạo bằng Visio cũng có thể được xuất sang các định dạng tệp khác nhau, chẳng hạn như [PNG](/vi/image/png/), [BMP](/vi/image/bmp/), [PDF](/vi/pdf/) và các định dạng khác.

## Định dạng tệp VSDM

Các tệp VSDM dựa trên Quy ước đóng gói mở và XML và các nhà phát triển có thể hưởng lợi từ định dạng này bằng cách tìm hiểu cách làm việc với các tệp này theo chương trình. Định dạng kế thừa nhiều cấu trúc XML giống như các phần của nó từ định dạng tệp Bản vẽ Visio XML (.vdx). Khả năng tương tác với các tệp Visio được tăng lên đáng kể do phần mềm bên thứ ba có thể thao tác với các tệp Visio ở cấp độ định dạng tệp.

Mỗi tệp Visio được gọi là gói chứa các tệp hoặc phần khác. Một phần của gói có thể là một tệp XML, một hình ảnh hoặc thậm chí là một giải pháp VBA. Các phần bên trong gói có thể được chia thành các phần "tài liệu" và "mối quan hệ".

### Tài liệu ###

Các phần tài liệu chứa nội dung và siêu dữ liệu thực tế của tệp Visio, chẳng hạn như tên của tệp, trang đầu tiên và tất cả các hình có trong tệp, thậm chí cả các kết nối dữ liệu cho các hình. Các tệp hình ảnh và văn bản trong gói được coi là các phần tài liệu.

### Các mối quan hệ ###

Các phần mối quan hệ của tệp Visio được lưu trữ trong thư mục "\_rels" và mô tả cách các phần trong gói có liên quan đến từng phần. Nó cũng cung cấp cấu trúc của tập tin. Một tài liệu XML độc lập sử dụng mối quan hệ cha/con của các phần tử để xác định mối quan hệ của các thực thể với nhau. Định dạng tệp Visio 2013 hợp lệ chứa đúng bộ phần và gói chứa mối quan hệ giữa các phần.

Các phần quan hệ là các tài liệu XML mô tả các mối quan hệ giữa các phần tài liệu khác nhau trong gói. Chúng xác định mối liên kết giữa hai mục: một nguồn được chỉ định (được xác định bởi tên và vị trí của tệp mối quan hệ) và một phần tài liệu đích được chỉ định. Ví dụ: các phần quan hệ được sử dụng để mô tả các hình dạng chính được liên kết với tệp, cách các trang liên quan đến tệp và với nhau hoặc cách hình ảnh và đối tượng liên quan đến một trang cụ thể.

## Người giới thiệu ##

* [Giới thiệu về Định dạng tệp Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

