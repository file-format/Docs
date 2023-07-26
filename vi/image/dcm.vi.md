{
  "date" : "2019-10-11",
  "keywords" :[ "tệp dcm", "định dạng tệp dcm", "tệp dcm là gì", "tệp", "ví dụ dcm", "phần mở rộng tệp dcm","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp DCM - Tệp thông tin y tế kỹ thuật số",
  "description":"Tìm hiểu về định dạng tệp DCM và API có thể tạo và mở tệp DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Tệp DCM là gì?

Các tệp có phần mở rộng .dcm đại diện cho hình ảnh kỹ thuật số lưu trữ thông tin y tế của bệnh nhân như ảnh chụp cộng hưởng từ (MRI), ảnh chụp CT và ảnh siêu âm. Các tệp DCM sử dụng định dạng tệp hình ảnh [DICOM](/vi/image/dicom/) (Hình ảnh kỹ thuật số và Truyền thông trong Y học) và có thể bao gồm thông tin của bệnh nhân để tham khảo. Nó được phát triển bởi [Hiệp hội các nhà sản xuất điện quốc gia](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) và nhằm chuẩn hóa định dạng tệp hình ảnh để phân phối và xem hình ảnh y tế.

## Định dạng tệp DCM

Các tệp DCM lưu trữ thông tin ở định dạng hình ảnh DICOM. Các tệp này lưu trữ Tập dữ liệu, là thông tin trong thế giới thực, đại diện cho một phiên bản SOP liên quan đến DICOM IOD. Thông tin meta tệp DICOM được lưu trữ trong tệp theo sau là luồng byte của tập dữ liệu thực tế.

### Thông tin siêu tệp DICOM ##

Mỗi tệp DICOM bao gồm một tiêu đề thông tin nhận dạng cho tập dữ liệu được đóng gói bao gồm:
* Phần mở đầu tệp 128 byte
* Tiền tố DICOM 4 byte
* Phần tử tệp Meta

Tiêu đề này là bắt buộc đối với mọi tệp DICOM.

### Phần tử meta tệp ###
|Tên thuộc tính|Thẻ|Loại| Mô tả thuộc tính
---|---|---|---|
|Phần mở đầu của tệp|Không có trường thẻ hoặc độ dài|1|Một trường 128 byte cố định có sẵn cho Hồ sơ ứng dụng hoặc sử dụng được chỉ định triển khai. Nếu không được sử dụng bởi Hồ sơ ứng dụng hoặc triển khai cụ thể, tất cả các byte sẽ được đặt thành 00H. Trình đọc hoặc Trình cập nhật tập hợp tệp sẽ không dựa vào nội dung của Lời mở đầu này để xác định rằng Tệp này có phải là Tệp DICOM hay không.
|Tiền tố DICOM|Không có trường thẻ hoặc độ dài|1|Bốn byte chứa chuỗi ký tự "DICM". Tiền tố này nhằm mục đích sử dụng để nhận biết rằng Tệp này có phải là Tệp DICOM hay không.
|Độ dài nhóm thông tin meta tệp|(0002,0000)|1|Số byte theo sau Phần tử meta tệp này (cuối trường Giá trị) cho đến và bao gồm cả Phần tử meta tệp cuối cùng của Thông tin meta tệp nhóm 2
|Phiên bản thông tin siêu tệp|(0002,0001)|1|Đây là trường hai byte trong đó mỗi bit xác định một phiên bản của tiêu đề Thông tin siêu tệp này. Trong phiên bản 1, giá trị byte đầu tiên là 00H và giá trị byte giá trị thứ hai là 01H. Việc triển khai đọc Tệp có Thông tin Siêu dữ liệu trong đó thuộc tính này có bit 0 (lsb) của byte thứ hai được đặt thành 1 có thể diễn giải Thông tin Siêu tệp như được chỉ định trong phần này phiên bản PS3.10. Tất cả các bit khác sẽ không được kiểm tra.
|UID Lớp SOP Lưu trữ Phương tiện|(0002,0002)|1|Xác định duy nhất Lớp SOP được liên kết với Tập dữ liệu. Các UID lớp SOP được phép lưu trữ phương tiện được chỉ định trong PS3.4 - Cấu hình ứng dụng lưu trữ phương tiện.
|UID Phiên bản SOP lưu trữ phương tiện|(0002,0003)|1|Xác định duy nhất Phiên bản SOP được liên kết với Tập dữ liệu được đặt trong tệp và tuân theo Thông tin meta tệp.
|Cú pháp truyền UID|(0002,0010)|1|Nhận dạng duy nhất Cú pháp truyền được sử dụng để mã hóa Tập dữ liệu sau. Cú pháp chuyển này không áp dụng cho Thông tin Meta tệp.
|UID lớp triển khai|(0002,0012)|1|Xác định duy nhất việc triển khai đã viết tệp này và nội dung của nó. Nó cung cấp một nhận dạng rõ ràng về kiểu triển khai đã ghi tệp lần cuối trong trường hợp có sự cố trao đổi.
|Tên Phiên bản Triển khai|(0002,0013)|3|Xác định phiên bản cho UID Lớp Triển khai (0002,0012) bằng cách sử dụng tối đa 16 ký tự của danh mục.
|Tiêu đề Thực thể Ứng dụng Nguồn|(0002,0016)|3|Tiêu đề Thực thể Ứng dụng DICOM (AE) của AE đã viết nội dung của tệp này (hoặc cập nhật lần cuối). Nếu được sử dụng, nó cho phép truy tìm nguồn lỗi trong trường hợp xảy ra sự cố trao đổi phương tiện.
|UID của người tạo thông tin cá nhân|(0002,0100)|3|UID của người tạo thông tin cá nhân (0002,0102).
|Thông tin Riêng tư|(0002,0102)|1C|Chứa Thông tin Riêng tư được đặt trong Thông tin Meta Tệp. Người tạo sẽ được xác định trong (0002,0100). Bắt buộc nếu có UID của Trình tạo thông tin cá nhân (0002,0100).

### Đóng gói tập dữ liệu ###

Tệp DICOM chứa một Tập dữ liệu duy nhất đại diện cho một Phiên bản SOP duy nhất liên quan đến một Lớp SOP duy nhất. Cú pháp truyền UID của Thông tin meta tệp DICOM sẽ xác định Cú pháp truyền được sử dụng để mã hóa Tập dữ liệu.

### Hỗ trợ thông tin quản lý tệp ###

Lớp định dạng phương tiện cung cấp Thông tin quản lý tệp sau đây nếu cần thiết cho một Hồ sơ ứng dụng DICOM nhất định.

* Nhận dạng chủ sở hữu nội dung tệp

* Thống kê truy cập tệp (ví dụ: ngày và thời gian tạo)

* Kiểm soát truy cập tệp ứng dụng

* Kiểm soát truy cập phương tiện vật lý (ví dụ: bảo vệ ghi)

## Người giới thiệu ##
* [Tiêu chuẩn DICOM](https://www.dicomstandard.org/current/)
* [Định dạng tệp DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

