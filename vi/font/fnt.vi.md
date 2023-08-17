{
  "date" : "2020-08-20",
  "keywords" :[ "tệp fnt", "định dạng tệp fnt", "tệp fnt là gì", "tệp", "ví dụ fnt", "phần mở rộng tệp fnt","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Tệp phông chữ Windows",
  "description":"Tìm hiểu về định dạng tệp FNT và các API có thể tạo và mở tệp FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Tệp FNT là gì?

Tệp có phần mở rộng .fnt là tệp phông chữ lưu trữ thông tin phông chữ chung trên Hệ điều hành Windows. Các tệp FNT hầu hết đã được thay thế bằng các định dạng tệp TrueType (.TTF) và OpenType (.OTF) và hiện tại là định dạng tệp phông chữ lỗi thời. Các tệp này có thể lưu trữ một phông chữ vectơ hoặc trình đánh giá duy nhất. Tất cả trình điều khiển thiết bị đều hỗ trợ phông chữ Windows 2.x. Tuy nhiên, không phải tất cả trình điều khiển thiết bị
hỗ trợ phiên bản Windows 3.0.

## Định dạng tệp FNT

Các tệp FNT có khả năng lưu trữ một phông chữ raster hoặc vector. Các định dạng véc-tơ được GDI sử dụng thường xuyên hơn so với raster trong đó mỗi biểu tượng của điều lệ được xác định bằng cách sử dụng một bitmap nhỏ. Lý do rõ ràng cho việc thay thế .fnt bằng .ttf và .otf là định dạng raster của nó.

### Tiêu đề tệp phông chữ
Phần đầu của cả tệp phông chữ raster và vectơ là phổ biến, theo sau là thông tin khác nhau cho từng loại tệp. Tiêu đề tệp phông chữ bao gồm cho Windows 3.0 bao gồm sáu trường mới như sau được đặt thành 0 để đảm bảo khả năng tương thích với các phiên bản Windows trong tương lai.

* dFlags
* dfAspace
* dfBspace
* không gian dfC
* con trỏ dfColor
* dfReserve1

Để biết thông tin chi tiết về các tiêu đề dành cho Windows 3.0 và 2.0, hãy truy cập [Kho lưu trữ Cơ sở Kiến thức của Microsoft](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Người giới thiệu
* [Định dạng tệp phông chữ](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Cách cài đặt hoặc xóa phông chữ trong Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

