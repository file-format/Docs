{
  "date" : "2019-10-11",
  "keywords" :[ "tệp j2c", "định dạng tệp j2c", "tệp j2c là gì", "tệp", "ví dụ j2c", "phần mở rộng tệp j2c","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Tìm hiểu về định dạng tệp J2C và API có thể tạo và mở tệp J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Tệp J2C là gì?

Tệp có phần mở rộng .j2c là một biến thể của định dạng tệp JPEG và được nén bằng phương pháp nén wavelet. Nó có hệ thống đánh dấu và phân đoạn gần giống với định dạng tệp JPEG 2000. Định dạng tệp J2C như được xác định trong Phần 1 của giá đỡ JPEG 2000 hỗ trợ cả nén mất dữ liệu và nén không mất dữ liệu. Dòng mã JPEG 2000 được thiết kế để nhúng trong [JP2](/vi/image/jp2/) hoặc định dạng tệp khác, mặc dù nó có thể xuất hiện trong một tệp riêng lẻ. Có thể mở tệp J2C bằng Adobe Photoshop 2020, Adobe Illustrator 2020 và Corel Paintshop Pro.

## Định dạng tệp J2C

Định dạng tệp J2C giống với định dạng của JPEG 2000 thường được lưu dưới dạng .jp2 và .jpc. Điều này làm cho các tệp J2C tuân theo cùng một phương pháp mã hóa siêu dữ liệu ở định dạng XML trong đó Tiêu chuẩn 12234-1 được sử dụng làm tham chiếu giữa các thẻ Exif và các thành phần XML. Nó được cải thiện hơn nữa bởi phần mở rộng JPEG 2000 phần 2 kết hợp cơ chế hoạt hình và cấu hình luồng mã thành một hình ảnh duy nhất. Các tệp định dạng tệp mở rộng như vậy được lưu dưới dạng [.jpx](/vi/image/jpx/).

### Bố cục của Tệp JPEG2000

JPEG2000 hỗ trợ nhiều ứng dụng khác nhau dựa trên sự tuân thủ đối với các định dạng tệp có thể mở rộng. Mặc dù loại đơn giản nhất có thể chứa một hình ảnh duy nhất, nhưng các loại phức tạp hơn có thể bao gồm một loạt hình ảnh, xếp chồng lên nhau hoặc được sắp xếp theo trình tự thời gian.

#### Hộp JP2
Đây là khối xây dựng cấp cao nhất của định dạng tệp JP2 và chứa các trường loại và độ dài trong tiêu đề và một phần dữ liệu. Loại hộp đáng chú ý nhất là hộp dòng mã liền kề. Hộp này lưu trữ dòng mã JPEG2000 trong phần dữ liệu của nó.

#### Dòng mã JPEG2000

JPEG2000 CodeStream là một chuỗi byte cần thiết để giải mã hình ảnh nén JPEG2000. Trong trường hợp tệp không có gì khác ngoài dòng mã này, nó được gọi là tệp dòng mã thô. Thông thường, dòng mã JPEG là ứng dụng của thuật toán nén JPEG2000 trên một hình ảnh, mặc dù đó không phải là cách duy nhất.

#### Bộ phận ngói ####

Hình ảnh được mã hóa JPEG2000 là tập hợp các đơn vị dữ liệu được gọi là gói. Các gói này được duy trì trong dòng mã bên trong các nhóm gói được gọi là phần khối ảnh. Trước khi mã hóa một hình ảnh, bộ mã hóa chia hình ảnh thành một lưới các khối hình chữ nhật, được gọi là các ô trong đó mỗi ô được mã hóa riêng biệt bất kể các ô khác.

{{< figure src="../JPEG2000_Codestream.png" alt="Định dạng tệp JPEG2000" >}}

## Nén J2C
JPEG 2000 sử dụng công nghệ nén sóng con làm cho nó nhanh dựa trên thực tế là tương đối ít điểm ảnh được hiển thị trong bất kỳ cổng xem hoặc cửa sổ nào mà trình xem hiển thị hình ảnh. Điều này có thể được nhấn mạnh bởi thực tế là chỉ một vài megabyte pixel sẽ xuất hiện trên màn hình đối với những hình ảnh có kích thước rất lớn (tính bằng gigabyte). Điều này giúp nhanh chóng tìm nạp và chỉ hiển thị phần dữ liệu hình ảnh cần thiết để điền vào các pixel hiển thị. Điều này cũng đòi hỏi công nghệ giải nén tốc độ cao để tăng tốc cơ chế tìm nạp hình ảnh nhằm tạo ra hình ảnh cần thiết một cách nhanh chóng.

J2C tận dụng khả năng giải nén nhanh và chỉ tìm nạp thông tin cần thiết cho dữ liệu pixel để nhanh chóng hiển thị một phần hình ảnh hiển thị trên màn hình. J2C được thiết kế chủ yếu để xem dữ liệu và không chỉnh sửa dữ liệu.

## Nhận dạng J2C
Các tệp JPEG 2000 có byte chữ ký `FF 4F FF 51`.

### Các loại kịch câm
Các loại Mime đã đăng ký cho các tệp JPEG 2000 bao gồm:
* hình ảnh/j2c
* hình ảnh/jpx
* hình ảnh/jpm
* video/mj2

## Những cải tiến so với tiêu chuẩn JPEG
Những cải tiến so với tiêu chuẩn JPEG bao gồm:
* Hiệu suất nén vượt trội
* Đại diện nhiều độ phân giải
* Truyền lũy tiến theo pixel và độ chính xác của độ phân giải
* Lựa chọn nén không mất dữ liệu hoặc mất dữ liệu
* Khả năng phục hồi lỗi, Định dạng tệp linh hoạt
* Hỗ trợ dải động cao
* Thông tin không gian kênh bên

## Người giới thiệu ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

