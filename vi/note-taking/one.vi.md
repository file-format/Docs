{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Định dạng tệp Microsoft OneNote",
  "description":"Tìm hiểu về MỘT định dạng tệp và các API có thể tạo và mở MỘT tệp.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp .ONE là gì? ##

Tệp đại diện bởi phần mở rộng .ONE được tạo bởi ứng dụng Microsoft OneNote. OneNote cho phép bạn thu thập thông tin bằng cách sử dụng ứng dụng như thể bạn đang sử dụng bảng nháp để ghi chú. Các tệp OneNote có thể chứa các thành phần khác nhau có thể được đặt ở các vị trí không cố định trên các trang tài liệu. Các thành phần này có thể chứa văn bản, chữ viết tay số hóa và các đối tượng được sao chép từ các ứng dụng khác bao gồm hình ảnh, bản vẽ và clip đa phương tiện (âm thanh/video). Microsoft hiện cung cấp phiên bản trực tuyến của OneNote như một phần của Office365 nơi có thể chia sẻ Ghi chú với những người dùng OneNote khác qua internet.

## Thông số kỹ thuật định dạng tệp .ONE ##

Định dạng tệp OneNote cung cấp một cách hiệu quả để biểu diễn các ghi chú kỹ thuật số dưới dạng tập hợp các phần và trang có thứ bậc. Mỗi trang chứa nội dung do người dùng xác định trong một cấu trúc cụ thể để biểu diễn bằng định dạng tệp Mô hình Đối tượng Tài liệu (DOM). Mô hình dữ liệu của định dạng này như minh họa bên dưới.

### Tổng quan về cấu trúc ###

Như được minh họa trong mô hình dữ liệu cho định dạng tệp OneNote, tài liệu OneNote bao gồm các phần tử khác nhau.

#### Tiết diện ####

Một phần là vùng chứa trên cùng trong tệp OneNote, ngoài ra còn chứa các phần tử khác nhau trong đó như:

* Trang
* Metadata
* Đặc tính

Siêu dữ liệu và thuộc tính bao gồm tên phần, nhận dạng các trang có trong phần và thứ tự các trang đó xuất hiện. Thuật ngữ "phần" dùng để chỉ tất cả các trang nằm trong một phần và biểu thị dữ liệu đó trong tệp lưu trữ bản sửa đổi OneNote®, có phần mở rộng tên tệp .one.

#### Trang ####

Nội dung do người dùng xác định trong tài liệu OneNote được chứa bên trong một trang. Thông tin trang bao gồm văn bản, danh sách, bảng, tiêu đề trang, hình ảnh và thẻ ghi chú. Một trang bao gồm các đối tượng phác thảo mà hầu hết các đối tượng chứa trong đó được thêm vào. Mỗi trang có thể được gán một tên để thể hiện có ý nghĩa và các đối tượng cũng có thể được thêm trực tiếp vào các trang. Một trang có thể chứa thêm các trang phụ trong một hệ thống phân cấp.

#### Thuộc tính và Tập thuộc tính ####

Nội dung OneNote bao gồm các thuộc tính, bộ thuộc tính và đối tượng dữ liệu tệp. Bộ thuộc tính là tập hợp các thuộc tính đại diện cho một số loại nội dung. Đối tượng dữ liệu tệp là một khối dữ liệu nhị phân chứa ảnh, tệp nhúng hoặc nội dung âm thanh/video.

#### Sổ tay OneNote ####

Sổ ghi chép là một tập hợp các tệp phần được lưu trữ trong cùng một thư mục. Một tập hợp các thuộc tính được sử dụng để chỉ định các cài đặt chẳng hạn như thứ tự của các phần trong sổ ghi chép và màu của sổ ghi chép.

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

|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Một số nguyên không dấu. PHẢI là một trong các giá trị trong bảng sau, tùy thuộc vào định dạng tệp của tệp này.

|Định dạng tệp|Giá trị
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 byte):` Một cấu trúc **FileChunkReference32** PHẢI có giá trị là "fcrZero".

`fcrLegacyTransactionLog (8 byte):` Cấu trúc **FileChunkReference32** PHẢI là "fcrNil".

`cTransactionsInLog (4 byte):` Một số nguyên không dấu chỉ định số lượng giao dịch trong nhật ký giao dịch. KHÔNG ĐƯỢC bằng không.

`cbLegacyExpectedFileLength (4 byte):` Một số nguyên không dấu PHẢI bằng 0 và PHẢI được bỏ qua.

`rgbPlaceholder (8 byte):` Một số nguyên không dấu PHẢI bằng 0 và PHẢI được bỏ qua.

`fcrLegacyFileNodeListRoot (8 byte):` Cấu trúc **FileChunkReference32** PHẢI là "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 byte):` Một số nguyên không dấu PHẢI bằng 0 và PHẢI được bỏ qua.

`fNeedsDefrag (1 byte):` PHẢI được bỏ qua.

`fRepairedFile (1 byte):` PHẢI được bỏ qua.

`fNeedsGarbageCollect (1 byte):` PHẢI được bỏ qua.

`fHasNoEmbeddedFileObjects (1 byte):` Một số nguyên không dấu PHẢI bằng 0 và PHẢI được bỏ qua.

`guidAncestor (16 byte):` Một GUID chỉ định trường **Header.guidFile** của tệp mục lục, được cung cấp bởi bảng sau:


|Định dạng tệp mục lục|Vị trí của tệp mục lục
--- | --- |
|Tệp mục - .One|Tệp mục lục nằm trong cùng thư mục với tệp này.
|Tệp mục lục - .onetoc2|Tệp mục lục nằm trong thư mục mẹ của tệp này.

Nếu GUID là {00000000-0000-0000-0000-000000000000}, thì trường này không tham chiếu tệp mục lục.

`crcName (4 byte):` Một số nguyên không dấu xác định giá trị CRC của tên của tệp lưu trữ sửa đổi này. Tên là biểu diễn Unicode của tên tệp với phần mở rộng và một ký tự rỗng bổ sung ở cuối. CRC này luôn được tính toán bằng cách sử dụng thuật toán CRC cho tệp .one, bất kể định dạng tệp lưu trữ bản sửa đổi này.

`fcrHashedChunkList (12 byte):` Cấu trúc **FileChunkReference64x32** chỉ định tham chiếu đến **FileNodeListFragment** đầu tiên trong danh sách đoạn được băm. Nếu giá trị của cấu trúc **FileChunkReference64x32** là "fcrZero" hoặc "fcrNil", thì danh sách đoạn mã băm không tồn tại.

`fcrTransactionLog (12 byte):` Cấu trúc **FileChunkReference64x32** chỉ định tham chiếu đến cấu trúc **TransactionLogFragment** đầu tiên trong nhật ký giao dịch. Giá trị của trường **fcrTransactionLog** KHÔNG PHẢI là "fcrZero" và KHÔNG PHẢI là "fcrNil".

`fcrFileNodeListRoot (12 byte):` Cấu trúc **FileChunkReference64x32** chỉ định tham chiếu đến danh sách nút tệp gốc. Giá trị của trường **fcrFileNodeListRoot** KHÔNG PHẢI là "fcrZero" và KHÔNG PHẢI là "fcrNil".

`fcrFreeChunkList (12 byte):` Cấu trúc **FileChunkReference64x32** chỉ định tham chiếu đến cấu trúc **FreeChunkListFragment** đầu tiên. Nếu giá trị của cấu trúc **FileChunkReference64x32** là "fcrZero" hoặc "fcrNil", thì danh sách đoạn miễn phí không tồn tại.

`cbExpectedFileLength (8 byte):` Một số nguyên không dấu xác định kích thước, tính bằng byte, của tệp lưu trữ sửa đổi này.

`cbFreeSpaceInFreeChunkList (8 byte):` Một số nguyên không dấu NÊN chỉ định kích thước, tính bằng byte, của không gian trống được chỉ định bởi danh sách đoạn trống.

`guidFileVersion (16 byte):` GUID. Khi giá trị của trường **cTransactionsInLog** hoặc trường **guidDenyReadFileVersion** bị thay đổi, **guidFileVersion** PHẢI được thay đổi thành GUID mới.

`nFileVersionGeneration (8 byte):` Một số nguyên không dấu xác định số lần tệp đã thay đổi. PHẢI được tăng lên khi trường **guidFileVersion** thay đổi.

`guidDenyReadFileVersion (16 byte):` GUID. Khi nội dung hiện có của tệp đang được thay đổi, ngoại trừ cấu trúc **Header** của tệp và các khối lưu trữ không sử dụng, **guidDenyReadFileVersion** PHẢI được thay đổi thành GUID mới.

`grfDebugLogFlags (4 byte):` PHẢI bằng không. PHẢI bỏ qua.

`fcrDebugLog (12 byte):` Cấu trúc **FileChunkReference64x32** PHẢI có giá trị "fcrZero". PHẢI bỏ qua.

`fcrAllocVerificationFreeChunkList (12 byte):` Cấu trúc **FileChunkReference64x32** PHẢI là "fcrZero". PHẢI bỏ qua.

`bnCreated (4 byte):` Một số nguyên không dấu chỉ định số bản dựng của ứng dụng đã tạo tệp lưu trữ sửa đổi này. NÊN bỏ qua.

`bnLastWroteToThisFile (4 byte):` Một số nguyên không dấu chỉ định số bản dựng của ứng dụng được ghi lần cuối vào tệp lưu trữ sửa đổi này. NÊN bỏ qua.

`bnOldestWritten (4 byte):` Một số nguyên không dấu xác định số bản dựng của ứng dụng cũ nhất đã ghi vào tệp lưu trữ sửa đổi này. NÊN bỏ qua.

`bnNewestWritten (4 byte):` Một số nguyên không dấu chỉ định số bản dựng của ứng dụng mới nhất đã ghi vào tệp lưu trữ sửa đổi này. NÊN bỏ qua.

`rgbReserveed (728 byte):` PHẢI bằng không. PHẢI bỏ qua.

## Người giới thiệu ##

* [[MS-ONESTORE] - Định dạng tệp OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

