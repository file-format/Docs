{
  "date" : "2019-10-11",
  "keywords" :[ "tệp osm", "tệp osm là gì", "tệp", "ví dụ osm", "phần mở rộng tệp osm","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Định dạng tệp OpenStreetMap",
  "description":"Tìm hiểu về định dạng tệp OSM và API có thể tạo và mở tệp OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp OSM là gì?

OpenStreetMap (OSM) là một tập hợp khổng lồ các kho lưu trữ thông tin địa lý tự nguyện trong các loại tệp khác nhau, sử dụng các lược đồ mã hóa khác nhau để chuyển đổi dữ liệu này thành bit và byte. OSM là một nỗ lực hợp tác hướng tới việc tạo ra một bản đồ thế giới có thể chỉnh sửa miễn phí. Đầu ra chính của nỗ lực hợp tác này là dữ liệu địa lý chứ không phải bản đồ. Các hạn chế về việc sử dụng hoặc tính sẵn có của thông tin địa lý trên khắp thế giới gây ra nhu cầu tạo một OSM. Dữ liệu có sẵn từ OSM đã sẵn sàng để thay thế Google Maps cho các ứng dụng cổ điển (Facebook, Craigslist, v.v.) và dữ liệu mặc định cho các ứng dụng của máy thu GPS.^^ ^^Mặc dù chất lượng dữ liệu rất đa dạng trên toàn thế giới nhưng dữ liệu OpenStreetMap có thể được so sánh thuận tiện với bằng sáng chế nguồn dữ liệu.

## Lược Sử ##

Lấy cảm hứng từ sự thành công của Wikipedia, vào năm 2004, Steve Coast, một doanh nhân người Anh, đã tạo ra dự án lập bản đồ thế giới dựa vào cộng đồng này ở Vương quốc Anh. Ban đầu, ông tập trung vào việc lập bản đồ Vương quốc Anh. OpenStreetMap Foundation lần đầu tiên được thành lập vào tháng 4 năm 2006 để hỗ trợ quá trình phát triển, mở rộng và lưu hành không gian địa lý miễn phí cho bất kỳ ai. Vào tháng 12 năm 2006, Yahoo đã hỗ trợ OpenStreetMap chụp ảnh trên không để sản xuất bản đồ. Dữ liệu đường hoàn chỉnh cho Hà Lan và dữ liệu đường chính cho Ấn Độ và Trung Quốc đã được đóng góp cho OSM vào tháng 4 năm 2007 bởi Dữ liệu Điều hướng Ô tô (AND). Vào tháng 12 năm 2007, Đại học Oxford là tổ chức nổi bật nhất đã tích hợp dữ liệu OpenStreetMap trong trang web chính của họ. Kể từ đó, hơn 2 triệu người dùng đã đăng ký đóng góp dữ liệu cho dự án này bằng thiết bị GPS, chụp ảnh trên không và khảo sát thủ công. Dữ liệu do cộng đồng đóng góp này được cung cấp theo Giấy phép Cơ sở dữ liệu Mở. Tổ chức phi lợi nhuận OpenStreetMap Foundation đã đăng ký ở Anh duy trì trang web OSM.

## Định dạng tệp OSM ##

Có rất nhiều cách và định dạng tệp để lưu trữ dữ liệu địa lý nhưng định dạng tệp **OSM** bị hạn chế đối với OpenStreetMap. OSM là định dạng tiêu chuẩn được thiết kế đặc biệt nhằm mục đích vận chuyển dễ dàng qua internet. Định dạng được sắp xếp có cấu trúc, được mã hóa bằng XML tạo thành tệp .osm. Trong OpenStreetMap có bốn yếu tố trục để lưu trữ cấu trúc dữ liệu cấu trúc liên kết:

{{< figure src="../OSM.png" alt="Định dạng tệp OSM" >}}


|Nút|Cách|Mối quan hệ|Thẻ
---|---|---|---|
|<ul><li> Thể hiện vị trí địa lý được lưu trữ dưới dạng các cặp vĩ độ và kinh độ.</li><li> Được sử dụng để thể hiện các tính năng bản đồ không có kích thước, chẳng hạn như các đỉnh núi.</li></ul> |<ul><li> Danh sách các nút được sắp xếp, biểu thị một đa tuyến hoặc đa giác</li><li> Biểu thị các đối tượng tuyến tính như đường và sông cũng như các khu vực như khu vực đỗ xe, rừng rậm và công viên.</li></ul> |<ul><li> Danh sách các nút và đường được sắp xếp thể hiện mối quan hệ của chúng như rào cản và ngã rẽ trên đường, đường cao tốc trải qua các đường hiện có khác nhau và các khu vực có lỗ hổng.</li></ul> |<ul><li> Lưu trữ siêu dữ liệu về các đối tượng bản đồ.* Luôn được đính kèm với bất kỳ nút, đường hoặc mối quan hệ nào</li></ul>


Các thẻ được sử dụng để mô tả các đặc điểm vật lý trên mặt đất (tòa nhà và đường, v.v.) trong OpenStreetMap. Mỗi thẻ liên quan đến một đặc điểm địa lý của tính năng được đại diện bởi nút hoặc mối quan hệ cụ thể đó. Trong hệ thống gắn thẻ miễn phí này, để mô tả một đối tượng địa lý, có thể đưa vào bản đồ số lượng thuộc tính không giới hạn. Các kết hợp khóa và giá trị cụ thể được xác nhận bởi người dùng đã đăng ký đóng vai trò là tiêu chuẩn không chính thức cho các thẻ được sử dụng thường xuyên. Tuy nhiên, các thẻ mới có thể được tạo bất cứ khi nào các khía cạnh mới yêu cầu phân tích các thuộc tính chưa được ánh xạ trước đây của các đối tượng địa lý. Hầu hết các tính năng chỉ sử dụng một số lượng nhỏ các thẻ để mô tả.

Ba loại tệp được OSM sử dụng để lưu trữ dữ liệu chính của nó.

OSM xử lý tất cả các tệp này với thông tin về chi tiết định dạng của chúng. Nhưng các đối tượng bên trong giống nhau được tạo ra bởi các tệp này. Đối với các tệp dữ liệu, cờ hiển thị trên các đối tượng OSM luôn đúng, điều này không đúng đối với các tệp lịch sử và tệp thay đổi.

Trong sử dụng phổ biến, có nhiều định dạng tệp OSM. Các định dạng tệp xác định mã hóa nội dung trên đĩa hoặc dây theo bit và byte. OSM có khả năng đọc và ghi tối đa các định dạng này.

**XML**

Định dạng OSM ban đầu dựa trên XML. Dữ liệu trả về của API cơ sở dữ liệu OSM chính ở định dạng XML.

**PBF**

Mã hóa Bộ đệm giao thức đứng trên định dạng nhị phân và là một trong những định dạng nhỏ gọn nhất.

**O5M/O5C**

Định dạng nhị phân dựa trên định dạng đơn giản hơn nhưng tương đối ít được sử dụng. OSM có thể đọc nhưng không thể viết định dạng này.

**OPL**

Một định dạng đơn giản được đề xuất để sử dụng với các công cụ dòng lệnh UNIX tiêu chuẩn. Gần với tệp CSV, cho phép một thực thể OSM trên một dòng.

** GỠ LỖI **

Một định dạng dựa trên văn bản nhằm tạo ra để gỡ lỗi. OSM có thể viết định dạng này nhưng không đọc được.

**HỐ ĐEN**

Một định dạng giả loại bỏ tất cả dữ liệu. OSM có thể ghi định dạng này nhưng không đọc được.

## Lưu trữ dữ liệu OSM ##

Cơ sở dữ liệu **PostgreSQL** chính của OSM giữ bản sao chính của dữ liệu OSM với phần mở rộng PostGIS. Đối với mỗi dữ liệu nguyên thủy, cơ sở dữ liệu chính duy trì một bảng có các hàng lưu trữ các đối tượng riêng lẻ. Tất cả các chỉnh sửa cập nhật cơ sở dữ liệu này và tất cả các định dạng khác được hình thành bằng cơ sở dữ liệu này. Nhiều nhóm cơ sở dữ liệu có thể tải xuống được tạo để truyền dữ liệu từ nơi này sang nơi khác. Hai định dạng, một sử dụng XML và định dạng khác sử dụng Định dạng nhị phân bộ đệm giao thức (PBF) xác định các nhóm này. Toàn bộ dữ liệu được lưu trữ trong một tệp có tên là hành tinh.osm

## Nén trong Tệp OSM ##

Các định dạng dựa trên văn bản (XML, OPL và Gỡ lỗi) sử dụng tùy chọn nén gzip hoặc bzip2.

## Người giới thiệu ##

* [Hướng dẫn định dạng tệp OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Tìm hiểu OSM](https://learnosm.org/en/osm-data/getting-data/)

