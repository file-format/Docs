{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","tệp vdw", "định dạng tệp vdw", "loại tệp vdw", "tệp", "loại", "tệp vdw là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Định dạng tệp dịch vụ đồ họa Visio",
  "description":"Tìm hiểu về định dạng tệp VDW và các API có thể tạo và mở tệp VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Tệp VDW là gì?

VDW là định dạng tệp Dịch vụ Đồ họa Visio chỉ định các luồng và kho lưu trữ cần thiết để hiển thị bản vẽ Web. Bản vẽ web là tập hợp các trang bản vẽ, hình dạng, phông chữ, hình ảnh, kết nối dữ liệu và thông tin cập nhật sơ đồ có thể được hiển thị dưới dạng bản vẽ vectơ hoặc raster. Các tệp VDW cũng có thể được mở trong Microsoft Visio nhưng chủ yếu được lưu để sử dụng trên web. Microsoft Visio cung cấp khả năng chuyển đổi các tệp Visio sang một số định dạng tệp khác nhau bao gồm [PNG](/vi/Image/PNG/), [BMP](/vi/Image/BMP/), [PDF](/vi/pdf/) và các định dạng khác.

## Định dạng tệp **VDW**

Thông số kỹ thuật của định dạng tệp VDW có sẵn trực tuyến bởi [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) và nhà phát triển có thể tham khảo để tạo các ứng dụng. Tài liệu kỹ thuật mô tả dữ liệu chứa trong một tệp phức hợp chứa kho lưu trữ và luồng. Có thể biểu diễn Bản vẽ web thông qua một luồng, có tên là VisioServerData, thông qua kho lưu trữ ZIP. Phần ShapGraphic XML trong kho lưu trữ mô tả các yếu tố đồ họa được hiển thị trong bản vẽ Web và được thể hiện bằng Ngôn ngữ đánh dấu ứng dụng mở rộng (XAML). Một bộ sưu tập các phần XML trong kho lưu trữ ZIP mô tả kết nối dữ liệu của bản vẽ Web, thông tin về hình dạng của nó và logic cập nhật sơ đồ. Những phần này được thể hiện dưới dạng XML. Phần DataGraphic XML mô tả các thuộc tính được tính toán lại sẽ được đánh giá sau khi dữ liệu trong bản vẽ Web đã được làm mới từ nguồn dữ liệu. Các mục bổ sung trong kho lưu trữ ZIP chứa thông tin về phông chữ và hình ảnh được sử dụng trong bản vẽ trên Web.

|![Có thể triển khai một tệp](/vi/web/vdw.png "Có thể triển khai một tệp")

## Người giới thiệu

* [[MS-VGSFF]: Định dạng tệp Dịch vụ đồ họa Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

