{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "tệp", "phần mở rộng", "định dạng", "định dạng tệp trao đổi âm thanh", "âm nhạc" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp WMA và các API có thể tạo và mở tệp WMA.",
  "title" :"WMA - Tệp âm thanh Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Tệp WMA là gì?

Tệp có phần mở rộng .wma đại diện cho tệp âm thanh được lưu ở định dạng Định dạng Hệ thống Nâng cao (ASF). ASF là định dạng độc quyền của Microsoft chứa các dòng bit được mã hóa bởi Windows Media Audio 9. Ngoài nội dung âm thanh, tệp WMA còn chứa các đối tượng siêu dữ liệu như tiêu đề, album, nghệ sĩ và thể loại của bản nhạc. Các tệp WMA chủ yếu được sử dụng để phát trực tuyến trên web tương tự như các tệp [.mp3](/vi/audio/mp3/).

## Định dạng tệp WMA

Tệp WMA là định dạng tệp nhị phân và được chứa trong định dạng tệp ASF. Nó chỉ định mã hóa siêu dữ liệu về tệp tương tự như các thẻ ID3 được sử dụng bởi các tệp MP3. Bộ giải mã WMA đã được Microsoft sử dụng ở Định dạng tệp có thể tương tác được bảo vệ (PIFF) từ năm 2008. Tuy nhiên, bộ giải mã này chưa được tuyên bố là bộ giải mã âm thanh được tiêu chuẩn hóa theo các tiêu chuẩn ngành liên quan như DECE UltraViolet và MPEG-DASH.

### Dữ liệu cụ thể của loại WMA

Thông tin dành riêng cho loại dành cho codec Windows Media Audio được lưu trữ ở định dạng sau như một phần của Dữ liệu dành riêng cho loại của Đối tượng thuộc tính luồng.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Người giới thiệu

* [Tổng quan về ASF - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

