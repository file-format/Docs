{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "tệp", "tệp mở rộng", "định dạng", "âm thanh", "smaf", "tiện ích mở rộng mmf", "tệp mmf", "tệp nhạc di động", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp MMF và các API có thể tạo và mở tệp MMF.",
  "title" :"MMF - Định dạng tệp nhạc di động",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Tệp MMF là gì?

MMF là phần mở rộng tệp được liên kết với tệp SMAF. MMF là viết tắt của Tệp nhạc di động trong khi SMAF là viết tắt của Định dạng ứng dụng di động âm nhạc tổng hợp. Các tệp MMF trong điện thoại thông minh chứa nhạc chuông hệ thống, âm thanh và cũng có thể chứa đồ họa và hiển thị văn bản. MMF còn chứa ba loại tham số thiết bị bao gồm FM, PCM và Stream PCM. Các định dạng tệp này tương thích với nền tảng hệ thống Windows. Các tệp MMF được phân loại là tệp dữ liệu. Thông thường, Microsoft Mail hỗ trợ các tệp MMF. Tệp có hậu tố MMF có thể được sao chép vào bất kỳ thiết bị di động hoặc nền tảng hệ thống nào.

Hơn nữa, các tệp này có kích thước nhỏ hơn nhiều so với các tệp định dạng MIDI tiêu chuẩn. Các tệp [WAV](/vi/audio/wav/) và [MID](/vi/audio/mid/) có thể được chuyển đổi sang định dạng MMF, sau đó có thể được chia sẻ và phân phối dưới dạng nội dung âm thanh. Các tệp này có thể được nhận qua email trực tiếp đến điện thoại và PC.


## Lịch sử tóm tắt về định dạng tệp MMF

Yamaha đã phát triển các công cụ SMAF dưới dạng tệp âm thanh để điện thoại thông minh có thể lưu trữ nhiều nhạc chuông độc đáo hơn. Yamaha đã giới thiệu SMAF với việc sản xuất chip âm thanh MA-1, MA-2, MA-3, MA-5 và MA-7 LSI của họ. Tất cả các định dạng này trở nên khá quen thuộc với điện thoại di động ở Thị trường Đông Á vào đầu năm 2000.

Ở cấp độ quốc tế, định dạng MMF đã được Samsung ủy quyền. Với sự trợ giúp của định dạng MMF, Samsung đã có thể thiết kế nhiều loại nhạc chuông đa âm để sử dụng trong điện thoại thông minh Samsung.

Yamaha muốn làm cho định dạng này trở nên phổ biến hơn và do đó, trên các tệp Yamaha SMAF chính thức, hãng đã xuất bản thêm các công cụ tương thích với định dạng này. Với điều này, giờ đây người dùng có thể dễ dàng phát các tệp MMF trên máy tính của họ.


## Thông số kỹ thuật định dạng tệp MMF ##

Các tệp MMF được phân loại thành các phần dữ liệu. Cấu trúc tiền tố xung quanh 8 byte được sử dụng để mô tả từng phân đoạn.
Nhãn 4 byte bao gồm CNTI, OPDA, MSTR, MTR và ATR. Kích thước dữ liệu cộng với 8 byte là kích thước khối; toàn bộ kích thước tệp được tính bằng cách tính tổng tất cả các kích thước khối. Nếu một tệp không bị hỏng, kích thước tệp tổng hợp phải giống với kích thước tiêu đề chính.

### Tiêu đề ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Đây là một ví dụ về tệp MMF:

![](../mmf.png)

## Người giới thiệu

* [MMF - Theo Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

