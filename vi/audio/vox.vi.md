{
  "date" : "2021-08-11",
  "keywords" :[ "vox", "file", "extension", "format", "audio", "ADPCM", "Dialogic ADPCM", "Xentec VOX Studio","vox extension", "vox files"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp VOX và các API có thể tạo và mở tệp VOX.",
  "title" :"VOX - Định dạng tệp âm thanh",
  "linktitle" : "VOX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-11"
}

## Tệp VOX là gì? ##

Ở tốc độ lấy mẫu thấp, các tệp VOX được chỉ định để lưu trữ dữ liệu giọng nói được số hóa. Đây là những tệp âm thanh thường được sử dụng trong các ứng dụng được chỉ định cho liên lạc qua điện thoại. Loại định dạng tệp này sử dụng thuật toán nén mất dữ liệu có tối ưu hóa cho giọng nói.

Thường được sử dụng trong các ứng dụng giọng nói, các tệp VOX chứa các lời nhắc bằng giọng nói được ghi âm trước. Loại định dạng tệp này cũng được chuyển đổi thành các định dạng phổ biến khác. Chúng có thể được sử dụng trong hệ điều hành Windows và macOS.

Nó chủ yếu được sử dụng để ghi âm và nén giọng nói. Ở định dạng này, không thể lưu trữ dữ liệu đa âm vì nó chỉ hỗ trợ dữ liệu đồng âm.



## Lược Sử ##

Các tệp VOX được liên kết với Bảng phương tiện được gọi là DMV và JCT của Hộp thoại. Chúng thuộc về VoxWare và nhiều phần mềm khác. Nó từng được coi là một định dạng lỗi thời.

Là một định dạng lỗi thời, nó không được sử dụng sau đó. Tương tự như các định dạng ADPCM khác, nó được nén thành 4 bit. Các tính năng của các tệp này đủ gần với thông số kỹ thuật của tệp [WAV](/vi/audio/wav/).


## Thông số kỹ thuật định dạng ##

Loại định dạng tệp này tương thích với các chương trình HĐH Windows như Xentec Vox Studio. Nó có các tính năng cụ thể được sử dụng để kích thích lời nói của con người. Trò chơi điện tử chủ yếu sử dụng định dạng này. Phần mở rộng tệp VOX có tiêu đề 32 byte cùng với các chỉ mục và khung 10 byte. Dữ liệu giọng nói thực tế được lưu trong các khung ở dạng phân đoạn trong một tệp. Có một dạng khác nhau của một số byte trong mỗi khung dựa trên loại mã hóa.

Độ rõ của giọng nói được duy trì ở tốc độ lấy mẫu thấp, điều hiếm gặp ở hầu hết các định dạng âm thanh. Thuật toán được sử dụng trong đó là toán học.

Tệp này được mã hóa bằng cách sử dụng ADPCM. Nó rút ngắn dữ liệu âm thanh 16 bit và nén 4 bit. Vì vậy, có một lợi thế là lưu thông tin âm thanh có kích thước lớn hơn ở dạng nhỏ gọn bằng các tệp VOX.


## Người giới thiệu ##

* [VOX - Theo Wikipedia](https://en.wikipedia.org/wiki/Dialogic_ADPCM)

