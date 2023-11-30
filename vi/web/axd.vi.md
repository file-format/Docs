{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp AXD - Định dạng tệp xử lý web ASP.NET",
  "description" :"Tìm hiểu về tệp AXD và các API có thể tạo và mở tệp AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Một tập tin AXD là gì?

Tệp AXD là tệp cài đặt web được sử dụng để xử lý và truy xuất các yêu cầu tài nguyên được nhúng trong ASP.NET. Nó bao gồm các hướng dẫn để truy xuất các tài nguyên được nhúng như hình ảnh, tệp JavaScript ([.JS](/vi/web/js/)) và tệp [.CSS](/vi/web/css/). Các tệp AXD được sử dụng để đưa tài nguyên vào các trang phía máy khách. Điều này cho phép các trang khách truy cập các tài nguyên này trên máy chủ theo cách tiêu chuẩn.

## Định dạng tệp AXD

Các tệp AXD được lưu trữ dưới dạng tệp nhị phân ở phía máy chủ. Nó đề cập đến tệp Trình xử lý web trong ASP.NET là các thành phần tạo ra phản hồi cho các yêu cầu cụ thể tới máy chủ web. Các tệp AXD thực hiện xử lý tùy chỉnh trước khi tạo phản hồi dựa trên yêu cầu trang phía máy khách. Chúng thường được lưu dưới dạng tệp **WebResource.axd**.

### Tệp WebResource.axd là gì?

Hầu hết các dự án ASP.NET đều lưu các tệp AXD dưới dạng tệp WebResource.axd cho phép các trang phía máy khách tải xuống các tài nguyên được nhúng trong một tập hợp. Ứng dụng của bạn có thể phải đối mặt với hiệu suất chậm trong trường hợp bạn chạy nó ở chế độ gỡ lỗi vì trình xử lý WebResources.axd không được lưu vào bộ đệm.

## Người giới thiệu

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

