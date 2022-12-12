{
  "date" : "2021-04-08",
  "keywords" :[ "tệp rpm", "định dạng tệp rpm", "tệp rpm là gì", "tệp", "ví dụ rpm", "phần mở rộng tệp rpm","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Tệp trình quản lý gói Red Hat",
  "description":"Tìm hiểu về định dạng tệp RPM và các API có thể tạo và mở tệp RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Tệp RPM là gì?

Tệp có phần mở rộng .rpm là gói hệ điều hành Red Hat Linux để cài đặt các chương trình trên hệ thống Linux. Trình quản lý gói Red Hat sử dụng định dạng tệp RPM và là hệ thống quản lý gói nguồn mở và miễn phí. Mặc dù các tệp RPM có thể được sử dụng để cài đặt chương trình, nhưng chúng có thể được chuyển đổi sang các định dạng gói khác, chẳng hạn như [DEB](/vi/compression/deb/) bằng chương trình Debian có tên là Alien.

## Định dạng tệp RPM

Tệp RPM là tệp nhị phân có thể chứa một tập hợp tệp. Hầu hết các tệp RPM là "RPM nhị phân" là tệp thực thi được biên dịch của phần mềm. Tệp RPM có thể chứa các RPM nguồn (SRPM) có thể được sử dụng để xây dựng gói từ mã nguồn. Định dạng tệp RPM bao gồm bốn phần.

* Chì - Nó xác định tệp là tệp RPM
* Chữ ký - Nó có thể được sử dụng để đảm bảo tính toàn vẹn và/hoặc tính xác thực
* Header - Chứa siêu dữ liệu bao gồm tên gói, phiên bản, kiến trúc, danh sách tệp, v.v.
* Lưu trữ tệp - Còn được gọi là tải trọng, thường ở định dạng cpio, được nén bằng [GZIP](/vi/compression/gz/)

## Người giới thiệu

* [RPM - Wikipedia](https://rpm.org)
* [Tài liệu RPM](https://rpm.org/documentation.html)

