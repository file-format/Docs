{
  "date" : "2021-01-21",
  "keywords" :[ "tệp ai", "định dạng tệp ai", "tệp ai là gì", "tệp", "ví dụ ai", "phần mở rộng tệp ai","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Tệp tác phẩm nghệ thuật Adobe Illustrator",
  "description":"Tìm hiểu về định dạng tệp AI và các API có thể tạo và mở tệp AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Tệp AI là gì?

Tệp có phần mở rộng .ai là tệp Tác phẩm nghệ thuật Adobe Illustrator chứa đồ họa vector trong một trang. nó sử dụng các điểm để tạo đường dẫn hiển thị dữ liệu hình ảnh, do đó đảm bảo an toàn không bị giảm chất lượng hình ảnh nếu nó được phóng to. Định dạng tệp AI dựa trên định dạng tệp PGF tương tự như tệp AI. Định dạng AI được sử dụng chủ yếu cho logo và phương tiện in, đồng thời các phiên bản ban đầu của nó được coi là tương tự như phiên bản của tệp [EPS](/vi/page-description-language/eps/). Các tệp AI có thể được mở bằng các công cụ Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro và CorelDraw Graphics.

## Định dạng tệp AI

AI là định dạng tệp độc quyền của Adobe Illustrator và sử dụng cách tiếp cận đường dẫn kép tương tự như PGF để lưu các tệp tương thích với EPS. [Thông số kỹ thuật định dạng tệp Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) cung cấp thông tin chi tiết tài liệu tham khảo của nhà phát triển để biết chi tiết nội bộ của định dạng tệp này. Tất cả các tài liệu (tệp) do Adobe Illustrator tạo đều là tài liệu ngôn ngữ PostScript và có hai phần chính tuân theo Quy ước cấu trúc tài liệu: `prolog` và `script`.

### Lời mở đầu

Phần prolog gói gọn thông tin cần thiết để giải thích tệp. Một ví dụ sẽ là hộp giới hạn chứa tất cả các dấu trên trang. Nó cũng chứa thông tin tài nguyên như phông chữ và định nghĩa thủ tục. Các tài nguyên này được nhóm hợp lý thành các bộ được gọi là procset và chứa các phương thức rõ ràng để khởi tạo và kết thúc các thủ tục của chúng.

### Script

Các yếu tố đồ họa trên trang được mô tả bằng tập lệnh. Một tập lệnh chứa các tham chiếu đến các toán tử và thủ tục trong prolog, cùng với các toán hạng và dữ liệu. Ba phần hợp lý của một kịch bản bao gồm:

* Trình tự thiết lập - khởi tạo và kích hoạt các tài nguyên được xác định trong prolog
* Trình tự các toán tử mô tả
* Đoạn giới thiệu tắt tài nguyên

Các toán tử trong tập lệnh là chuỗi các thành phần đồ họa được viết bằng ngôn ngữ được xác định bởi các procset trong prolog. Các trình tự này bao gồm các tập hợp các phần tử dữ liệu, các định nghĩa thuộc tính đồ họa và các cuộc gọi đến các thủ tục được xác định trong các procset.

### Thẻ đối tượng

Thẻ đối tượng được sử dụng để đính kèm thông tin tùy chỉnh vào đối tượng nghệ thuật Adobe Illustrator. Các thẻ bao gồm:

* Định danh thẻ
* Loại thẻ
* Dữ liệu

## Người giới thiệu
* [Thông số kỹ thuật định dạng tệp Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Định dạng tệp AI của PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

