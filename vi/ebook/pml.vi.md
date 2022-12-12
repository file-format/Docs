{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "extension", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PML, Ngôn ngữ đánh dấu Palm và các API có thể tạo và mở tệp PML.",
  "title" :"PML - Tệp ngôn ngữ đánh dấu Palm",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Tệp PML là gì?

Palm Inc đã giới thiệu định dạng tệp PML viết tắt của Palm Markup Language File. Mục đích của nó là tạo tài liệu cho eReader, một thiết bị đọc sách điện tử tương tự như máy tính bảng. Tệp PML cung cấp bố cục cho tệp [PDB](/vi/ebook/pdb/) (chứa nhiều tệp dữ liệu khác nhau) để hiển thị trên Thiết bị Palm.

## Chi tiết kỹ thuật của Tệp PML

Cấu trúc của tệp PML bao gồm các thẻ để tạo thiết lập Sách điện tử, bao gồm các đoạn văn, tiêu đề, thụt lề và tài liệu tham khảo. Nó cũng cho phép các thẻ định dạng như Bold, Small Caps và Superscript. Các nhà phát triển cũng có thể thêm hình ảnh vào sách điện tử.

### Ngôn ngữ đánh dấu Palm
Bảng sau chỉ định các lệnh PML:

|Lệnh|Mô tả|
---|---|
| \p | Trang mới |
| \x | Chương mới; cũng gây ra hiện tượng ngắt trang mới. Kèm theo tiêu đề chương (và bất kỳ mã kiểu dáng nào) với \x và \x |
| \Xn | Chương mới, n cấp thụt lề (bao gồm cả n từ 0 đến 4) trong hộp thoại Chương; không gây ngắt trang. Kèm theo tiêu đề chương (và bất kỳ mã kiểu dáng nào) với \Xn và \Xn |
| \Cn="Tiêu đề chương" | Chèn "Tiêu đề chương" vào danh sách chương, với cấp n (như \Xn). Văn bản không được hiển thị trên trang và không buộc phải ngắt trang. Điều này đôi khi có thể hữu ích để chèn một dấu chương ở phần đầu của phần giới thiệu chương, chẳng hạn. |
| \c | Căn giữa khối văn bản này; đóng bằng \c ở đầu dòng |
| \ r | Căn phải khối văn bản; đóng bằng \r ở đầu dòng |
| \i | In nghiêng khối; đóng bằng \i |
| \u | gạch dưới khối; đóng bằng \u |
| \o | Tấn công khối; đóng bằng \o |
| \v | Văn bản vô hình; đóng bằng \v (có thể dùng để bình luận) |
| \t | khối thụt lề. Bắt đầu ở đầu dòng, đóng bằng \t ở cuối dòng |
| \T="50%" | Thụt lề phần trăm được chỉ định của chiều rộng màn hình, 50% trong trường hợp này. Nếu vị trí bản vẽ hiện tại đã vượt qua vị trí màn hình được chỉ định, thì thẻ này sẽ bị bỏ qua. |
| \w="50%" | Nhúng quy tắc ngang có chiều rộng phần trăm nhất định của màn hình, trong trường hợp này là 50%. Thẻ này gây ngắt dòng trước và sau nó. Quy tắc là trung tâm. Dấu phần trăm là bắt buộc. |
| \n | Chuyển sang phông chữ "bình thường" do người dùng chỉ định |
| \s | Chuyển sang stdFont; đóng bằng \s để hoàn nguyên về phông chữ bình thường |
| \b | Chuyển sang kiểu chữ đậm; đóng bằng \b để hoàn nguyên về phông chữ bình thường (không dùng nữa; thay vào đó hãy sử dụng \B) |
| \l | Chuyển sang phông chữ lớn; đóng bằng \l để hoàn nguyên về phông chữ bình thường |
| \B | Đánh dấu văn bản là in đậm. Không giống như thẻ \b, \B không thay đổi phông chữ, vì vậy bạn có thể in đậm văn bản lớn. Bạn không thể kết hợp \b và \B trong cùng một tệp PML. |
| \Sp | Đánh dấu văn bản là chỉ số trên. Không nên trộn lẫn với các kiểu khác như in đậm, in nghiêng, v.v. Đính kèm văn bản được viết trên cùng với \Sp. |
| \Sb | Đánh dấu văn bản là chỉ số dưới. Không nên trộn lẫn với các kiểu khác như in đậm, in nghiêng, v.v. Đính kèm văn bản được chỉ định bằng \Sb. |
| \k | Đặt văn bản đính kèm thành chữ hoa nhỏ; đóng bằng \k. Bất kỳ ký tự nào nằm trong thẻ \k (kể cả những ký tự có dấu) đều được viết hoa và hiển thị ở kích thước điểm nhỏ hơn so với ký tự viết hoa thông thường. |
| \\ | Đại diện cho một dấu gạch chéo ngược đơn |
| \aXXX | Chèn ký tự không phải ASCII có mã Windows-1252 là số thập phân XXX. Xem bảng ký tự PML để biết chi tiết. |
| \UXXXX | Chèn ký tự không phải ASCII có mã Unicode ở dạng thập lục phân XXXX. Xem bảng ký tự PML mở rộng để biết chi tiết. |
| \m="tên_hình_ảnh.png" | Chèn hình ảnh được đặt tên. Xem phần về Hình ảnh bên dưới. |
| \q="#linkanchor"Một số văn bản\q | Tham chiếu một neo liên kết ở một vị trí khác trong tài liệu. Chuỗi sau đặc tả neo và trước dấu \q được gạch dưới hoặc được hiển thị là một liên kết khi xem tài liệu. |
| \Q="linkanchor" | Chỉ định một neo liên kết trong tài liệu. |
| \- | Chèn một dấu gạch nối mềm. Dấu gạch nối mềm chỉ xuất hiện nếu cần ngắt một từ trên một dòng. |
| \Fn="footnote1"1\Fn | Liên kết "1" với chú thích có tên là footnote1, được gắn thẻ ở cuối tài liệu PML. Xem phần Chú thích và Thanh bên bên dưới. |
| \Sd="sidebar1"Thanh bên\Sd | Liên kết văn bản "Thanh bên" với một thanh bên có tên là sidebar1, được gắn thẻ ở cuối tài liệu PML. Xem phần Chú thích và Thanh bên bên dưới. |
| \Tôi | Đánh dấu là mục chỉ mục tham khảo. Kèm theo mục chỉ mục (và bất kỳ mã kiểu dáng nào) với \I và \I.|
 


## Người giới thiệu

* [Ngôn ngữ đánh dấu lòng bàn tay - Bởi MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - By MobileRead](https://vi.wikipedia.org/wiki/E-reader)

