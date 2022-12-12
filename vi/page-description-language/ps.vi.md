{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PS",
  "description":"Tìm hiểu về định dạng tệp PS và các API có thể tạo và mở tệp PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp .PS là gì? ##

PostScript (PS) là ngôn ngữ mô tả trang có mục đích chung được sử dụng trong kinh doanh xuất bản điện tử và máy tính để bàn. Trọng tâm chính của PostScript (PS) là tạo thuận lợi cho thiết kế đồ họa hai chiều. Hầu hết các ngôn ngữ yêu cầu một giai đoạn biên dịch riêng biệt trước khi thực thi mã trong khi định dạng Post Script (PS) hỗ trợ diễn giải trực tiếp trong thời gian chạy. Phiên bản đầu tiên của nó xác định các hình dạng đồ họa, các dạng văn bản khác nhau và hình ảnh được mô hình hóa trên các trang in hoặc các trang được hiển thị, tuân theo các quy tắc của mô hình hình ảnh Adobe. Một chương trình của PS có thể liên lạc mô tả tài liệu giữa một thành phần và hệ thống in giữ cho thiết bị độc lập và ở mức cao. Ngoài ra, chương trình này cũng có khả năng quản lý sự xuất hiện của văn bản và đồ họa trên màn hình.

Mô tả trang PostScript có sẵn để được kết xuất, hiển thị trên máy in và thiết bị đầu ra khác với sự trợ giúp của trình thông dịch PostScript của thiết bị. Khi các lệnh in ký tự, hình dạng đồ họa và hình ảnh được thực thi bởi trình thông dịch, đối với thiết bị cụ thể đó, mô tả PostScript cấp cao sẽ chuyển đổi thành định dạng dữ liệu raster cấp thấp. Nói chung, các ứng dụng khác nhau như họa sĩ minh họa, hệ thống soạn thảo tài liệu và thiết kế có sự hỗ trợ của máy tính (CAD) được tự động tạo ra các mô tả trang PostScript. Nói chung, các lập trình viên phải viết các chương trình PostScript tại thời điểm tạo ứng dụng mới. Tuy nhiên, một lập trình viên có thể tận dụng các khả năng của ngôn ngữ PostScript mà không phải ứng dụng nào cũng có được bằng cách viết một chương trình PS cho tình huống đặc biệt đó.

## Lược Sử ##

Khái niệm về ngôn ngữ PostScript lần đầu tiên được giới thiệu bởi John Warnock. Năm 1966, ông đang thực hiện dự án Cảng New York. Anh ấy đang cố gắng phát triển một trình thông dịch đồ họa ba chiều lớn cho cơ sở dữ liệu của dự án đó. Để xử lý những đồ họa này, John Warnock đã nghĩ ra ngôn ngữ Hệ thống thiết kế. Trong khi đó, Xerox PARC đang tìm kiếm một phương tiện tiêu chuẩn để xác định hình ảnh trang cho máy in laser đầu tiên của họ. Mặc dù Bob Sproull và William Newman vào năm 1975-76 đã phát triển định dạng Báo chí (định dạng dữ liệu) để điều khiển máy in laser nhưng vẫn cần một ngôn ngữ để linh hoạt hơn. Năm 1978, Warnock tham gia cùng Martin Newell tại Xerox PARC và viết lại ngôn ngữ diễn giải, JaM, ngôn ngữ này sau đó được phát triển và mở rộng thành ngôn ngữ Interpress. Warnock thành lập Adobe Systems vào tháng 12 năm 1982 cùng với Chuck Geschke, Doug Brotz, Ed Taft và Bill Paxton. Họ bắt đầu làm việc trên một ngôn ngữ đơn giản hơn gọi là PostScript tương tự như Interpress, được phát hành thương mại vào năm 1984. Steve Jobs từ Apple đã đến thăm họ và khuyên họ nên điều chỉnh PostScript để điều khiển máy in laser.

Vào tháng 3 năm 1985, máy in đầu tiên có trình thông dịch PostScript được nhúng là LaserWriter của Apple, đã cách mạng hóa việc xuất bản trên máy tính để bàn (DTP). Sự ổn định về kỹ thuật và tính khả dụng rộng rãi đã khiến PostScript trở thành ngôn ngữ được lựa chọn cho xuất bản điện tử và máy tính để bàn. Trong suốt năm 1990, một trình thông dịch cho ngôn ngữ PostScript là một phần thiết yếu của máy in laser.

## Những đặc điểm chính ##

Các khả năng của ngôn ngữ PostScript để xử lý đồ họa tương tác và mô tả trang có các tính năng sau:

**Hình dạng:** Có bản chất tùy ý, có thể bao gồm các đường thẳng, đường cong, hình vuông và đường cong hình khối có thể tự đi ngang và không liên kết (trong các phần và lỗ).

**Các toán tử vẽ:** cho phép đường viền hình dạng có độ dày, màu sắc, màu tô bất kỳ hoặc cho phép vẽ hình dưới dạng cắt xén để cho phép cắt xén bất kỳ đồ họa nào khác.

**Màu sắc:** có sự đa dạng như thang độ xám, RGB, CMYK và CIE. Các loại màu đặc biệt được mô hình hóa thành các tính năng khác nhau: màu vết, ánh xạ màu, thậm chí bóng và các mẫu lặp lại.

**Văn bản:** được tích hợp đầy đủ với đồ họa. Hơn nữa, mô hình hình ảnh adobe cho phép các ký tự văn bản được hiển thị dưới dạng hình dạng đồ họa có thể được vận hành bởi bất kỳ toán tử đồ họa thông thường nào.

**Hình ảnh được lấy mẫu**: được trích xuất từ các nguồn gốc (ảnh được quét) hoặc có thể được sản xuất tổng hợp. Ngôn ngữ PostScript cung cấp các phương tiện đa dạng để tái tạo hình ảnh ở bất kỳ độ phân giải nào và theo các kiểu màu khác nhau trên thiết bị đầu ra.

Một ngôn ngữ lập trình có mục đích chung có thể tận dụng các khả năng đồ họa của ngôn ngữ PostScript bằng cách nhúng Ps vào trong khuôn khổ của nó. Các kiểu dữ liệu nguyên thủy, chẳng hạn như số, ký tự, mảng và chuỗi; kiểm soát nguyên thủy, chẳng hạn như, vòng lặp, thủ tục và điều kiện; và một số tính năng độc đáo, chẳng hạn như từ điển được chỉ định trong ngôn ngữ. Các tính năng này tạo điều kiện cho người lập trình viết các lệnh để gọi các hoạt động cấp cao hơn. Các hoạt động cấp cao này đáp ứng nhu cầu của ứng dụng phức tạp. Cách thực hành như vậy gọn nhẹ và hiệu quả hơn là sử dụng một tập hợp các thao tác cơ bản cố định.

Các chương trình được viết bằng PostScript có thể được sản xuất, giao tiếp và diễn giải dưới dạng văn bản nguồn ASCII. Toàn bộ ngôn ngữ có thể được định nghĩa dưới dạng các ký tự có thể in được và khoảng trắng. Biểu diễn này hỗ trợ người lập trình tạo, thao tác và hiểu ngôn ngữ một cách dễ dàng. Hơn nữa, việc lưu trữ và truyền tệp giữa các máy tính và hệ điều hành khác nhau vẫn thuận tiện thông qua tính độc lập của máy.

Các dạng mã hóa nhị phân của ngôn ngữ có thể thực hiện được khi chương trình được đảm bảo có một đường dẫn truyền thông hoàn toàn minh bạch tới trình thông dịch PostScript. Sự gắn kết chặt chẽ với biểu diễn ASCII của các chương trình PS được Adobe khuyên dùng để trao đổi tài liệu hoặc lưu trữ.

## Phiên bản ##

PS(.ps) là phần mở rộng tệp cho tài liệu PostScript. Lưu trữ Quốc gia Vương quốc Anh phân loại năm phiên bản theo trình tự thời gian của tệp PostScript, được định nghĩa trong phiên bản DSC: phiên bản 1.0, 2.0, 2.1, 3.0, 3.1. Mỗi phiên bản xác định các nhận xét cấu trúc quan trọng. Tệp PostScript được đóng gói (EPS) là một kiểu con đặc biệt của tệp PostScript sử dụng ngôn ngữ để chỉ định đồ họa hình chữ nhật. Sổ tay tham khảo ngôn ngữ PostScript mô tả một EPS là "Tệp PostScript (EPS) được đóng gói là một chương trình PostScript mô tả tối đa một trang trong một biểu mẫu mà các ứng dụng khác có thể nhập để nhúng vào trong tài liệu chứa." Một tệp tài liệu PostScript có thể đóng gói một tệp EPS trong đó. Việc sử dụng thêm PostScript được đề cập là Hiển thị PostScript (DPS). DPS tạo đồ họa trên màn hình thông qua một công cụ đồ họa sử dụng mô hình và ngôn ngữ hình ảnh PostScript.

## Người giới thiệu ##

* [Họ định dạng PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

