{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp FIT- Tệp hoạt động của Garmin",
  "description":"Tìm hiểu về định dạng tệp FIT và các API có thể tạo và mở tệp FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Tệp FIT là gì?

Tệp FIT là tệp GIS được tạo bởi các thiết bị đeo thể thao của Garmin. Nó được sử dụng để ghi lại các hoạt động của người đó khi họ di chuyển khi đeo các thiết bị này. Dữ liệu hoạt động bao gồm vị trí và thời gian được thiết bị GPS ghi lại. Các tệp FIT cũng được sử dụng để chuyển dữ liệu hoạt động được ghi lại bằng API web. Đó là lý do tệp FIT là định dạng tệp được sử dụng phổ biến nhất để chia sẻ dữ liệu thể dục với các nền tảng thể dục khác. Các định dạng tệp phổ biến khác bao gồm [GPX](/vi/gis/gpx/), TCX và [KML](/vi/gis/kml/).

## Định dạng tệp FIT - Thông tin khác

Các tệp FIT được lưu vào đĩa dưới dạng tệp nhị phân với thông tin được thiết bị Garmin ghi lại cho hoạt động. Thông tin được lưu trữ bên trong tệp FIT bao gồm:

* Ngày giờ
* Các loại thể thao
* Lập & tách dữ liệu
* Theo dõi GPS
* Dữ liệu cảm biến
* Sự kiện cho phiên hoạt động

Dữ liệu hoạt động có thể được ghi vào tệp theo thời gian thực hoặc được xuất sau khi quá trình ghi hoạt động hoàn tất.

### Tin nhắn Hoạt động FIT

Tệp hoạt động FIT có thể bao gồm một số loại thông báo bắt buộc. Sau đây là các thông báo cần thiết cho một tệp hoạt động.

|Thông điệp|Mục đích|
---|---|
|Id tập tin| Thông báo Id tệp được yêu cầu bởi tất cả các loại tệp FIT và phải là thông báo đầu tiên trong tệp. Đối với các tệp Hoạt động, thuộc tính Loại phải được đặt thành 4.|
|Hoạt động| Một thông báo Hoạt động duy nhất được yêu cầu trong tệp Hoạt động FIT. Bao gồm trong thông báo Hoạt động là các thuộc tính Dấu thời gian cục bộ và Số phiên. Dấu thời gian cục bộ được sử dụng để xác định độ lệch múi giờ có thể được áp dụng cho tất cả các dấu thời gian trong tệp. Hầu hết các thiết bị ghi tệp FIT trong thời gian thực và số lượng phiên sẽ không xác định cho đến khi kết thúc quá trình ghi. Do đó, thông báo Hoạt động thường sẽ là thông báo cuối cùng trong tệp.|
|Phiên| Các tệp hoạt động sẽ chứa một hoặc nhiều thông báo Phiên. Thông báo Phiên là loại thông báo Tóm tắt. Thời gian bắt đầu, Tổng thời gian đã trôi qua, Tổng thời gian hẹn giờ và Dấu thời gian là các trường bắt buộc đối với tất cả các thông báo tóm tắt.|
|Lập| Thông báo vòng chạy đại diện cho các vòng chạy hoặc khoảng thời gian trong phiên. Tin nhắn Vòng lặp là loại tin nhắn Tóm tắt. Thời gian bắt đầu, Tổng thời gian đã trôi qua, Tổng thời gian hẹn giờ và Dấu thời gian là các trường bắt buộc đối với tất cả các thông báo tóm tắt.|
|Bản ghi| Ghi lại tin nhắn bao gồm tọa độ GPS, tốc độ, khoảng cách, nhịp tim, sức mạnh, v.v.|

## Tệp FIT Tài nguyên hữu ích

* [Giải mã tệp hoạt động FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Mã hóa tệp hoạt động FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Người giới thiệu ##

* [Tệp hoạt động FIT](https://developer.garmin.com/fit/file-types/activity/)

