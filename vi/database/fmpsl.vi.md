{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp FMPSL và API có thể tạo và mở tệp FMPSL.",
  "title" :"Định dạng tệp FMPSL - Tệp liên kết ảnh chụp nhanh FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Tệp FMPSL là gì?

Tệp FMPSL là tệp ảnh chụp nhanh của cơ sở dữ liệu được tạo bằng FileMaker Pro 12. Tệp này lưu trữ kết quả được truy vấn từ cơ sở dữ liệu cùng với các thông tin khác, chẳng hạn như bố cục trực quan và thông tin hiển thị. Tệp FMPSL có thể được sử dụng để khôi phục tất cả dữ liệu này trong một phiên bản khác của cơ sở dữ liệu FileMaker Pro. Định dạng tệp này được giới thiệu cùng với sự ra mắt của FileMaker Pro v 12. Trước phiên bản này, các liên kết ảnh chụp nhanh được giới thiệu dưới dạng định dạng tệp FPSL trong FileMaker Pro v 11. Có thể mở các tệp FMPSL bằng phần mềm FileMaker Pro Advanced. Các định dạng tệp khác được FileMaker Pro hỗ trợ bao gồm [FP5](/vi/database/fp5/), [FP7](/vi/database/fp7/) và [FMP12](/vi/database/fmp12/).

## Định dạng tệp FMPSL

Chi tiết định dạng tệp nội bộ của tệp FMPSL không có sẵn công khai để nhà phát triển tham khảo.

### Làm cách nào để Lưu Bản ghi dưới dạng tệp FMPSL?

Dữ liệu từ cơ sở dữ liệu FileMaker Pro có thể được lưu dưới dạng tệp liên kết chụp nhanh bằng các bước sau.

1. Tìm kiếm các bản ghi từ cơ sở dữ liệu được yêu cầu lưu dưới dạng tệp liên kết chụp nhanh.
1. Sử dụng tùy chọn Send Record As Snapshot Link từ menu, lưu tệp bằng cách nhập tên tệp.
1. Sử dụng các Bản ghi đang được duyệt để lưu toàn bộ bộ bản ghi đã tìm được.

Tệp ảnh chụp nhanh được tạo sẽ được lưu vào đĩa với tên được chỉ định.

## Người giới thiệu

* [Chuyển đổi các phiên bản cũ hơn của định dạng tệp FileMaker Pro sang định dạng tệp FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Lưu bản ghi dưới dạng tệp liên kết chụp nhanh](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

