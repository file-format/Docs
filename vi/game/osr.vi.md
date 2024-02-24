{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp OSR và các API có thể tạo và mở tệp OSR.",
  "title" : "Tệp OSR - osu! Phát lại định dạng tệp",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-vi",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Tập tin OSR là gì?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**Loại MIME của định dạng tệp OSR:** x-osu-replay

## Định dạng tệp OSR

Các tệp OSR được lưu dưới dạng tệp nhị phân với các trường dữ liệu có độ dài cố định cũng như thay đổi.

|Loại dữ liệu| Định dạng|
---|---|
|Byte |Chế độ chơi lại của trò chơi (0 = osu! Tiêu chuẩn, 1 = Taiko, 2 = Bắt nhịp, 3 = osu!mania)|
|Số nguyên |Phiên bản của trò chơi khi tạo bản phát lại (ví dụ: 20131216)|
|Chuỗi |osu! beatmap MD5 băm |
|Chuỗi| Tên người chơi|
|Chuỗi| ôi! phát lại hàm băm MD5 (bao gồm một số thuộc tính nhất định của phát lại)|
|Ngắn| Số 300 |
|Ngắn| Số 100 ở tiêu chuẩn, 150 ở Taiko, 100 ở CTB, 100 ở hưng cảm|
|Ngắn| Số 50 ở tiêu chuẩn, quả nhỏ ở CTB, 50 ở hưng cảm|
|Ngắn| Số lượng Geki tiêu chuẩn, tối đa 300 Geki trong cơn hưng cảm|
|Ngắn| Số lượng Katus tiêu chuẩn, 200 trong hưng cảm|
|Ngắn| Số lần bỏ lỡ|
|Số nguyên| Tổng số điểm hiển thị trên báo cáo điểm|
|Ngắn| Combo tuyệt vời nhất được hiển thị trên báo cáo điểm số|
|Byte| Sự kết hợp hoàn hảo/đầy đủ (1 = không trượt, không ngắt thanh trượt và không có thanh trượt hoàn thành sớm)|
|Số nguyên| Các mod đã được sử dụng. Xem bên dưới để biết danh sách các giá trị mod.|
|Chuỗi| Biểu đồ thanh cuộc sống: các cặp u/v được phân tách bằng dấu phẩy, trong đó u là thời gian tính bằng mili giây của bài hát và v là giá trị dấu phẩy động từ 0 - 1 biểu thị lượng thời gian bạn có tại thời điểm nhất định (0 = thanh cuộc sống là trống, 1= thanh cuộc sống đã đầy)|
|Dài| Dấu thời gian (tích tắc Windows)|
|Số nguyên| Độ dài tính bằng byte của dữ liệu phát lại đã nén|
|Byte |Array Dữ liệu phát lại được nén|
|Dài| ID điểm trực tuyến|
|Đôi| Thông tin mod bổ sung. Chỉ hiển thị nếu Target Practice được bật.|

## Người giới thiệu

* [OSU! Trò chơi nhịp điệu](https://osu.ppy.sh/home)

* [Định dạng tệp OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


