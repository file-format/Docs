{
  "date" : "2021-10-20",
  "keywords" :[ "tệp sfar", "định dạng tệp sfar", "tệp sfar là gì", "tệp", "ví dụ sfar", "Phần mở rộng tệp DLC của Mass Effect 3","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp SFAR của Mass Effect 3 và các API có thể tạo và mở tệp SFAR.",
  "title" :"SFAR - Tệp DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Tệp SFAR là gì?

Tệp có phần mở rộng .sfar là tệp dữ liệu trò chơi được Mass Effect 3 sử dụng để lưu trữ DLC (nội dung có thể tải xuống) của nó trong một kho lưu trữ nén, độc quyền. Mass Effect 3 là một trò chơi được tạo ra bởi Electronic Arts, một công ty phát triển trò chơi hàng đầu. Nội dung DLC được lưu trữ trong tệp SFAR được sử dụng để mở rộng trò chơi với nội dung và tính năng bổ sung.

## Định dạng tệp SFAR - Thông tin khác

Các tệp SFAR được lưu trữ/lưu dưới dạng tệp lưu trữ nén ở định dạng tệp nhị phân. Chúng sử dụng cả thuật toán nén LZX và LZMA để nén nội dung. Các tệp SFAR có thể được mở bằng Trình chỉnh sửa DLC đi kèm với ME3 Explorer. Ngoài SFAR, DLC Editor có thể trích xuất các tệp trò chơi khác như [PCC](/vi/game/pcc/).

## Thông số kỹ thuật định dạng tệp SFAR

Một tệp SFAR được chia thành bốn phần chính sau đây.

### Tiêu đề SFAR

Tiêu đề SFF chứa thông tin về các phần khác nhau bao gồm tệp.

### Bảng tệp SFAR

Bảng tệp SFAR chứa danh sách các mục nhập tệp trong đó mỗi mục nhập dài 30 byte.

### Bảng kích thước khối

Kích thước khối chứa nhiều mục, trong đó mỗi mục dài 2 byte. Giá trị này chỉ định Kích thước khối tương ứng với một mục trong Bảng tệp.

### Khối

Khối khối trong tệp SFAR chứa dữ liệu bên trong tệp SFAR.

## Người giới thiệu

* [Định dạng tệp DLC SFAR - Nghiên cứu](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

