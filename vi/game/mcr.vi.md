{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tìm hiểu về định dạng tệp MCR và các API có thể tạo và mở tệp MCR.",
  "title": "MCR - Định dạng tệp vùng Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-vir"
}
},
  "lastmod": "2022-12-14"
}

## Một tập tin MCR là gì?

Định dạng tệp Minecraft MCR là định dạng dữ liệu được Minecraft sử dụng để lưu trữ các phần địa hình của Thế giới Minecraft. Nó dựa trên định dạng NBT (Thẻ nhị phân được đặt tên), được phát triển bởi các nhà phát triển công cụ trò chơi nguồn mở phổ biến, Minecraft Forge. Loại tệp MCR đã được giới thiệu ngay từ đầu và sau đó được thay thế bằng [MCA file format](/game/mca/).

## Định dạng tệp MCR

Định dạng tệp MCR được cấu trúc dưới dạng một chuỗi các thẻ nhị phân được đặt tên, mỗi thẻ chứa một loại dữ liệu cụ thể. Thẻ cấp cao nhất là thẻ Cấp độ, chứa tất cả dữ liệu cho một cấp độ trò chơi. Trong thẻ Cấp độ, có một số thẻ được đặt tên khác lưu trữ các loại dữ liệu khác nhau, chẳng hạn như thẻ Dữ liệu, lưu trữ thông tin về thế giới trò chơi và thẻ Thực thể và TileEntities, lưu trữ dữ liệu về đối tượng trò chơi và thực thể ô tương ứng trên thế giới.

## Định dạng tệp MCR bên trong có gì?

Ở định dạng tệp Minecraft MCR, vùng là khu vực khối 32x32 của thế giới trò chơi. Định dạng MCR chia thế giới trò chơi thành các khu vực để quản lý dữ liệu hiệu quả hơn và cho phép tải và lưu các cấp độ trò chơi nhanh hơn. Mỗi khu vực được lưu trữ trong một tệp riêng biệt và định dạng tệp MCR sử dụng hệ thống tọa độ để xác định vị trí của từng khu vực trong thế giới trò chơi. Tọa độ của một vùng được xác định bởi tọa độ khối ở góc dưới bên trái của vùng. Ví dụ: một vùng có tọa độ (-1,0) sẽ nằm ở một vùng ở bên trái và các vùng bằng 0 tính từ điểm gốc của thế giới trò chơi.

## Thông số định dạng tệp MCR

Thông số định dạng tệp MCR được cung cấp công khai. Thông số kỹ thuật cho định dạng NBT, dựa trên định dạng MCR, có sẵn trên trang web Minecraft Forge. Ngoài ra, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) còn có thông tin chi tiết về định dạng tệp MCR, bao gồm cấu trúc của nó và các loại dữ liệu khác nhau mà nó hỗ trợ.

### Dữ liệu nén trong tệp MCR

Định dạng tệp Minecraft MCR hỗ trợ nén. Định dạng tệp MCR dựa trên [NBT format](https://minecraft.fandom.com/wiki/NBT_format) cho phép dữ liệu được lưu trữ ở dạng nén. Điều này giúp giảm kích thước của tệp MCR và giúp việc truyền và lưu trữ chúng hiệu quả hơn. Đây là một tính năng quan trọng của định dạng tệp MCR, vì nó cho phép người chơi chia sẻ dữ liệu địa hình Thế giới Minecraft lớn với người khác.

## Người giới thiệu

* [Trình chỉnh sửa thế giới cho Minecraft](https://www.mcedit.net/)

* [Giới thiệu về Minecraft](https://www.minecraft.net/)

* [Định dạng tệp khu vực](https://minecraft.fandom.com/wiki/Region_file_format)

* [Định dạng NBT](https://minecraft.fandom.com/wiki/NBT_format)


