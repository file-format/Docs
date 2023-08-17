{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp Torrent - Tệp BitTorrent",
  "description":"Tìm hiểu về tệp TORRENT và API có thể tạo và mở tệp TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Tệp TORRENT là gì?

Tệp TORRENT là một tệp văn bản được BitTorrent và các chương trình P2P (ngang hàng) khác sử dụng để tải xuống và trao đổi nội dung. Nội dung có thể tải xuống có thể bao gồm tài liệu, video, trò chơi, phim và các phương tiện khác có sẵn trên internet. Nó bao gồm thông tin siêu dữ liệu về nội dung và vị trí của phương tiện sẽ được tải xuống. Phần mềm như BitTorrent sử dụng thông tin từ tệp này, chẳng hạn như tên, kích thước tệp và cấu trúc thư mục để tải xuống dữ liệu. Các tệp torrent có thể được chuyển đổi sang các định dạng tệp khác như [PDF](/vi/pdf/) trực tuyến.

## Tải torrent là gì? Định dạng tệp TORRENT để trao đổi dữ liệu

Torrenting là khái niệm trao đổi (tải xuống và tải lên) các tệp dữ liệu bằng mạng BitTorrent. Không giống như các máy chủ thông thường, nơi dữ liệu được tải lên để người khác truy cập và tải xuống, các tệp torrent được truy xuất và gửi bằng mạng torrent. Khi người dùng mở tệp .torrent trong các ứng dụng như BitTorrent, phần mềm sẽ bắt đầu tải xuống nội dung của tệp theo từng bit. Nếu nhiều người dùng có cùng một tệp, BitTorrent sẽ chia các lượt tải xuống cho tất cả người dùng để tăng tốc quá trình tải xuống. Đồng thời, máy tính của người dùng đang tải xuống tệp cũng trở thành nguồn tệp để gửi tệp cho những người dùng khác cũng đang tải xuống cùng một tệp.

### Cấu trúc của tệp TORRENT

Tệp torrent là sự kết hợp của danh sách tệp và thông tin siêu dữ liệu về tất cả các phần của tệp sẽ được tải xuống. Nó chứa các thông tin sau dưới dạng các phím.

- `announce` — URL của trình theo dõi được thông báo cho các đồng nghiệp khác để thông báo về tính khả dụng của tệp
- `info` — Cái này ánh xạ tới một từ điển có các khóa phụ thuộc vào việc một hay nhiều tệp đang được chia sẻ:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — kích thước của tệp tính bằng byte.
- `path` — danh sách các chuỗi tương ứng với tên thư mục con, chuỗi cuối cùng là tên tệp thực
- `length` — kích thước của tệp tính bằng byte (chỉ khi một tệp đang được chia sẻ)
- `name` — tên tệp mà tệp sẽ được lưu
- `độ dài mảnh` — số byte trên mỗi mảnh. Đây thường là 28 KiB = 256 KiB = 262.144 B.
- `mảnh` — một danh sách băm là sự kết hợp của hàm băm SHA-1 của mỗi phần.

## Tải torrent có an toàn và hợp pháp không?

Giao thức torrent để trao đổi dữ liệu giữa những người dùng P2P là an toàn vì nó chỉ là phương tiện chia sẻ bất kỳ loại tệp nào. Do đó, bản thân giao thức không phải là không an toàn hoặc bất hợp pháp. Tuy nhiên, nội dung được chia sẻ qua mạng có thể chứa các tệp hoặc phương tiện có thể vi phạm tình trạng pháp lý của các tài liệu được chia sẻ. Trong trường hợp như vậy, việc trao đổi dữ liệu như vậy có thể gây ra các hành động pháp lý chống lại các bên liên quan đến việc chia sẻ các tệp đó một cách công khai.

## Người giới thiệu

* [Tệp Torrent - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

