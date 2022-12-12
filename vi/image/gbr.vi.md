{
  "date" : "2019-10-11",
  "keywords" :[ "tệp gbr", "định dạng tệp gbr", "tệp gbr là gì", "tệp", "ví dụ gbr", "phần mở rộng tệp gbr","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp GBR - Định dạng tệp Gerber cho PCB",
  "description":"Tìm hiểu về định dạng tệp GBR và các API có thể tạo và mở tệp GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GBR là gì?

Tệp có phần mở rộng .gbr là định dạng tệp hình ảnh Gerber để trao đổi dữ liệu thiết kế bảng mạch in (PCB). Nó được phát triển bởi Ucamco. Dữ liệu thiết kế PCB là thành phần chính mà ngành công nghiệp chế tạo yêu cầu để xử lý. Tệp GRB chứa dữ liệu PCB như lớp đồng, mặt nạ hàn, chú giải, dữ liệu khoan và định tuyến. Nó có thể được sử dụng để truyền dữ liệu chẳng hạn như các đặc điểm chế tạo PCB bao gồm độ dày hoặc lớp hoàn thiện ở định dạng tiêu chuẩn hóa. Tất cả các hệ thống thiết kế PCB đều xuất các tệp Gerber có thể được xử lý bởi các hệ thống chế tạo PCB. Các tệp GBR hiện đã trở thành tiêu chuẩn thực tế để truyền dữ liệu thiết kế bảng mạch in (PCB). Ucamco đã cung cấp [trình xem trực tuyến miễn phí](https://gerber-viewer.ucamco.com/) để mở và xem các định dạng tệp GBR.

## Định dạng tệp GBR

GBR là định dạng UTF-8 mà con người có thể đọc được, chỉ bao gồm 27 lệnh. Do danh sách lệnh ngắn này và tính nhỏ gọn của nó, GBR rất dễ gỡ lỗi. Cốt lõi của Gerber là một định dạng vector mở cho hình ảnh nhị phân 2D. Thông tin meta được truyền cùng với hình ảnh thông qua Thuộc tính. Một tệp GRB chỉ định một hình ảnh duy nhất và không yêu cầu bất kỳ tệp đi kèm hoặc tham số bên ngoài nào được diễn giải. Một hình ảnh chỉ cần một tệp. Nó sử dụng các ký tự ASCII 7 bit cho tất cả các lệnh và tên được xác định trong thông số kỹ thuật có thể in được. Điều này hoàn toàn bao gồm tạo hình ảnh hoàn chỉnh.

### Tệp GBR Ví dụ

Sau đây là một ví dụ về tệp Gerber tạo một vòng tròn có đường kính 1,5 mm có tâm ở gốc tọa độ. Có một lệnh trên mỗi dòng.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Người giới thiệu

* [Định dạng Gerber](https://www.ucamco.com/en/gerber)

