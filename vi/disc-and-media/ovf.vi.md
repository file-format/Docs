{
  "date" : "2021-08-10",
  "keywords" :[ "tệp .ovf", "định dạng tệp", "tệp .ovf là gì", "tệp", "phần mở rộng tệp"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp .ovf là gì và các API có thể tạo và mở tệp OVF.",
  "title" :"Định dạng tệp OVF - Mở tệp ảo hóa",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Tệp OVF là gì?

Tệp OVF là tệp văn bản chứa thông tin về việc đóng gói và phân phối phần mềm chạy trên máy ảo. Nó được định dạng theo [Thông số kỹ thuật tiêu chuẩn ảo hóa mở](https://www.dmtf.org/standards/ovf) mô tả tất cả các yêu cầu (chẳng hạn như bảo mật, tính di động, hiệu quả và khả năng mở rộng) để chạy các ứng dụng trên máy ảo. Tổ chức Tiêu chuẩn hóa Quốc tế (ISO) đã thông qua OVF làm tiêu chuẩn ISO 17203.

## Lịch sử tóm tắt về định dạng tệp OVF

Định dạng tệp OVF được giới thiệu bởi DMTF (Lực lượng đặc nhiệm quản lý phân tán) tạo ra các tiêu chuẩn về khả năng quản lý mở. Nó độc lập với bất kỳ cấu trúc bộ hướng dẫn hoặc trình ảo hóa cụ thể nào. Gói OVF chứa một hoặc nhiều hệ thống ảo, mỗi hệ thống có thể được triển khai cho một máy ảo.

## Định dạng tệp OVF - Thông tin khác

Một gói OVF bao gồm nhiều tệp được đặt trong một thư mục. Trong số này, nó chứa chính xác một tệp mô tả OVF (có phần mở rộng .ovf) được lưu trữ ở định dạng tệp [XML](/vi/web/xml/). Nó mô tả thông tin máy ảo được đóng gói và thông tin siêu dữ liệu về gói OVF, chẳng hạn như:

* Tên
* yêu cầu phần cứng
* tham chiếu đến các tệp khác trong gói OVF và
* mô tả con người có thể đọc được

Các tệp khác có thể được tìm thấy trong gói OVF bao gồm một hoặc nhiều ảnh đĩa và các tệp chứng chỉ tùy chọn và các tệp phụ trợ khác.

## Người giới thiệu

* [Định dạng ảo hóa mở - DMTF](https://www.dmtf.org/standards/ovf)
* [Thông số định dạng tệp OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

