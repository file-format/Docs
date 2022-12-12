{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Định dạng tệp Microsoft OneNote",
  "description":"Tìm hiểu về định dạng tệp ONETOC2 và các API có thể tạo và mở tệp ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2 là gì? ##

Những người đã làm việc với ứng dụng [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) có thể nhận thấy sự hiện diện của các tệp .onetoc2 trong thư mục sổ ghi chép. Microsoft OneNote tạo tệp nhị phân .onetoc2 dưới dạng Mục lục để giữ chỉ mục về thứ tự của các phần ghi chú khác nhau trong sổ ghi chép. Sổ ghi chép là một tập hợp các tệp phần được lưu trữ trong cùng một thư mục. Tệp .onetoc2 sử dụng một tập hợp các thuộc tính để chỉ định các cài đặt chẳng hạn như thứ tự các phần trong sổ ghi chép và màu của sổ ghi chép.

Khi bạn tạo sổ ghi chép trong OneNote 2016, nó sẽ tự động được lưu ở định dạng tệp 2010-2016 mới. Bạn sẽ cần định dạng này nếu muốn tất cả các tính năng trong OneNote 2016, như phương trình toán học và ghi chú được liên kết, hoạt động bình thường.

## Định dạng tệp ONETOC2 ##

Định dạng tệp .onetoc2 được biểu diễn dưới dạng Định dạng tệp lưu trữ bản sửa đổi OneNote và là một tập hợp các cấu trúc chỉ định một kho sửa đổi được tổ chức thành các không gian đối tượng được tham chiếu chéo, chứa các đối tượng có bộ thuộc tính và chứa nhật ký giao dịch để đảm bảo tính toàn vẹn của tệp trong quá trình không đồng bộ viết. Toàn bộ thông số kỹ thuật cho định dạng tệp .onetoc2 hiện có [trực tuyến](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) và có thể tham khảo để phát triển ứng dụng .

### Cấu trúc tệp ###

Tệp lưu trữ bản sửa đổi PHẢI bắt đầu bằng cấu trúc **Header**. Phần còn lại của tệp được phân vùng thành các khối byte, trong đó kích thước và cấu trúc của mỗi khối được chỉ định bởi trường tham chiếu nó. Một khối có thể truy cập được nếu nó được tham chiếu bởi cấu trúc **Header** hoặc nếu nó được tham chiếu bởi một trường trong một khối có thể truy cập khác. Dữ liệu bên ngoài cấu trúc **Header** và mọi khối có thể truy cập PHẢI được bỏ qua.

Tất cả các cấu trúc được căn chỉnh trên ranh giới 1 byte. Tất cả các số nguyên được ký trừ khi có quy định khác. Tất cả các trường đều là [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) trừ khi có quy định khác.

#### Tiêu đề ####

Tiêu đề của tệp .ONE bao gồm các khối chứa các id và trường duy nhất khác nhau để thể hiện thông tin tệp như sau:

`guidFileType (16 byte):` GUID chỉ định loại tệp lưu trữ sửa đổi. PHẢI là một trong các giá trị từ bảng sau.

|Định dạng tệp|Giá trị
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 byte):` GUID chỉ định danh tính của tệp lưu trữ sửa đổi này. NÊN là duy nhất trên toàn cầu.

`guidLegacyFileVersion (16 byte):` PHẢI là "{00000000-0000-0000-0000-000000000000}" và PHẢI được bỏ qua.

`guidFileFormat (16 byte):` GUID chỉ định rằng tệp là tệp lưu trữ sửa đổi. PHẢI là "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 byte):` Một số nguyên không dấu. PHẢI là một trong các giá trị trong bảng sau, tùy thuộc vào loại tệp.

|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 byte):` Một số nguyên không dấu. PHẢI là một trong các giá trị trong bảng sau, tùy thuộc vào định dạng tệp của tệp này.


|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 byte):` Một số nguyên không dấu. PHẢI là một trong các giá trị trong bảng sau, tùy thuộc vào định dạng tệp của tệp này.
:


|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Một số nguyên không dấu. PHẢI là một trong các giá trị trong bảng sau, tùy thuộc vào định dạng tệp của tệp này.


|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Người giới thiệu ##

* [[MS-ONESTORE] - Định dạng tệp OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

