{
  "date" : "2019-10-11",
  "keywords" :[ "tệp wmf", "định dạng tệp wmf", "tệp wmf là gì", "tệp", "ví dụ wmf", "phần mở rộng tệp wmf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Định dạng siêu tệp Microsoft Windows",
  "description":"Tìm hiểu về định dạng tệp WMF và các API có thể tạo và mở tệp WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp WMF là gì?

Các tệp có phần mở rộng WMF đại diện cho Siêu tệp Microsoft Windows (WMF) để lưu trữ dữ liệu hình ảnh định dạng vectơ cũng như bitmap. Nói chính xác hơn, WMF thuộc danh mục định dạng tệp vectơ của các định dạng tệp Đồ họa độc lập với thiết bị. Giao diện thiết bị đồ họa Windows (GDI) sử dụng các chức năng được lưu trữ trong tệp WMF để hiển thị hình ảnh trên màn hình. Một phiên bản nâng cao hơn của WMF, được gọi là Tệp Meta nâng cao (EMF), đã được xuất bản sau đó làm cho định dạng này có nhiều tính năng phong phú hơn. Thực tế, WMF tương tự như SVG.

## Thông số kỹ thuật định dạng tệp WMF ##

Tệp WMF được gọi là định dạng tệp 16 bit tại thời điểm khởi chạy với Windows 3.0. Định dạng tệp bao gồm một loạt các bản ghi có độ dài thay đổi chứa các lệnh vẽ đồ họa, định nghĩa đối tượng và thuộc tính. Vì các tệp WMF dựa trên các lệnh được hiển thị cho GDI để vẽ hình ảnh, nên nó còn được gọi là bản ghi kỹ thuật số của hình ảnh có thể được phát lại để tái tạo hình ảnh đó. Thông số kỹ thuật định dạng tệp hoàn chỉnh của WMF có sẵn trực tuyến và nên được giới thiệu để phát triển các ứng dụng hoạt động với tệp WMF. Tệp WMF được tổ chức thành:

* Bản ghi tiêu đề WMF
* (Các) Bản ghi WMF
* Bản ghi cuối tập tin WMF

### Bản ghi tiêu đề WMF ###

**Bản ghi META_HEADER** chứa thông tin xác định các đặc điểm của siêu tệp, bao gồm:

* Loại siêu tệp
* Phiên bản của siêu tệp
* Kích thước của siêu tệp
* Số lượng đối tượng được xác định trong siêu tệp
* Kích thước của bản ghi lớn nhất trong siêu tệp

### Bản ghi tiêu đề có thể đặt WMF ###

**Bản ghi META_PLACEABLE** chứa thông tin mở rộng liên quan đến hình ảnh, bao gồm:

* Một hình chữ nhật giới hạn
* Kích thước đơn vị logic, để chia tỷ lệ
* Tổng kiểm tra, để xác nhận

### Bản ghi WMF ###

Bản ghi WMF có định dạng chung, được chỉ định trong tài liệu thông số kỹ thuật. Mỗi bản ghi WMF chứa các thông tin sau:

* Kích thước kỷ lục
* Chức năng ghi
* Tham số, nếu có, cho chức năng ghi

## Người giới thiệu ##

* [[MS-WMF]: Định dạng siêu tệp Windows](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Siêu tệp Windows - Wikipedia](https://vi.wikipedia.org/wiki/Windows_Metafile)

