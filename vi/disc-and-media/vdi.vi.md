{
  "date" : "2021-08-11",
  "keywords" :[ "tệp vdi", "định dạng tệp vdi", "tệp vdi là gì", "tệp", "ví dụ vdi", "phần mở rộng tệp vdi","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp VDI và các API có thể tạo và mở tệp VDI.",
  "title" :"VDI - Tệp ảnh đĩa ảo VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Tệp VDI là gì?
Tệp có phần mở rộng .vdi là ảnh đĩa ảo; dành riêng cho chương trình ảo hóa máy tính để bàn mã nguồn mở của Oracle có tên là VirtualBox. Các tệp VDI được sử dụng để khởi động máy ảo VirtualBox. Máy ảo cho phép người dùng chạy các hệ điều hành hoặc chương trình bổ sung trên một máy tính. Do đó, lợi ích của các tệp VDI là người dùng có thể lưu các tệp ảnh đĩa này trên đĩa cứng của họ và có thể chạy chúng bằng trình giả lập bất cứ khi nào họ cần.

## Định dạng tệp VDI
Virtual Disk Image (VDI) là định dạng tệp đĩa chính dành cho máy ảo Oracle nguồn mở, được phát triển tích cực, được gọi là VirtualBox, là một sản phẩm ảo hóa cấp doanh nghiệp. Định dạng tệp VDI được thiết kế để tạo ảnh đĩa di động có thể dễ dàng chạy bằng các chương trình ảo hóa khác. Nó hỗ trợ cả lưu trữ được phân bổ động và kích thước cố định. Nó cho phép bạn mở rộng tệp hình ảnh sau khi nó được tạo, ngay cả khi nó đã chứa dữ liệu.

### Ảo hóa đĩa
Hệ thống giả lập đĩa cứng ở định dạng ảnh đĩa VDI. Máy ảo VirtualBox có thể sử dụng các đĩa trước đó được tạo trong Microsoft Virtual PC hoặc VMware, cũng như định dạng gốc của chính nó. VirtualBox cũng có khả năng kết nối với các mục tiêu iSCSI và phân vùng thô trên máy chủ, sử dụng làm đĩa cứng ảo. VirtualBox mô phỏng IDE (bộ điều khiển PIIX4 và ICH6), SATA (bộ điều khiển ICH8M), bộ điều khiển SAS có thể gắn ổ cứng và SCSI.

Hỗ trợ có sẵn cho Định dạng ảo hóa mở (OVF) kể từ phiên bản 2.2.0 của VirtualBox. Cả thiết bị vật lý được kết nối với máy chủ và hình ảnh ISO đều có thể được gắn dưới dạng ổ đĩa CD hoặc DVD.
Theo mặc định, VirtualBox hỗ trợ đồ họa thông qua card đồ họa ảo tùy chỉnh tương thích VESA.

### Hỗ trợ ảo hóa cho Ethernet
VirtualBox ảo hóa các Thẻ giao diện mạng sau cho bộ điều hợp mạng Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Máy tính để bàn Intel Pro/1000 MT (82540EM)
- Máy chủ Intel Pro/1000 MT (82545EM)
- Máy chủ Intel Pro/1000 T (82543GC)
- Bộ điều hợp mạng ảo hóa (virtio-net)

Các card mạng được mô phỏng cho phép HĐH khách chạy mà không cần tìm kiếm và cài đặt trình điều khiển cho phần cứng mạng vì chúng có sẵn như một phần của HĐH khách. Một bộ điều hợp mạng ảo hóa đặc biệt cải thiện hiệu suất mạng bằng cách cắt giảm nhu cầu khớp với một giao diện phần cứng cụ thể. Do đó, nó đòi hỏi sự hỗ trợ đặc biệt của tài xế trong khách.


## Người giới thiệu

* [VirtualBox - theo Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


