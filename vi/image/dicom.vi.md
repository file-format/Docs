{
  "date" : "2019-10-11",
  "keywords" :[ "tệp dicom", "định dạng tệp dicom", "tệp dicom là gì", "tệp", "ví dụ dicom", "phần mở rộng tệp dicom","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Định dạng tệp liên lạc và hình ảnh kỹ thuật số",
  "description":"Tìm hiểu về định dạng tệp DICOM và API có thể tạo và mở tệp DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tập tin DICOM là gì?

DICOM là từ viết tắt của Digital Imaging and Communications in Medicine và liên quan đến lĩnh vực Tin học Y tế. DICOM được sử dụng để tích hợp các thiết bị hình ảnh y tế như máy in, máy chủ, máy quét, v.v. từ nhiều nhà cung cấp khác nhau và cũng chứa dữ liệu nhận dạng của từng bệnh nhân để đảm bảo tính duy nhất. Các tệp DICOM có thể được chia sẻ giữa hai bên nếu chúng có khả năng nhận dữ liệu hình ảnh ở định dạng DICOM. Phần giao tiếp của DICOM là giao thức tầng ứng dụng và sử dụng TCP/IP để giao tiếp giữa các thực thể. Các phiên bản được dịch vụ web hỗ trợ là 1.0, 1.1, 2 trở lên.

## Lịch sử ##

DICOM được đồng phát triển bởi American College of Radiology (ACR) và Hiệp hội các nhà sản xuất điện quốc gia (NEMA) để trao đổi và xem các hình ảnh y tế như MRI, CT scan và hình ảnh siêu âm. Ban đầu, thật khó để giải mã những hình ảnh mà máy tạo ra. Do đó, ACR và NEMA đã cùng nhau thành lập một nhóm vào năm 1983. Nhóm này đã phát hành tiêu chuẩn đầu tiên, ACR/NEMA 300 vào năm 1985. Phiên bản thứ hai được phát hành vào năm 1988, phiên bản này được các nhà cung cấp ưa chuộng hơn, nhưng ngay sau đó người ta nhận ra rằng phiên bản thứ hai cũng cần được cải tiến. Phiên bản thứ 3 của tiêu chuẩn được phát hành vào năm 1993 với tên gọi "DICOM". 3.0 vẫn là phiên bản mới nhất nhưng nó đã được cập nhật liên tục từ năm 1993.

## Định dạng tệp DICOM ##

DICOM là sự kết hợp giữa định nghĩa định dạng tệp và giao thức truyền thông mạng. DICOM sử dụng phần mở rộng .DCM. .DCM tồn tại ở hai định dạng khác nhau, tức là định dạng 1.x và định dạng 2.x. Định dạng DCM 1.x hiện có thêm hai phiên bản bình thường và mở rộng. Các giao thức HTTP và HTTPS được sử dụng cho các dịch vụ web của DICOM.

### Tiêu đề tệp ###

Tiêu đề tệp chứa Phần mở đầu tệp 128 byte và tiền tố DICOM 4 byte.

**Lời mở đầu # 128 byte**|**Tiền tố # 4 byte “D, I, C, M**

**Lời mở đầu** được sử dụng để truy cập hình ảnh và dữ liệu khác trong tệp DICOM cung cấp khả năng tương thích với các định dạng tệp hình ảnh thường được sử dụng.

**Prefix** chứa chuỗi "DICM" dưới dạng ký tự viết hoa.

### Tập dữ liệu ###

Mỗi tệp phải chứa một bộ dữ liệu duy nhất đại diện cho phiên bản SOP và Lớp SOP với IOD liên quan. Tập dữ liệu là đại diện của thông tin thế giới thực. Tập dữ liệu chứa các phần tử dữ liệu và phần tử dữ liệu chứa các giá trị thuộc tính của đối tượng đó. Cấu trúc của các thuộc tính được chỉ định trong IOD. Một đối tượng dữ liệu DICOM bao gồm một số thuộc tính, bao gồm các mục như tên, ID, v.v., và cũng có một thuộc tính đặc biệt chứa dữ liệu pixel hình ảnh.

### Thành phần dữ liệu ###

Phần tử dữ liệu bao gồm Thẻ phần tử dữ liệu, Độ dài giá trị và giá trị cho Phần tử dữ liệu. Có 5 loại phần tử Dữ liệu là Phần tử dữ liệu bắt buộc loại 1, Phần tử dữ liệu có điều kiện loại 1C, Phần tử dữ liệu bắt buộc loại 2, Phần tử dữ liệu có điều kiện loại 2C và Phần tử dữ liệu tùy chọn loại 3. Ba loại cấu trúc phần tử dữ liệu cơ bản như sau.

**Phần tử dữ liệu có VR rõ ràng**

|Số nhóm|Số phần tử|Đại diện giá trị|Dành riêng|Độ dài giá trị|Trường giá trị
---|---|---|---|---|---|
|2 byte|2 byte|2 byte|2 byte # 0x00, 0x00|4 byte|"Bytes độ dài giá trị"

**Phần tử dữ liệu có VR rõ ràng**

|Số nhóm|Số phần tử|Đại diện giá trị|Độ dài giá trị|Trường giá trị
---|---|---|---|---|
|2 byte|2 byte|2 byte|2 byte|"Bytes độ dài giá trị"

**Phần tử dữ liệu có VR ẩn**


|Số nhóm|Số phần tử|Độ dài giá trị|Trường giá trị
---|---|---|---|
|2 byte|2 byte|4 byte|"Bytes độ dài giá trị"

1. **Thẻ phần tử dữ liệu**: Một số nguyên được sắp xếp đại diện cho số nhóm và số phần tử
1. **Đại diện giá trị VR**: VR là một chuỗi ký tự đại diện cho VR của Phần tử dữ liệu.
1. **Độ dài giá trị**: là số nguyên không dấu biểu thị độ dài rõ ràng của trường giá trị.
1. **Trường giá trị**: Mô tả giá trị của các phần tử dữ liệu.

## Cú pháp chuyển ##

Cú pháp truyền là một tập hợp các quy tắc để mã hóa nhằm thể hiện rõ ràng các cú pháp trừu tượng hơn. Với sự trợ giúp của cú pháp truyền tải, các thực thể giao tiếp đàm phán về các kỹ thuật mã hóa phổ biến mà chúng hỗ trợ.

## SOP ##

Sự kết hợp của IOD và DIMSE định nghĩa một Lớp SOP. Định nghĩa Lớp SOP chứa các quy tắc và ngữ nghĩa có thể hạn chế việc sử dụng các dịch vụ trong Nhóm Dịch vụ DIMSE hoặc Thuộc tính của IOD. Ví dụ về các Thành phần Dịch vụ là Lưu trữ, Nhận, Tìm, Di chuyển, v.v. Ví dụ về Đối tượng là hình ảnh CT, hình ảnh MR, nhưng cũng bao gồm danh sách lịch trình, hàng đợi in, v.v.

## Dịch vụ ##

DICOM cung cấp nhiều dịch vụ khác nhau, chủ yếu liên quan đến truyền thông dữ liệu. Mỗi cái được mô tả ngắn gọn dưới đây:


**Lưu trữ:** Dịch vụ DICOM Store gửi hình ảnh hoặc các đối tượng khác đến hệ thống liên lạc và lưu trữ ảnh (PACS) hoặc máy chủ.


**Cam kết lưu trữ:** Dịch vụ cam kết lưu trữ được sử dụng để xác nhận rằng một hình ảnh đã được lưu trữ vĩnh viễn trên một thiết bị trên bất kỳ loại phương tiện nào.


**Truy vấn/truy xuất:** Dịch vụ này cho phép máy trạm tìm danh sách hình ảnh hoặc các đối tượng khác rồi truy xuất chúng từ PACS.


**Danh sách công việc theo phương thức:** Dịch vụ danh sách công việc theo phương thức cung cấp danh sách các quy trình hình ảnh đã được lên lịch để thực hiện bởi một thiết bị thu nhận hình ảnh.


**In:** Dịch vụ này gửi hình ảnh tới máy in.

## Số cổng qua IP ##

DICOM sử dụng các cổng TCP và UDP sau:

1. 104
1.2761
1.2762
1.11112

## Người giới thiệu ##

* [https://vi.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

