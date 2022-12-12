{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MKS",
  "keywords" :[ "mks", "matroska video", "định dạng mkv", "tệp", "định dạng", "video"],
  "description":"Tìm hiểu về định dạng tệp MKS dành cho phụ đề chỉ được tạo bởi Matroska và các API có thể tạo và mở tệp MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Tệp MKS là gì?

Các tệp MKS thường được gọi là tệp Matroska chỉ chứa phụ đề. Mặc dù Matroska là một bộ chứa tệp chung, nhưng nó tránh lưu giữ thông tin của các định dạng cụ thể. Do phụ đề đang được sử dụng trong một số vùng chứa âm thanh hoặc video nên Matroska đang chú ý lưu trữ một số định dạng phụ đề phổ biến. Nó giúp Matroska phù hợp với tốc độ tăng trưởng. Bạn cần làm theo các điểm được đưa ra dưới đây để lưu trữ phụ đề trong Matroska:

- “.mks”. phần mở rộng sẽ được sử dụng bởi tệp Matroska (chỉ chứa phụ đề).
- **CodecPrivate** đang được sử dụng để lưu trữ tất cả thông tin liên quan đến codec chung cho toàn bộ luồng.
- Xóa dấu thời gian Bắt đầu và dừng được sử dụng trong định dạng lưu trữ gốc có dấu thời gian. Thay vào đó, hãy sử dụng dấu thời gian và Thời lượng của Khối.
- Bạn có thể sử dụng bất kỳ thứ gì có lớp trong suốt, kể cả video.

## Định dạng phụ đề phổ biến

Dưới đây là một số lưu ý ngắn gọn về các định dạng phụ đề phổ biến hơn được lưu trữ trong Matroska:

### Hình ảnh Phụ đề
Định dạng phụ đề VobSub là định dạng phụ đề hình ảnh đầu tiên được nhập vào Matroska. Định dạng này được tạo bằng cách xuất phụ đề từ đĩa DVD. Các rãnh nên được tách biệt trong khi lưu trữ trong Matroska nếu VobSub bao gồm một tập hợp nhiều luồng.

### Phụ đề SRT
SRT là định dạng phụ đề đơn giản và cơ bản nhất. Nó bao gồm bốn phần như được đưa ra dưới đây:
 



1. Một số cho biết trình tự của phụ đề.
2. Thời gian xuất hiện và biến mất của phụ đề trên màn hình.
3. Bản thân phụ đề.
4. Một dòng trống để chỉ điểm bắt đầu của phụ đề tiếp theo.
 



### Phụ đề SSA/ASS
Sub Station Alpha (SSA) là định dạng tệp được sử dụng bởi trình chỉnh sửa phụ đề phổ biến SubStation Alpha. Phụ đề SSA được người hâm mộ sử dụng rộng rãi. Nó có khả năng hiển thị các tính năng hiện đại, ví dụ như karaoke, định vị, kiểu dáng, v.v.
 



### WebVTT Phụ đề
World Wide Web Consortium (W3C) đã phát triển WebVTT, được viết tắt là “Định dạng theo dõi văn bản video trên web”. Định dạng này đang được sử dụng để đánh dấu các tài nguyên theo dõi văn bản bên ngoài liên quan đến phần tử HTML.

### Phụ đề đồ họa trình chiếu HDMV
Định dạng phụ đề đồ họa trình chiếu HDMV (HDMV PGS) là một loạt ảnh bitmap và chúng tôi không thể nói nó là văn bản. Nói cách khác, bạn có thể nói nó chỉ là một chuỗi các hình ảnh đồ họa theo thời gian. Để trích xuất thông tin, việc chuyển đổi PGS sang SRT là một quá trình cần thiết.

### Phụ đề văn bản HDMV
Văn bản HDMV được gọi là định dạng phụ đề văn bản được sử dụng trên Blu-ray. Matroska chỉ cho phép bộ ký tự UTF-8 Khi lưu trữ phụ đề TextST.

### phụ đề Phát sóng video kỹ thuật số (DVB)
Định dạng phụ đề DVB đã được giới thiệu để điều chỉnh việc truyền và hiển thị một số ngôn ngữ phụ đề trên tín hiệu TV. Một định dạng phụ đề điển hình cũng sẽ cho phép bất kỳ người xem nào xem các chương trình truyền có phụ đề DVB, bất kể nhà sản xuất hệ thống truyền là gì.


## Người giới thiệu ##

- [Phụ đề Matroska](https://www.matroska.org/technical/subtitles.html)

