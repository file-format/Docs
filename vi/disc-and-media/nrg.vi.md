{
  "date" : "2021-08-16",
  "keywords" :[ "tệp nrg", "định dạng tệp nrg", "tệp nrg là gì", "tệp", "ví dụ nrg", "phần mở rộng tệp nrg","phần mở rộng", "định dạng", "chân trang nrg", "tệp định dạng của nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp NRG và API có thể tạo và mở tệp NRG.",
  "title" :"NRG - Định dạng tệp ảnh đĩa",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Tệp NRG là gì?

Định dạng tệp hình ảnh được tạo bằng cách sử dụng đĩa quang được coi là định dạng tệp NRG. Định dạng này được Nero tạo riêng cho tiện ích của Nero Burning Rom. Để lưu trữ ảnh đĩa, định dạng này được coi là được sử dụng vì nó phù hợp với các tệp cụ thể này. Các tệp này có thể ở dạng bản sao chính xác của đĩa CD hoặc DVD hoặc có thể có một số tệp có thể được gắn dưới dạng đĩa. Các định dạng tệp phổ biến khác như định dạng tệp [ISO](/vi/compression/iso/) là những định dạng mà các tệp này có thể được chuyển đổi thành một số tiện ích cơ bản. Hầu hết, các tệp NRG được sử dụng để tạo bản sao lưu hoặc bản sao của một số dữ liệu hoặc đĩa quan trọng.

## Định dạng tệp NRG ##

Định dạng tệp này được Nero AG phát triển dưới dạng định dạng ảnh đĩa. Nó có thuộc tính cụ thể của tiện ích Nero Burning Rom vì nó được phát triển để lưu trữ ảnh đĩa. Phiên bản đầu tiên của nó được chỉ định để lưu trữ các giá trị dưới dạng số nguyên 32 bit. Tuy nhiên, phiên bản thứ hai của nó đã được tung ra và có hỗ trợ cho các số nguyên 64 bit.

## Thông số kỹ thuật ##

Ở phần đầu của tệp, định dạng này không lưu trữ dữ liệu của nó dưới dạng tiêu đề. Giống như footer, nó được đính kèm ở cuối tập tin. Ở dạng khối của IFF, thông tin của hình ảnh được lưu trữ. Độ lệch của đoạn đầu tiên có thể thu được bằng cách đọc chân trang NRG ở 8 byte cuối cùng đến 12 byte của tệp. Trong tất cả các phiên bản của định dạng tệp NRG, có các khối, DAOI, văn bản CD, loại phương tiện thông tin phiên, thông tin đĩa, Relo và phần cuối của chuỗi được đính kèm với nó. Thứ tự byte là big-endian và tất cả các giá trị số nguyên không được ký tại thời điểm lưu trữ.

### Đoạn chính ###

#### Cue sheet ####

Bảng gợi ý này có sẵn dễ dàng trong tất cả các phiên bản định dạng tệp NRG. Đoạn **CUEX** có nghĩa là các khối nối có kích thước cố định và mỗi khối này đại diện cho điểm dừng.

#### Thông tin ĐẠO ####

Thông tin này cũng có trong tất cả các phiên bản định dạng NRG. Các đoạn **DAOI** lưu trữ thông tin cụ thể có liên quan thành 2 phần. Phần đầu tiên của nó chỉ bao gồm dữ liệu phiên cụ thể. Phần thứ hai của nó chỉ lặp lại thông tin màu xám liên quan đến theo dõi và nó chỉ một lần cho mỗi bản nhạc.

#### Văn bản CD ####

Điều này có sẵn trong phiên bản thứ hai của NRG. Đoạn của **CDTX** bao gồm phần ghép thô của gói văn bản CD có 18 byte cho mỗi phần.

#### Thông tin theo dõi mở rộng ####

Điều này có sẵn trong mọi phiên bản định dạng tệp của NRG. Các khối này được sử dụng để lưu trữ thông tin theo dõi cho theo dõi phiên cùng một lúc. Dữ liệu này chỉ được lặp lại một lần trong trường hợp của mỗi bản nhạc.

#### Thông tin phiên ####

Điều này cũng có sẵn trong mọi phiên bản định dạng tệp của NRG. Thông tin về các khối phiên cần được sử dụng để quét hình ảnh của phiên một cách nhanh chóng và sau đó đếm số lần theo dõi.

#### Kết thúc chuỗi ####

Đoạn cuối có nghĩa là tín hiệu cho biết hiện tại không còn đoạn nào cần đọc nữa và điều này cũng có sẵn trong tất cả các phiên bản của NRG.


## Người giới thiệu ##

* [NRG - theo Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


