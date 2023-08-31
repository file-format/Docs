{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp BAK", "Phần mở rộng tệp BAK", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp BAK và API có thể tạo và mở tệp BAK.",
  "title" :"Định dạng tệp BAK - Tệp sao lưu cơ sở dữ liệu",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Tệp BAK là gì?

Tệp có phần mở rộng .bak thường là tệp sao lưu được các công cụ phần mềm khác nhau sử dụng để lưu trữ các bản sao lưu dữ liệu. Từ góc độ cơ sở dữ liệu, tệp BAK được Microsoft SQL Server sử dụng để lưu trữ nội dung của cơ sở dữ liệu. Tất cả dữ liệu và tệp được liên kết với cơ sở dữ liệu được lưu trữ ở định dạng tệp này để được truy xuất trong trường hợp cơ sở dữ liệu có thể bị hỏng hoặc không hợp lệ vì bất kỳ lý do gì. Các tệp sao lưu có thể được lưu trữ và lập chỉ mục trên các máy chủ khác vì mục đích an toàn. Một số ứng dụng có thể tạo tệp BAK như SQL Server Management Studio, Transact-SQL và Windows PowerShell.

## Định dạng tệp BAK

Các chi tiết bên trong của tệp BAK không được biết nhưng nhiều người cho rằng nó dựa trên Định dạng băng của Microsoft (MTF). Thông số kỹ thuật MTF có sẵn và có thể được tham khảo để hiểu cấu trúc của tệp. Tài liệu này cung cấp thông tin chi tiết về lưu trữ MTF cho bất kỳ ai có kiến thức chung về hoạt động quản lý lưu trữ, ổ băng từ và hệ thống tệp.

### Tập dữ liệu

Tập dữ liệu là tập hợp các đối tượng được ghi vào phương tiện lưu trữ (băng, đĩa quang, v.v.) trong quá trình sao lưu hoặc khôi phục dữ liệu. Bộ dữ liệu bao gồm nhiều phương tiện trong trường hợp khối lượng dữ liệu lớn.

### Các yếu tố cơ bản của MTF

Tệp MTF bao gồm một số thành phần cơ bản cấu thành các khối xây dựng của nó. Những yếu tố này là:

#### Khối mô tả

Khối mô tả (DBLK) được sử dụng để kiểm soát định dạng và tạo thành nền tảng chính của tệp MTF. Một tệp MTF duy nhất xác định nhiều DBLK cho mỗi vai trò duy nhất. Mỗi DBLK là một khối dữ liệu có độ dài thay đổi được chia thành bốn phần sau:

* `Tiêu đề khối chung` - Cấu trúc độ dài cố định chung cho tất cả các DBLK. Đây là Tiêu đề khối duy nhất được yêu cầu.
* `Thông tin loại DBLK` - Khối độ dài cố định dành riêng cho loại DBLK được xác định
* `Dữ liệu Hệ điều hành` - Dữ liệu cụ thể được xác định dựa trên loại DBLK và Hệ điều hành
* `Thông tin DBLK` - Thông tin cụ thể về DBLK có độ dài thay đổi không thể lưu với thông tin DBLK có Độ dài cố định.

 {{< figure src="../bak.png" alt="Định dạng tệp sao lưu Microsoft SQL" >}}

#### Dòng dữ liệu

Các luồng dữ liệu trong tệp MTF được sử dụng để đóng gói và căn chỉnh dữ liệu. Nó bao gồm một Tiêu đề luồng, theo sau là Dữ liệu luồng. Tiêu đề luồng chỉ có thể gói gọn một loại Dữ liệu luồng.

{{< figure src="../bak_datastream.png" alt="Định dạng tệp sao lưu Microsoft SQL" >}}

#### Dấu tệp

Dấu tệp được sử dụng để phân tách hợp lý và truy cập nhanh trong phương tiện. Dấu tệp được mô phỏng bởi trình điều khiển thiết bị hoặc bằng cách sử dụng khối Mô tả dấu tệp mềm trong trường hợp thiết bị đang được sử dụng không cung cấp dấu tệp.

## Người giới thiệu ##

* [[MS-BCP]: Định dạng sao chép hàng loạt](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

