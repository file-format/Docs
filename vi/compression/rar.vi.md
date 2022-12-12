{
  "date" : "2019-10-11",
  "keywords" :[ "tệp rar", "định dạng tệp rar", "tệp rar là gì", "tệp", "ví dụ rar", "phần mở rộng tệp rar","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Phần mở rộng tệp RAR là gì và các API có thể tạo và mở tệp RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp RAR là gì?

Các tệp có phần mở rộng .rar là các tệp lưu trữ được tạo để lưu trữ thông tin ở dạng nén hoặc thông thường. RAR, viết tắt của định dạng tệp Roshal ARchive, là định dạng tệp độc quyền được tạo bởi Eugene Roshal vào năm 1995, một kỹ sư phần mềm người Nga. Định dạng được sử dụng để lưu trữ tệp bằng các phương pháp khác nhau bao gồm các kỹ thuật nén khác nhau. Có một số phần mềm ứng dụng có sẵn cho Windows, Linux và MacOS để giải nén các tệp RAR. Phần mềm WinRAR, của RARLab, là tiện ích lưu trữ tệp phần mềm chia sẻ (miễn phí trong 40 ngày) cho nền tảng Microsoft Windows; phần mềm đã được chuyển sang Linux (chỉ dưới dạng trình trích xuất) bởi cùng một Tác giả, Eugene Roshal.

## Phiên bản Lịch sử của định dạng tệp RAR

* v1.3 (bản gốc, không có chữ ký "Rar!")
* v1.5
* v2.0 - phát hành với WinRAR 2.0 và Rar cho MS-DOS 2.0
* v2.9 - phát hành trong phiên bản WinRAR 3.00
* v5.0 - được hỗ trợ bởi WinRAR 5.0 trở lên

## Các tính năng chính của định dạng RAR

RAR đã có mặt trong lĩnh vực này từ khá lâu và là một trong những định dạng tệp lưu trữ được yêu thích. Các tính năng chính về định dạng RAR là:

**`Tỷ lệ nén cao:`** Vượt trội so với [ZIP](/vi/compression/zip/), có thể so sánh với định dạng 7z và zipx.

**`Mã hóa tệp mạnh theo thiết kế:`** Các tệp lưu trữ RAR4 được mã hóa dựa trên mã hóa dựa trên AES-128 trong khi các tệp lưu trữ RAR5 được mã hóa dựa trên mã hóa AES-256 với lập lịch trình khóa được cải thiện

**`Khả năng khôi phục dữ liệu và sửa lỗi nâng cao:`** các bản ghi khôi phục tùy chọn trong quá trình tạo tệp lưu trữ

**`Kích thước tệp:`** Kích thước tối thiểu 20 byte và tối đa 2^63 byte (8 exabyte trong tổng kích thước của kho lưu trữ)

**`Kho lưu trữ RAR nhiều tập:`** Khả năng chia các kho lưu trữ lớn thành nhiều tệp nhỏ hơn để tạo điều kiện truyền qua mạng. Trong trường hợp như vậy, phần mở rộng của tệp được tăng thêm 1 để biểu thị các khối lượng được phân chia

## Định dạng tệp RAR

Thông số kỹ thuật đầy đủ của định dạng RAR không có sẵn công khai và đó là lý do tại sao các chi tiết về định dạng không thể được xây dựng một cách ngắn gọn.

### Bố cục Lưu trữ Chung

Bố cục chung của định dạng tệp RAR được giới thiệu trong phiên bản 5.0 như sau:

|Định dạng tệp
---|
|Mô-đun tự giải nén (tùy chọn)
|RAR 5.0 Chữ ký
|Lưu trữ tiêu đề mã hóa (tùy chọn)
|Tiêu đề Lưu trữ Chính
|Lưu trữ tiêu đề dịch vụ bình luận (tùy chọn)
Tiêu đề tệp 1
|Tiêu đề dịch vụ (NTFS ACL, luồng, v.v.) cho tệp trước đó (tùy chọn)
|...
|Tiêu đề tập tin N
|Tiêu đề dịch vụ (NTFS ACL, luồng, v.v.) cho tệp trước đó (tùy chọn)
|Bản ghi phục hồi (tùy chọn)
|Kết thúc tiêu đề lưu trữ

Bạn có thể tìm thấy thông tin về từng phần của tệp RAR được đề cập ở trên trong tài liệu [Thông số định dạng tệp RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Bản lưu trữ RAR tự giải nén

Nếu bản thân tệp RAR tự giải nén, thì thông tin tự giải nén được chứa ở phần đầu của tệp trước chữ ký lưu trữ. Kích thước và nội dung của nó không được xác định.

#### Chữ ký RAR 5.0

Chữ ký RAR là một tiêu đề 8 byte bao gồm số ma thuật sau:

0x 52 61 72 21 1A 07 00

ở đâu

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Người giới thiệu

* [Định dạng lưu trữ RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - Theo Wikipedia](https://vi.wikipedia.org/wiki/RAR_(file_format))

