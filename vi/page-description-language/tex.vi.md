{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp TEX",
  "description":"Tìm hiểu về định dạng tệp TEX và API có thể tạo và mở tệp TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp TEX là gì? ##

**TeX** là ngôn ngữ bao gồm các tính năng lập trình cũng như đánh dấu, được sử dụng để sắp chữ tài liệu. Donald Knuth từ Đại học Stanford, là người tạo ra hệ thống sắp chữ tháo vát này. Trên khắp thế giới, TeX là sự lựa chọn cuối cùng của các tác giả và nhà xuất bản để tạo ra các tài liệu kỹ thuật chất lượng cao. TeX thực hiện xuất sắc công việc định dạng các biểu thức toán học phức tạp. Cùng với một máy sắp chữ ảnh chất lượng cao, TeX cạnh tranh với các kết quả do các hệ thống sắp chữ truyền thống tốt nhất tạo ra. Do đó được coi là hệ thống đánh máy kỹ thuật số đẳng cấp nhất.

Các tệp đầu vào TeX dựa trên mã ASCII, do đó cho phép chia sẻ bản thảo giữa các nhà văn, nhà quản lý xuất bản và nhà phê bình. Một loạt các môi trường máy tính, hầu hết mọi nền tảng hiện đại và nhiều nền tảng cũ hơn đều hỗ trợ TeX. Hơn nữa, TeX là một phần mềm miễn phí, có sẵn cho nhiều người tiêu dùng. Nhiều bản cài đặt UNIX sử dụng cả UNIX troff và TeX làm hệ thống định dạng cho các mục đích khác nhau. Các tác vụ sắp chữ khác được thực hiện rất nhiều dưới dạng LaTeX, ConTeXt và các gói macro khác.

## Lược Sử ##

TeX được thiết kế và viết bởi Donald Knuth vào năm 1978. Guy Steele từ Viện Công nghệ Massachusetts đã sửa đổi đầu vào/đầu ra của TeX để làm cho nó chạy trong hệ điều hành Không tương thích như Hệ thống chia sẻ thời gian (ITS). Phiên bản đầu tiên của TeX được phát triển trong hệ điều hành WAITS của Stanford bằng ngôn ngữ lập trình (SAIL) và được thử nghiệm để chạy trên PDP-10. Knuth đã giới thiệu ý tưởng về lập trình biết chữ cho các phiên bản nâng cao. Lập trình biết chữ là một cách tạo mã nguồn có thể biên dịch được và bộ sắp chữ (bằng TeX) cho tài liệu được liên kết chéo bằng tệp gốc. Ngôn ngữ được sử dụng để phát triển các phiên bản TeX nâng cao này được gọi là WEB, một hỗn hợp của các chương trình Pascal PDP-10 của DEC để đảm bảo tính di động.

Một phiên bản mới được sửa đổi của TeX xuất bản năm 1982 và được gọi là TeX82. Thay đổi chính là việc thay thế thuật toán gạch nối ban đầu bằng thuật toán mới được viết bởi Frank Liang. Để đảm bảo tính di động trên các nền tảng khác nhau, Thay vì sử dụng dấu phẩy động, TeX82 sử dụng số học dấu phẩy động cùng với ngôn ngữ lập trình thực, hoàn chỉnh. Năm 1989, phiên bản mới của TeX và Metafont được phát hành. Vì vậy, phiên bản 3.0 của TeX hỗ trợ đầu vào 8 bit, cho phép 256 ký tự khác nhau trong văn bản. Sau phiên bản 3, các bản cập nhật được biểu thị bằng cách thêm một chữ số phụ vào cuối phần thập phân, ví dụ: phiên bản hiện tại của TeX được chỉ định là 3.14159265. Phiên bản này được cập nhật lần cuối vào ngày 12-1-2014.

## Đầu vào TeX ##

Tệp đầu vào TEX có thể được chuẩn bị bằng trình soạn thảo văn bản sử dụng văn bản thông thường. Không giống như trình xử lý Word thông thường, tệp đầu vào này không cho phép bất kỳ ký tự điều khiển vô hình nào. Một tệp có thể được nhúng vào một tệp khác, chứa các định nghĩa macro và các định nghĩa phụ giúp nâng cao khả năng của TeX. Nếu bản cài đặt TeX đi kèm với bất kỳ tệp macro nào, thì thông tin cục bộ về TeX sẽ minh họa về cách sử dụng tệp macro. Dạng tiêu chuẩn của TeX, tích hợp tổ hợp macro và các định nghĩa khác được gọi là TEX thuần túy.

Trên cơ sở kiến thức chính xác về kích thước của tất cả các ký tự và ký hiệu, nó tính toán tổ chức tối ưu của các chữ cái trên mỗi dòng và các dòng trên mỗi trang. Tại thời điểm xử lý tài liệu, tệp .dvi được tạo, trong đó “dvi” là viết tắt của “thiết bị độc lập”. Cần có các chương trình trình điều khiển thiết bị để in hoặc xem trước tài liệu có phần mở rộng dvi. Ngày nay, thế hệ dvi bị bỏ qua bởi pdf-TeX thường được sử dụng. Không có kiến thức trước về phông chữ trong quá trình cài đặt TeX, vì vậy các tệp phông chữ bên ngoài, là một phần của môi trường TeX cục bộ được sử dụng để lấy thông tin cho tài liệu.

## Hệ thống sắp chữ ##

Hệ thống TeX cơ sở có thể hiểu được khoảng 300 nguyên hàm (lệnh). Nguyên thủy là các lệnh cấp thấp, do đó, một người dùng thông thường hiếm khi sử dụng chúng trực tiếp và hầu hết chức năng được thực hiện bởi các tệp định dạng. Các tệp định dạng này là các hình ảnh bộ nhớ được tải trước của TeX, theo sau là việc tải các bộ sưu tập macro lớn. Định dạng mặc định ban đầu của ngôn ngữ tức là TeX đơn giản thêm khoảng 600 lệnh.

Dấu gạch chéo ngược được nhóm với dấu ngoặc nhọn biểu thị phần bắt đầu của lệnh TeX. Vì TeX là ngôn ngữ dựa trên macro và mã thông báo, nên hầu như tất cả các đặc điểm cú pháp của TeX có thể được thay đổi trong thời gian chạy, bao gồm cả những mã do người dùng xác định ngoại trừ các mã thông báo không thể mở rộng sau đó được thực thi. Bản thân việc mở rộng thực tế không gặp sự cố. Một số lệnh cần phải xuất hiện sau một đối số giúp giải thích chức năng của lệnh. Chẳng hạn, lệnh \vskip chỉ đạo TEX chuyển xuống/lên trang, theo sau là một đối số xác định lượng không gian cần bỏ qua.

## Phiên bản ##

LaTeX là định dạng được sử dụng thường xuyên nhất do Leslie Lamport phát triển. LaTeX tích hợp các kiểu tài liệu khác nhau cho tệp, chữ cái, sách và trang trình bày, đồng thời cung cấp tham chiếu và đánh số tự động cho các phần và biểu thức toán học khác nhau. AMS-TeX là một định dạng phổ biến khác, được phát triển bởi Hiệp hội Toán học Hoa Kỳ.

AMS-TeX cung cấp nhiều lệnh thân thiện với người dùng hơn, có thể được định nghĩa lại bởi các tạp chí để phù hợp với phong cách địa phương của họ. LaTeX có thể tận dụng các lợi ích của AMS-TeX bằng cách sử dụng các "gói" AMS mà sau đó được gọi là AMS-LaTeX. ConTeXt là một định dạng khác được viết bởi Hans Hagen được sử dụng chủ yếu để xuất bản trên máy tính để bàn.

Phần mềm TeX cung cấp một số tính năng không có sẵn hoặc có chất lượng thấp hơn trong các hệ thống sắp chữ khác tại thời điểm tạo ra nó. Một số tính năng sáng tạo của ngôn ngữ này dựa trên các thuật toán thú vị bắt nguồn từ luận văn của các sinh viên của Knuth. Trong khi các chương trình sắp chữ khác hiện đang tích hợp các tính năng hữu ích của TeX vào chương trình của họ.

## Người giới thiệu ##

* [Hệ thống sắp chữ TeX](https://en.wikipedia.org/wiki/TeX)

