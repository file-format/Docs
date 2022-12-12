{
  "date" : "2019-10-11",
  "keywords" :[ "tệp png", "định dạng tệp png", "tệp png là gì", "tệp", "ví dụ png", "phần mở rộng tệp png","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PNG - Tệp ảnh raster",
  "description":"Tìm hiểu về định dạng tệp PNG và các API có thể tạo và mở tệp PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PNG là gì?

Tệp **PNG** (Đồ họa mạng di động) là định dạng tệp hình ảnh raster sử dụng nén không mất dữ liệu. Định dạng tệp này được tạo để thay thế Định dạng trao đổi đồ họa ([GIF](/vi/image/gif/)) và không có giới hạn bản quyền. Tuy nhiên, định dạng tệp PNG không hỗ trợ hình ảnh động. Định dạng tệp PNG hỗ trợ nén hình ảnh không mất dữ liệu khiến nó trở nên phổ biến đối với người dùng. Theo thời gian, PNG đã phát triển thành một trong những định dạng tệp hình ảnh được sử dụng rộng rãi.

## Lịch sử tóm tắt về định dạng tệp PNG

Lý do chính đằng sau việc tạo định dạng tệp PNG là thuật toán nén đã được cấp bằng sáng chế, Lempel-Ziv-Welch, được sử dụng trong định dạng tệp GIF. Điều này cùng với các giới hạn GIF khác đã tạo ra nhu cầu thay thế định dạng tệp [**GIF**](/vi/image/gif/). Đề xuất và tên đầu tiên cho định dạng tệp PNG được đưa ra vào tháng 1 năm 1995. Các sự kiện chính liên quan đến định dạng tệp PNG được liệt kê bên dưới:

* Tháng 10 năm 1996: Thông số kỹ thuật PNG Phiên bản 1.0 được phát hành và sau đó xuất hiện dưới dạng [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Điều tương tự đã trở thành Khuyến nghị của W3C vào tháng 10 năm 1996.
* Tháng 12 năm 1998: Phiên bản 1.1, với một số thay đổi nhỏ và bổ sung ba khối mới, được phát hành.
* Tháng 8 năm 1999: Phiên bản 1.2, bổ sung thêm một đoạn, được phát hành.
* Tháng 11/2003: PNG trở thành Tiêu chuẩn quốc tế (ISO/IEC 15948:2003). Phiên bản PNG này chỉ khác một chút so với phiên bản 1.2 và không thêm khối mới.
* Tháng 3 năm 2004: ISO/IEC 15948:2004

## So sánh chức năng của GIF và PNG

Định dạng tệp PNG được thiết kế đơn giản và di động, không bị cản trở về mặt pháp lý, có thể hoán đổi cho nhau, linh hoạt và mạnh mẽ. Bảng sau đây liệt kê các tính năng GIF được kế thừa bởi định dạng tệp PNG bên cạnh các tính năng mới.

|Tính năng|GIF|PNG|
---|---|---|
|Hình ảnh màu chỉ mục lên đến 256 màu|Có|Có|
|Hỗ trợ phát trực tuyến|Có|Có|
|Tính minh bạch|Có|Có|
|Thông tin phụ trợ|Có|Có|
|Độc lập về phần cứng và nền tảng|Có|Có|
|Có hiệu lực|Có|Có|
|Hình ảnh màu trung thực lên đến 48 bit trên mỗi pixel|Không|Có|
|Hình ảnh thang độ xám lên đến 16 bit trên mỗi pixel|Không|Có|
|Kênh alpha đầy đủ (mặt nạ trong suốt chung)|Không|Có|
|Thông tin gamma hình ảnh|Không|Có|
|Độ tin cậy|Không|Có|
|Trình chiếu ban đầu nhanh hơn|Không|Có|

## Cấu trúc tệp PNG

Hầu như tất cả các Hệ điều hành đều có hỗ trợ mở tệp PNG. Ví dụ: trình xem Microsoft Windows có khả năng mở các tệp PNG vì theo mặc định, hệ điều hành có hỗ trợ sẵn có như một phần của quá trình cài đặt. Một tệp PNG bao gồm một `chữ ký` PNG theo sau là một loạt //khối //.

### Tiêu đề tệp PNG

Tám byte đầu tiên của tệp PNG luôn chứa các giá trị (thập phân) sau:

{{{137 80 78 71 13 10 26 10 }}}

Chữ ký này cho biết rằng phần còn lại của tệp chứa một hình ảnh PNG duy nhất, bao gồm một loạt các đoạn bắt đầu bằng một đoạn IHDR và kết thúc bằng một đoạn IEND.

### Miếng, mảnh nhỏ ###

Mỗi đoạn bao gồm bốn phần:

**Độ dài:** Số nguyên không dấu 4 byte cho biết số byte trong trường dữ liệu của đoạn. Độ dài chỉ tính trường dữ liệu, không phải trường dữ liệu, mã loại đoạn hoặc CRC. Zero là một chiều dài hợp lệ. Mặc dù bộ mã hóa và bộ giải mã nên coi độ dài là không dấu, nhưng giá trị của nó không được vượt quá 231 byte.

**Loại đoạn:** Mã loại đoạn 4 byte. Để thuận tiện trong việc mô tả và kiểm tra các tệp PNG, mã loại được hạn chế bao gồm các chữ cái ASCII viết hoa và viết thường (AZ và az, hoặc 65-90 và 97-122 thập phân). Tuy nhiên, bộ mã hóa và giải mã phải coi mã là giá trị nhị phân cố định, không phải chuỗi ký tự. Ví dụ: sẽ không đúng nếu biểu thị mã loại IDAT bằng các chữ cái tương đương EBCDIC của các chữ cái đó. Các quy ước đặt tên bổ sung cho các loại chunk sẽ được thảo luận trong phần tiếp theo.

**Dữ liệu đoạn dữ liệu:** Các byte dữ liệu phù hợp với loại đoạn dữ liệu, nếu có. Trường này có thể có độ dài bằng không.

**CRC:** CRC 4 byte (Kiểm tra dự phòng theo chu kỳ) được tính trên các byte trước đó trong đoạn, bao gồm mã loại đoạn và trường dữ liệu đoạn, nhưng không bao gồm trường độ dài. CRC luôn hiện diện, ngay cả đối với các khối không chứa dữ liệu.

Độ dài dữ liệu chunk có thể là bất kỳ số byte nào cho đến mức tối đa; do đó, những người triển khai không thể cho rằng các khối được căn chỉnh trên bất kỳ ranh giới nào lớn hơn byte.

Các khối có thể xuất hiện theo bất kỳ thứ tự nào, tùy thuộc vào các hạn chế được đặt trên từng loại khối. (Một hạn chế đáng chú ý là IHDR phải xuất hiện trước và IEND phải xuất hiện sau cùng; do đó, đoạn IEND đóng vai trò là điểm đánh dấu cuối tệp.) Nhiều đoạn cùng loại có thể xuất hiện, nhưng chỉ khi được phép cụ thể cho loại đó.

#### Các loại khối

Loại Chunk được phân loại thành các chunk **Critical** và **Ancillary** dựa trên giá trị ASCII 4 byte phân biệt chữ hoa chữ thường được gán cho Loại Chunk. Tất cả các triển khai phải hiểu và kết xuất thành công các khối quan trọng tiêu chuẩn. Một hình ảnh PNG hợp lệ phải chứa một đoạn IHDR, một hoặc nhiều đoạn IDAT và một đoạn IEND.

### Nén

Phương pháp nén PNG 0 (phương pháp nén duy nhất hiện được xác định cho PNG) chỉ định nén giảm phát/tăng cường với cửa sổ trượt tối đa 32768 byte. Nén giảm tốc là một dẫn xuất LZ77 được sử dụng trong zip, gzip, pkzip và các chương trình liên quan. Nghiên cứu sâu rộng đã được thực hiện để hỗ trợ tình trạng không có bằng sáng chế của nó. Dữ liệu nén trong luồng dữ liệu zlib được lưu trữ dưới dạng một chuỗi khối, mỗi khối có thể biểu thị dữ liệu thô (không nén), dữ liệu nén LZ77 được mã hóa bằng mã Huffman cố định hoặc dữ liệu nén LZ77 được mã hóa bằng mã Huffman tùy chỉnh. Một bit đánh dấu trong khối cuối cùng xác định nó là khối cuối cùng, cho phép bộ giải mã nhận ra phần cuối của luồng dữ liệu nén.

#### Lọc trước khi nén

Các bộ lọc trước khi nén được áp dụng để chuẩn bị dữ liệu hình ảnh cho quá trình nén tối ưu. Phương pháp bộ lọc PNG xác định năm loại bộ lọc cơ bản như sau:

|Loại bộ lọc|Tên|Giá trị dự đoán|
---|---|---|
|0|Không có|Dòng quét được truyền không sửa đổi|
|1|Sub|Truyền sự khác biệt giữa mỗi byte và giá trị của byte tương ứng của pixel trước đó.|
|2|Up|Bộ lọc Up() giống như bộ lọc Sub() ngoại trừ pixel ngay phía trên pixel hiện tại, thay vì chỉ ở bên trái của nó, được sử dụng làm công cụ dự đoán.|
|3|Trung bình|Bộ lọc Trung bình() sử dụng giá trị trung bình của hai pixel lân cận (bên trái và bên trên) để dự đoán giá trị của một pixel.|
|4|Paeth|Bộ lọc Paeth() tính toán một hàm tuyến tính đơn giản của ba pixel lân cận (trái, trên, trên bên trái), sau đó chọn làm công cụ dự đoán pixel lân cận gần nhất với giá trị được tính toán.|

Các thuật toán lọc được áp dụng cho `byte`, không phải cho pixel, bất kể độ sâu bit hoặc loại màu của hình ảnh. Các thuật toán lọc hoạt động trên chuỗi byte được hình thành bởi một đường quét. Nếu hình ảnh bao gồm một kênh alpha, thì dữ liệu alpha được lọc theo cách giống như dữ liệu hình ảnh.

Khi hình ảnh được xen kẽ, mỗi lần vượt qua mẫu xen kẽ được coi là một hình ảnh độc lập cho mục đích lọc. Các bộ lọc hoạt động trên các chuỗi byte được hình thành bởi các pixel thực sự được truyền trong một lần truyền và "đường quét trước đó" là đường được truyền trước đó trong cùng một lần truyền, không phải đường liền kề trong hình ảnh hoàn chỉnh. Lưu ý rằng ảnh con được truyền trong bất kỳ một lần truyền nào luôn là hình chữ nhật, nhưng có chiều rộng và/hoặc chiều cao nhỏ hơn ảnh hoàn chỉnh. Quá trình lọc không được áp dụng khi ảnh con này trống.

## Người giới thiệu ##

* [PNG - Trang chủ](http://www.libpng.org/pub/png/)

