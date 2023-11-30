{
"date" :  "2023-10-18",
   "keywords":[
"cpi",
"tệp cpi",
"tệp thông tin mã trang cpi",
"cách mở tệp cpi",
"tài liệu",
"phần mở rộng tập tin cpi",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp CPI - Tệp thông tin trang mã",
   "description":"Tìm hiểu về định dạng tệp Thông tin trang mã CPI và các API có thể tạo và mở tệp CPI.",
"linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
         "parent":"system"
}
},
"lastmod":"2023-10-18"
}

## Tập tin CPI là gì?

Tệp `.cpi`, trong ngữ cảnh của hệ điều hành Microsoft Windows và DOS, thường là **"Tệp thông tin trang mã."** Các tệp này chứa thông tin về các trang mã được sử dụng để mã hóa văn bản và ánh xạ bộ ký tự. Các trang mã rất cần thiết để hiển thị và xử lý văn bản bằng nhiều ngôn ngữ và bộ ký tự khác nhau.

Trong ngữ cảnh của Windows và DOS, các trang mã được sử dụng để xác định cách biểu diễn và mã hóa các ký tự trong các ngôn ngữ và khu vực khác nhau. Các trang mã này xác định cách các ký tự được lưu trữ trong bộ nhớ và hiển thị trên màn hình. Mỗi trang mã có mã định danh duy nhất và tệp `.cpi` lưu trữ thông tin về các trang mã này, bao gồm các chi tiết như ánh xạ ký tự và thông tin phông chữ.

Các tệp `.cpi` thường được tìm thấy trong các thư mục hệ thống Windows hoặc DOS và chúng đóng vai trò quan trọng trong việc cho phép hệ điều hành hiển thị văn bản chính xác cho các ngôn ngữ và bộ ký tự khác nhau. Chúng giúp hệ thống hiểu cách diễn giải và hiển thị các ký tự từ các ngôn ngữ và bảng mã khác nhau.

## Tệp thông tin trang mã

Chúng ta hãy xem xét kỹ hơn các Tệp thông tin trang mã (.cpi) và cách chúng hoạt động trong khuôn khổ MS-DOS và các phiên bản trước đó của Microsoft Windows:

1. **Mã hóa ký tự và trang mã**: Các trang mã là thành phần quan trọng trong cách mã hóa và hiển thị văn bản trên máy tính. Họ xác định mã hóa ký tự cho ngôn ngữ hoặc bộ ký tự cụ thể. Mỗi trang mã gán các giá trị số (điểm mã) cho các ký tự, cho phép máy tính biểu diễn và hiển thị chúng. Ví dụ: mã trang 437 thường được sử dụng ở Hoa Kỳ và Tây Âu, trong khi mã trang 850 được sử dụng để mã hóa Latin-1.
    







2. **Khởi tạo hệ thống**: Trong quá trình khởi tạo hệ thống (khi máy tính khởi động), MS-DOS và các phiên bản Windows cũ hơn sẽ đọc tệp `.cpi` để xác định trang mã nào sẽ hỗ trợ. Thông tin này rất quan trọng cho việc hiển thị văn bản, nhập liệu bằng bàn phím và chuyển đổi bộ ký tự.
    







3. **Hỗ trợ màn hình và bàn phím**: Những tệp này cung cấp thông tin về cách hiển thị các ký tự trên màn hình và bộ ký tự hoặc trang mã nào sẽ được hỗ trợ để nhập bằng bàn phím. Các trang mã khác nhau xác định các bộ ký tự khác nhau, vì vậy những tệp này giúp hệ điều hành biết cách xử lý dữ liệu nhập của người dùng và hiển thị văn bản một cách chính xác.
    







4. **Bản địa hóa**: Các tệp `.cpi` rất cần thiết cho việc bản địa hóa hệ điều hành. Chúng cho phép hệ thống thích ứng với các ngôn ngữ, khu vực và bộ ký tự khác nhau, giúp người dùng trên toàn thế giới có thể sử dụng MS-DOS hoặc Windows bằng ngôn ngữ ưa thích của họ.
    







5. **Nhiều tệp `.cpi`**: Trên máy tính có hỗ trợ đa ngôn ngữ, bạn có thể tìm thấy một số tệp `.cpi` tương ứng với các trang mã khác nhau. Ví dụ: hệ thống có thể có `437.cpi` cho Hoa Kỳ, `850.cpi` cho Latin-1, `852.cpi` cho Trung Âu, v.v. Tệp thích hợp được tải dựa trên ngôn ngữ của người dùng hoặc trang mã đã chọn.
    







6. **Thông tin phông chữ**: Ngoài ánh xạ ký tự, các tệp này có thể chứa thông tin phông chữ, chỉ định phông chữ nào sẽ sử dụng cho mỗi trang mã. Điều này rất quan trọng để hiển thị văn bản theo kiểu và kích thước phù hợp.
    







7. **Hệ thống kế thừa**: Tệp `.cpi` phổ biến hơn trong các phiên bản MS-DOS và Windows cũ hơn. Các phiên bản Windows hiện đại (chẳng hạn như Windows 10 trở lên) thường sử dụng Unicode để mã hóa văn bản, hỗ trợ nhiều loại ký tự và ngôn ngữ. Unicode đơn giản hóa việc xử lý văn bản cho môi trường đa ngôn ngữ và là tiêu chuẩn cho phần mềm hiện đại.

## Làm cách nào để mở tệp CPI?

Mở tệp .CPI (Thông tin trang mã) không phải là hành động thông thường của người dùng và những tệp này thường không được mở theo cách thủ công. Chúng được hệ điều hành sử dụng để quản lý mã hóa văn bản và bộ ký tự và nội dung của chúng được hệ thống truy cập và sử dụng tự động.

Tuy nhiên, nếu bạn muốn xem nội dung của tệp .CPI nhằm mục đích cung cấp thông tin, bạn có thể thử mở tệp đó bằng trình soạn thảo văn bản hoặc trình xem thập lục phân. Đây là cách bạn có thể thử mở tệp .CPI:

1. **Trình soạn thảo văn bản**: Bạn có thể sử dụng trình soạn thảo văn bản như Notepad (trên Windows) hoặc bất kỳ trình soạn thảo văn bản thuần túy nào trên các hệ điều hành khác để mở và xem tệp .CPI. Hãy nhớ rằng nội dung của tệp .CPI không phải để con người có thể đọc được và bạn có thể thấy một loạt ký tự khó diễn giải.
    







2. **Trình xem thập lục phân**: Có thể sử dụng trình xem thập lục phân hoặc trình soạn thảo thập lục phân để mở và kiểm tra nội dung của tệp .CPI ở dạng nhị phân thô. Trình chỉnh sửa hex cung cấp chế độ xem chi tiết hơn về dữ liệu của tệp, điều này có thể hữu ích nếu bạn đang cố gắng hiểu cấu trúc của tệp. Ví dụ về các phần mềm như vậy bao gồm HxD, Hex Fiend (dành cho macOS) và 010 Editor.

## Các tập tin CPI khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.cpi**.

**Hệ thống video**
- [CPI - Thông tin clip video AVCHD](/vi/video/cpi/)
- [CPI - Tệp thông tin trang mã](/vi/system/cpi/)

## Người giới thiệu
* [Trang mã](https://en.wikipedia.org/wiki/Code_page)

