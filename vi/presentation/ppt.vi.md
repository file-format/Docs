{
  "date" : "2019-12-13",
  "keywords" :[ "tệp ppt", "định dạng tệp ppt", "tệp ppt là gì", "tệp", "ví dụ ppt", "phần mở rộng tệp ppt","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PPT và API có thể tạo và mở tệp PPT.",
  "title" :"PPT - Định dạng tệp PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PPT là gì?

Một tệp có phần mở rộng PPT đại diện cho tệp PowerPoint bao gồm một tập hợp các trang chiếu để hiển thị dưới dạng Trình chiếu. Nó chỉ định Định dạng tệp nhị phân được sử dụng bởi Microsoft PowerPoint 97-2003. Tệp PPT có thể chứa một số loại thông tin khác nhau, chẳng hạn như văn bản, dấu đầu dòng, hình ảnh, đa phương tiện và các đối tượng OLE nhúng khác. Microsoft đã đưa ra định dạng tệp mới hơn cho PowerPoint, được gọi là [PPTX](/vi/presentation/pptx/), từ năm 2007 trở đi dựa trên Office OpenXML và khác với định dạng tệp nhị phân này. Một số chương trình ứng dụng khác như OpenOffice Impress và Apple Keynote cũng có thể tạo tệp PPT.

## Lược Sử ##

Microsoft đã giới thiệu định dạng tệp PPT cùng với việc phát hành PowerPoint vào năm 1987. Định dạng nhị phân ổn định được chia sẻ làm mặc định trong PowerPoint 97-2003 cho Windows. Định dạng tệp nhị phân được hỗ trợ để đọc và viết bởi các phiên bản PowerPoint mới nhất cũng như PowerPoint 2016.

## Thông số kỹ thuật định dạng tệp ##

Kể từ khi được giới thiệu, định dạng tệp PPT đã trải qua một số lần sửa đổi để bổ sung các tính năng và cải tiến mới. Thông số kỹ thuật của phiên bản mới nhất hiện có là thông số kỹ thuật của phiên bản 6.0 đã được xuất bản vào tháng 8 năm 2018. Phiên bản này không được trộn lẫn với số sản phẩm thực của định dạng tệp PPT vì Microsoft không còn cung cấp các sửa đổi cho định dạng này nữa.

### Tổng quan về định dạng tệp ###

Một số thành phần chính của định dạng tệp PPT như sau:

#### Trang trình bày ####

Dữ liệu người dùng như hình dạng, văn bản, hoạt ảnh và phương tiện được thêm vào bản trình bày bên trong Trang trình bày. Một bài thuyết trình có thể chứa một hoặc nhiều trang chiếu được hiển thị dưới dạng trình chiếu khi chạy bài thuyết trình. Một bản trình bày chứa các trang chiếu chính và các trang chiếu chính tiêu đề hoạt động như khuôn mẫu cho các thuộc tính trực quan phổ biến của các trang chiếu trình bày. Ngoài ra còn có một trang chiếu chính ghi chú và trang chiếu chính của bản phân phát phục vụ mục đích tương tự và cung cấp các thuộc tính trực quan chung cho tất cả các trang chiếu ghi chú và tất cả các bản phân phát được in.

#### Hình dạng ####

Hình dạng là các đối tượng cho phép người dùng thêm nhiều nội dung vào trang chiếu dưới dạng hình dạng giữ chỗ, ảnh và đồ thị. Hình dạng trên trang chiếu chính xác định dữ liệu chung cho các nhóm hình dạng.

#### Giữ chỗ Hình dạng ####

Đây là những trình giữ chỗ đặc biệt đóng vai trò là vùng chứa cho nhiều đối tượng. Các hình dạng giữ chỗ khác nhau có thể được sử dụng để cung cấp manh mối để chèn các loại hình dạng cụ thể, chẳng hạn như bảng hoặc biểu đồ. Bên trong một trang chiếu, một hình dạng giữ chỗ áp dụng cho các thuộc tính trực quan từ trang chiếu chính chính, trang chiếu chính tiêu đề hoặc trang chiếu chính ghi chú.

#### Đối tượng bên ngoài ####

Các đối tượng bên ngoài như âm thanh được nhúng và liên kết, video được liên kết, các đối tượng OLE được nhúng và liên kết cũng như siêu kết nối có thể được nhúng trong một trang chiếu. Các đối tượng này có thể được sử dụng để kích hoạt các đối tượng được liên kết để truy cập các tài nguyên bên ngoài trong khi trình chiếu.

### Cấu trúc định dạng tệp ###

Các định dạng tệp nhị phân PowerPoint bao gồm các luồng sau để thể hiện cấu trúc và dữ liệu tài liệu tổng thể.

* Luồng người dùng hiện tại
* Luồng tài liệu PowerPoint
* Dòng hình ảnh
* Thông tin Tóm tắt và Thông tin Tóm tắt Tài liệu (Tùy chọn)

Thông số kỹ thuật đầy đủ cho định dạng tệp DOC có thể được cung cấp bởi [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) và nên được tư vấn liên quan đến các phần được đề cập trong các chi tiết sau đây.

#### Luồng người dùng hiện tại ####

Nó lưu hồ sơ của người dùng cuối cùng đã mở tài liệu và tên của nó phải là "Người dùng hiện tại".

#### Luồng tài liệu PowerPoint ####

Lưu giữ bản ghi tất cả thông tin về bản trình bày PowerPoint và giải thích bố cục và nội dung của nó. Đó là luồng bắt buộc có tên PHẢI là "Tài liệu PowerPoint". Nội dung của luồng này được chỉ định bởi một chuỗi các bản ghi cấp cao nhất. Các hạn chế đặt hàng một phần trên chuỗi bản ghi được chỉ định trong các bản ghi PersistDirectoryAtom và UserEditAtom.

Là bản ghi vùng chứa, mỗi bản ghi DocumentContainer, MainMasterContainer (phần 2.5.3), HandoutContainer (phần 2.5.8), SlideContainer (phần 2.5.1) và NotesContainer (phần 2.5.6) đều là gốc của cây chứa các bản ghi vùng chứa và bản ghi nguyên tử. Bên trong bất kỳ bản ghi vùng chứa nào, có thể tồn tại các bản ghi khác không được liệt kê rõ ràng là bản ghi con. Các bản ghi không xác định được xác định khi trường recType của cấu trúc RecordHeader (phần 2.3.1) chứa một giá trị không được chỉ định bởi phép liệt kê RecordType (phần 2.13.24). Những bản ghi không xác định này, nếu gặp phải, PHẢI bị bỏ qua và CÓ THỂ<1> được giữ nguyên. Có thể bỏ qua các bản ghi không xác định bằng cách tìm kiếm các byte recLen chuyển tiếp từ phần cuối của cấu trúc RecordHeader.

Mỗi khi luồng này được ghi, các bản ghi cấp cao nhất mới, chỉnh sửa của người dùng, có thể được thêm vào luồng hiện có hoặc toàn bộ nội dung luồng có thể được thay thế bằng một chuỗi các bản ghi cấp cao nhất được cập nhật. Nếu toàn bộ luồng không được thay thế, bất kỳ bản ghi cấp cao nhất nào hiện có trước đây bao gồm bất kỳ chỉnh sửa nào của người dùng trước đó, đều có thể bị lỗi thời bởi các bản ghi cấp cao nhất được thêm vào sau đó bao gồm chỉnh sửa của người dùng hiện tại.

#### Dòng hình ảnh ####

Đây là luồng tùy chọn Chứa dữ liệu về ảnh có trong bản trình bày PowerPoint. Tên của nó PHẢI là "Pictures". Nội dung của luồng này được chỉ định bởi bản ghi OfficeArtBStoreDelay như được chỉ định trong phần [MS-ODRAW] 2.2.21.

#### Luồng thông tin tóm tắt ####

Nó giữ số liệu thống kê về tài liệu theo tiêu chuẩn Microsoft Office. Tên của Luồng thông tin tóm tắt phải là "\005SummaryInformation", trong đó \005 là ký tự có giá trị 0x0005, không phải là chuỗi ký tự "\005". Luồng này NÊN được bỏ qua đối với các tài liệu được mã hóa. Nội dung của luồng này được chỉ định trong phần [MS-OSHARED] 2.3.3.2.1.

#### Luồng thông tin tóm tắt tài liệu ####

Luồng tùy chọn có tên PHẢI là "\005DocumentSummaryInformation", trong đó \005 là ký tự có giá trị 0x0005, không phải chuỗi ký tự "\005". Luồng này CÓ THỂ<2> bị bỏ qua đối với các tài liệu được mã hóa. Nội dung của luồng này được chỉ định trong phần [MS-OSHARED] 2.3.3.2.2.

#### Luồng thông tin tóm tắt được mã hóa ####

Luồng tùy chọn có tên PHẢI là "EncryptedSummary". Luồng này chỉ tồn tại trong một tài liệu được mã hóa. Nội dung của luồng này được chỉ định trong [MS-OFFCRYPTO] phần 2.3.5.4.

#### Lưu trữ chữ ký số ####

Bộ lưu trữ tùy chọn có tên PHẢI là "_xmlsignatures". CÓ THỂ bỏ qua và CÓ THỂ bỏ qua. Nội dung của bộ lưu trữ này được chỉ định trong phần [MS-OFFCRYPTO] 2.5.2.

#### Lưu trữ dữ liệu XML tùy chỉnh ####

Bộ lưu trữ tùy chọn có tên PHẢI là "MsoDataStore". Nội dung của bộ lưu trữ được chỉ định trong [MS-OSHARED] phần 2.3.6.

#### Dòng chữ ký ####

Luồng tùy chọn có tên PHẢI là "_signatures". Nó NÊN được bỏ qua và CÓ THỂ được bỏ qua. Nội dung của luồng này được chỉ định trong [MS-OFFCRYPTO] phần 2.5.1.

## Người giới thiệu ##

* [Thông số định dạng tệp PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Cấu trúc đối tượng và kiểu dữ liệu chung của Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Cấu trúc mật mã tài liệu Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Định dạng tệp PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

