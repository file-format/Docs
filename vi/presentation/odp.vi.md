{
  "date" : "2019-10-11",
  "keywords" :[ "tệp odp", "định dạng tệp odp", "tệp odp là gì", "tệp", "ví dụ odp", "phần mở rộng tệp odp","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Định dạng tệp bản trình bày OpenOffice",
  "description":"Tìm hiểu về định dạng tệp ODP và API có thể tạo và mở tệp ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp ODP là gì?

Các tệp có phần mở rộng .odp đại diện cho định dạng tệp bản trình bày được OpenOffice.org sử dụng trong tiêu chuẩn OASISOpen. Tệp bản trình bày là một tập hợp các trang chiếu trong đó mỗi trang chiếu có thể bao gồm văn bản, hình ảnh, định dạng, hoạt ảnh và phương tiện khác. Các trang trình bày này được trình bày cho khán giả dưới dạng trình chiếu với cài đặt bản trình bày tùy chỉnh. Các tệp ODP có thể được mở bằng các ứng dụng phù hợp với định dạng OpenDocument (chẳng hạn như OpenOffice hoặc StarOffice).

## Tóm tắt lịch sử

Thông số kỹ thuật định dạng tệp ODP dựa trên tiêu chuẩn được phát triển dưới dạng thông số kỹ thuật ODF. Các thông số kỹ thuật này đã phát triển trong quá khứ dưới dạng ba phiên bản do OASIS phát triển và xuất bản như sau:

`2005` - Phiên bản 1.0 được xuất bản vào tháng 5 năm 2005
`2007` - Phiên bản 1.1 được xuất bản vào tháng 2 năm 2007
`2011` - Phiên bản 1.2 được xuất bản vào tháng 9 năm 2011

Có những thay đổi khá nhỏ trong quá trình chuyển đổi từ phiên bản ODF 1.0 sang 1.1. [Phiên bản ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) là phiên bản mới nhất dành cho các thông số kỹ thuật của ODF và nên được các nhà phát triển tham khảo để phát triển các ứng dụng liên quan đến việc đọc/ghi ODS.

## Thông số kỹ thuật định dạng tệp

Định dạng OpenDocument hỗ trợ biểu diễn tài liệu dưới dạng một tài liệu XML duy nhất cũng như tập hợp một số tài liệu phụ trong một gói dưới dạng kho lưu trữ [ZIP](https://docs.fileformat.com/Compression/ZIP/). Mỗi tệp từ kho lưu trữ ZIP lưu trữ một phần của tài liệu hoàn chỉnh. Mỗi tài liệu con lưu trữ một khía cạnh cụ thể của tài liệu. Ví dụ: một tài liệu con chứa thông tin về kiểu dáng và một tài liệu con khác chứa nội dung của tài liệu. Một tài liệu ODF điển hình có các thành phần sau:

* `content.xml` – Nội dung tài liệu và kiểu tự động được sử dụng trong nội dung.
* `styles.xml` – Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
* `meta.xml` – Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
* `settings.xml` – Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

Bên cạnh những thứ này, trong gói có thể có nhiều tài liệu phụ khác như hình thu nhỏ của tài liệu, hình ảnh, v.v.

Các tệp tài liệu bảng tính là tập hợp con của các tệp ODF nơi nội dung (trang tính) được lưu trữ trong tài liệu con content.xml.

## Người giới thiệu

* [OpenDocument - Bởi Wikipedia](https://vi.wikipedia.org/wiki/OpenDocument)

