{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Nén", "Tệp", "Phần mở rộng", "Định dạng tệp", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp LZO",
  "description":"Tìm hiểu về định dạng tệp LZO và API có thể tạo và mở tệp LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Tệp LZO là gì? ##

Tệp có phần mở rộng .lzo được kết hợp với các tính năng lưu trữ tệp có thể giảm tất cả kích thước tệp trong tệp nén. Tất cả các tệp nén có thể bao gồm một hoặc nhiều tệp hoặc thậm chí các nhóm chất kết dính với một số tệp có loại và kích thước khác nhau. Kích thước của tệp nén nhỏ hơn so với kích thước chung của tất cả các tệp và thư mục được lưu trữ trong tệp nén LZO. Tất cả các tệp nén LZO được lưu trữ ở định dạng LZO và được thực thi rõ ràng với các tính năng nén được sử dụng bởi phần mềm nén và giải nén tệp LZOP. Tất cả các thông số kỹ thuật nén được kết hợp vào chương trình nén và giải nén tệp này có nguồn gốc từ thư viện nén tệp Lempel-Ziv-Oberhume. Tốc độ giải nén nhanh hơn và tỷ lệ nén phát triển cũng được kết hợp vào các tệp LZO này.

## Đặc điểm kỹ thuật LZO ##

Markus Franz Xaver Johannes Oberhumer đã phát triển thuật toán "lzop" ban đầu, dựa trên các thuật toán trước đó của Abraham Lempel và Jacob Ziv, vào năm 1996. Thư viện này triển khai nhiều thuật toán với các đặc điểm sau:

* Nén nhanh hơn DEFLATE
* Giải nén nhanh chóng
* Bộ đệm bổ sung cần thiết trong quá trình nén (có kích thước 8KB hoặc 64KB, tùy thuộc vào mức độ nén)
* Bộ đệm nguồn và đích là tất cả bộ nhớ cần thiết để giải nén
* Cung cấp khả năng kiểm soát cả tỷ lệ nén và tốc độ nén

Là một thuật toán nén khối, LZO thực hiện nén chồng chéo cũng như giải nén tại chỗ. Để đạt được nén chồng lấp, kích thước khối của cả quá trình nén và giải nén phải khớp nhau. Thuật toán nén LZO chia dữ liệu đầu vào thành các kết quả khớp (từ điển trượt) và các chữ không khớp, cho kết quả tốt với dữ liệu dư thừa cao và kết quả chấp nhận được với dữ liệu không nén được, chỉ tăng 1/64 dữ liệu không nén được so với ban đầu kích thước.

## Sự cố khi mở tệp LZO ##

Sau đây là một số vấn đề có thể khiến định dạng tệp LZO hoạt động kém:
  


* Tập tin có thể bị hỏng. Để giải quyết vấn đề này, hãy tải xuống lại tệp hoặc yêu cầu người gửi gửi lại tệp
* Nguyên nhân thứ 2 là file bị nhiễm virus trường hợp này scan file đúng cách
* Liên kết không chính xác đến tệp LZO
* Xóa mô tả về LZO
* Không đủ tài nguyên phần cứng
* Trình điều khiển lỗi thời của thiết bị
  


## Người giới thiệu ##

* [LZO - Theo Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

