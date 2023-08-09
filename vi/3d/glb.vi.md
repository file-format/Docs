{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","tệp", "định dạng", "loại tệp", "phần mở rộng","tệp GLB là gì?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Tìm hiểu về định dạng tệp GLB và API có thể mở và tạo tệp GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Tệp GLB là gì?

GLB là biểu diễn định dạng tệp nhị phân của các mô hình 3D được lưu ở Định dạng Truyền GL ([glTF](/vi/3d/gltf/)). Thông tin về các mô hình 3D như phân cấp nút, máy ảnh, vật liệu, hoạt ảnh và mắt lưới ở định dạng nhị phân. Định dạng nhị phân này lưu trữ nội dung glTF (JSON, .bin và hình ảnh) trong đốm màu nhị phân. Nó cũng tránh được vấn đề tăng kích thước tệp xảy ra trong trường hợp glTF. Định dạng tệp GLB dẫn đến kích thước tệp nhỏ gọn, tải nhanh, thể hiện cảnh 3D hoàn chỉnh và khả năng mở rộng để phát triển thêm. Định dạng sử dụng model/gltf-binary làm loại MIME.

## Định dạng tệp GLB - Thông tin khác

Các phương pháp phân phối nội dung được sử dụng bởi glTF dẫn đến xử lý bổ sung để giải mã dữ liệu nhị phân được mã hóa cơ sở 64 và cũng làm tăng kích thước tệp lên 33%. Các phương thức phân phối này đã góp phần hình thành định dạng tệp GLB, bao gồm:

* glTF JSON trỏ đến dữ liệu nhị phân bên ngoài (hình học, khung hình chính, giao diện) và hình ảnh.
* glTF JSON nhúng dữ liệu nhị phân được mã hóa base64 và hình ảnh nội tuyến bằng cách sử dụng URI dữ liệu.

GLB dưới dạng định dạng vùng chứa đã được giới thiệu dưới dạng định dạng tệp nhị phân để biểu thị nội dung glTF ở dạng đốm màu nhị phân nhằm tránh các sự cố do glTF gây ra. Định dạng tệp GLB [thông số kỹ thuật](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) nên được giới thiệu cho mọi triển khai trình đọc/ghi tương tự để phát triển ứng dụng .

## Cấu trúc tệp GLB

Định dạng tệp GLB dựa trên little endian và cấu trúc của nó cho thấy nó chứa:

* Phần mở đầu 12 byte, có tên là tiêu đề.
* Một hoặc nhiều đoạn chứa nội dung JSON và dữ liệu nhị phân.

#### Tiêu đề GLB

Tiêu đề định dạng tệp GLB bao gồm ba mục nhập 4 byte:

* phép thuật uint32 - phép thuật bằng 0x46546C67. Đó là glTF chuỗi ASCII và có thể được sử dụng để xác định dữ liệu là glTF nhị phân
* phiên bản uint32 - cho biết phiên bản của định dạng vùng chứa Binary glTF
* chiều dài uin32 - tổng chiều dài của glTF nhị phân, bao gồm Tiêu đề và tất cả các khối theo byte

#### Miếng, mảnh nhỏ

Mỗi đoạn trong tệp GLB có cấu trúc như sau:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - độ dài của chunkData theo byte
* `chunkType` - chỉ ra loại chunk
* `chunkData` - tải trọng nhị phân của chunk

trong đó các loại chunk là:

|# |Loại khối|ASCII|Mô tả|Số lần xuất hiện
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Nội dung JSON có cấu trúc|1
|2.|0x004E4942|BIN|Bộ đệm nhị phân|0 hoặc 1

Phần đầu và phần cuối của mỗi đoạn phải được căn chỉnh theo ranh giới 4 byte và nên sử dụng phần đệm cho mục đích này.

##### Nội dung JSON có cấu trúc

Đây phải là đoạn đầu tiên của nội dung glTF nhị phân và cho phép triển khai truy xuất dần các tài nguyên từ các đoạn tiếp theo. Điều này cũng cung cấp khả năng chỉ đọc một tập hợp con tài nguyên đã chọn từ nội dung glTF nhị phân, chẳng hạn như LOD thô nhất của lưới. Để đáp ứng các yêu cầu căn chỉnh, đoạn này phải được đệm bằng các ký tự Dấu cách ở cuối (0x20).

##### Bộ đệm nhị phân #####

Đoạn này chứa tải trọng nhị phân cho hình học, khung hình chính hoạt ảnh, giao diện và hình ảnh. Nó phải là đoạn thứ hai của nội dung glTF nhị phân và phải được đệm bằng các số 0 ở cuối (0x00) để đáp ứng các yêu cầu căn chỉnh.

## Người giới thiệu ##

* [Thông số kỹ thuật định dạng tệp GLB - Khronos](/vi/3D/GLTF/)

