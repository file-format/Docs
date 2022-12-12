{
  "date" : "2021-04-08",
  "keywords" :[ "tệp deb", "định dạng tệp deb", "tệp deb là gì", "tệp", "ví dụ deb", "phần mở rộng tệp deb","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Lưu trữ tar nén Bzip",
  "description":"Tìm hiểu về định dạng tệp DEB và API có thể tạo và mở tệp DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Tệp DEB là gì?

Tệp có phần mở rộng .deb là định dạng tệp gói nhị phân Debian có sẵn để phân phối các gói phần mềm trên HĐH Linux. Nó bao gồm hai tệp lưu trữ [TAR](/vi/compression/tar/). DPKG cung cấp cơ chế để đọc và cài đặt các gói DEB. Các gói DEB có thể được cài đặt bằng giao diện quản lý phần mềm gói APT. Các tệp DEB có Loại phương tiện Internet là `application/vnd.debian.binary-package`.

## Định dạng tệp DEB

Tệp DEB bao gồm hai tệp lưu trữ [TAR](/vi/compression/tar/). Một kho lưu trữ chứa thông tin điều khiển và một kho lưu trữ khác chứa dữ liệu có thể cài đặt.

### Tổ chức trọn gói

Tệp DEB là tệp lưu trữ **ar** có giá trị kỳ diệu là `!<arch> `. Kể từ Debian 0.93, cơ chế lưu trữ các tệp DEB chứa ba tệp theo một thứ tự cụ thể.

1. `Debian Binary` - Nó có một loạt các dòng, được phân tách bằng các dòng mới. Hiện tại, chỉ có một dòng mô tả số phiên bản. Số phiên bản hiện tại là 2.0.
1. `Kho lưu trữ điều khiển` - Nó chứa kho lưu trữ control.tar có tập lệnh bảo trì và siêu thông tin về gói như tên gói, phiên bản, phụ thuộc và người bảo trì.
1. `Lưu trữ dữ liệu` - Đây là kho lưu trữ tar có tên data.tar và chứa các tệp phương tiện có thể cài đặt thực tế. Kho lưu trữ có thể được nén bằng gz, bz2, lzma hoặc xz và phần mở rộng tệp của kho lưu trữ dữ liệu sẽ thay đổi tương ứng.

### Lưu trữ Điều khiển

Kho lưu trữ kiểm soát có thể bao gồm các nội dung như sau.

* `control` - Nó chứa một mô tả ngắn gọn về gói cũng như các thông tin khác chẳng hạn như các thành phần phụ thuộc của nó.
* `md5sums` - Nó chứa tổng kiểm tra MD5 của tất cả các tệp trong gói để phát hiện các tệp bị hỏng hoặc không đầy đủ.
* `conffiles` - Nó liệt kê các tệp của gói sẽ được coi là tệp cấu hình. Các tệp cấu hình không bị ghi đè trong quá trình cập nhật trừ khi được chỉ định.
* `preinst`, postinst, prerm và postrm - Các tập lệnh tùy chọn được thực thi trước hoặc sau khi cài đặt hoặc gỡ bỏ gói
* `config` là tập lệnh tùy chọn hỗ trợ cơ chế cấu hình debconf.
* `shlibs` - Đây là danh sách các thư viện phụ thuộc được chia sẻ.

## Người giới thiệu

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Định dạng gói nhị phân Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

