{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MK3D",
  "keywords" :[ "mk3d", "matroska video", "định dạng mkv", "3d lập thể", "Chế độ âm thanh nổi", "video", "tệp", "định dạng" ],
  "description":"Tìm hiểu về định dạng tệp MK3D cho video 3d lập thể được tạo bởi Matroska và các API có thể tạo và mở tệp MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Tệp MK3D là gì? ##

Các tệp MK3D thuộc họ định dạng video Matroska. Các tệp này thực sự là **video 3d lập thể** được tạo bằng định dạng Matroska 3D. Bộ chứa tệp MKV sử dụng giá trị của trường Chế độ âm thanh nổi để xác định loại nội dung video 3D lập thể. Giá trị Chế độ âm thanh nổi cũng có sẵn để hiển thị các video 3D âm thanh nổi cũ bằng cách tách màu lục lam và đỏ (AnaGlyph)

## Chi tiết kỹ thuật ##
Các video 3D có thể được nén theo hai cách sau:

- Theo dõi riêng cho từng mắt.
- Kết hợp từng theo dõi mắt thành một bản nhạc duy nhất.

Bộ chứa tệp MKV hỗ trợ cả hai.

Đối với các video một rãnh dễ dàng hơn với vật liệu 3D bên trong chúng, bạn phải đặt trường **Chế độ âm thanh nổi** quyết định các mặt phẳng được lắp ráp trong rãnh kết hợp đơn hoặc trái phải. Bạn có thể sử dụng một trong các giá trị trường Chế độ âm thanh nổi sau:

|Giá trị | Mô tả |
|---|---|
|0| đơn |
|1| cạnh nhau (mắt trái trước)|
|2| trên-dưới (mắt phải trước)|
|3| trên-dưới (mắt trái trước)|
|4| bàn cờ (phải trước)|
|5| bàn cờ (trái là đầu tiên)|
|6| hàng xen kẽ (phải là đầu tiên)|
|7| hàng xen kẽ (trái là đầu tiên)|
|8| cột xen kẽ (bên phải là đầu tiên)|
|9| cột xen kẽ (bên trái là đầu tiên) |
|10| anaglyph (lục lam/đỏ)|
|11| cạnh nhau (mắt phải trước)|
|12| anaglyph (xanh lục/đỏ tươi)|
|13| cả hai mắt được nối vào một Khối (mắt trái là đầu tiên) (chế độ tuần tự trường)|
|14| cả hai mắt được nối vào một Khối (mắt phải là đầu tiên) (chế độ tuần tự trường)|

Đối với nhiều rãnh, bộ chứa MKV cần quyết định chức năng của từng rãnh riêng biệt. **TrackOperation** với **TrackCombinePlanes** được sử dụng để thực hiện công việc.


## Người giới thiệu ##

- [Ghi chú đặc điểm kỹ thuật Matroska](https://www.matroska.org/technical/notes.html)
- [Hỗ trợ bộ chứa tệp MKV cho video 3D âm thanh nổi và tệp MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

