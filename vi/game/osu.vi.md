{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp OSU và các API có thể tạo và mở tệp OSU.",
  "title" : "Tệp OSU - Osu! Định dạng tệp tập lệnh",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-vi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Tập tin OSU là gì?

Tệp OSU là tập lệnh trò chơi được viết cho osu! trò chơi nhịp điệu. Nó chứa thông tin về beatmap được sử dụng trong trò chơi, chẳng hạn như mức độ khó, bài hát sẽ được phát và thời gian của các đối tượng đánh mà người chơi phải đồng bộ hóa với âm nhạc. Nó cho phép người chơi trò chơi nhịp điệu phát triển các thử thách tùy chỉnh và chia sẻ với cộng đồng trò chơi.

**Loại MIME của định dạng tệp OSR:** x-osu-beatmap

## Định dạng tệp OSU

Các tệp OSU được lưu dưới dạng tệp văn bản thuần túy vào đĩa và cấu trúc của nó được xác định rất rõ ràng trong [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) bởi osu!.

### Các phần trong Tệp OSU

Một tệp OSU điển hình có các phần sau.

|Phần |Mô tả |Loại nội dung|
---|---|---|
|[Chung]| Thông tin chung về beatmap| khóa: cặp giá trị|
|[Biên tập viên]| Cài đặt đã lưu cho trình chỉnh sửa beatmap| khóa: cặp giá trị|
|[Siêu dữ liệu] |Thông tin dùng để xác định beatmap| khóa:cặp giá trị|
|[Độ khó] |Cài đặt độ khó| khóa:cặp giá trị|
|[Sự kiện]| Sự kiện đồ họa Beatmap và storyboard | Danh sách được phân tách bằng dấu phẩy|
|[Điểm tính thời gian]| Điểm kiểm soát và thời gian| Danh sách được phân tách bằng dấu phẩy|
|[Màu sắc]| Combo và màu da| khóa : cặp giá trị|
|[HitObjects]| Đánh đồ vật| Danh sách được phân tách bằng dấu phẩy|

## Người giới thiệu

* [OSU! Trò chơi nhịp điệu](https://osu.ppy.sh/home)

* [Định dạng tệp OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


