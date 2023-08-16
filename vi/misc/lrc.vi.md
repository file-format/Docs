{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp LRC - Tệp LRC là gì?",
  "description":"Tìm hiểu về tệp Lyric LRC và các API có thể tạo và mở tệp LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Tệp LRC là gì?

Tệp LRC là tệp lời bài hát dựa trên văn bản có chứa lời bài hát của một bài hát âm thanh. Khi bài hát âm thanh được phát bằng trình phát nhạc hoặc phần mềm phát âm thanh trên máy tính, tệp LRC được đọc song song và hiển thị theo thời gian. Các tệp LRC chứa các điểm gợi ý để hiển thị lời bài hát khi bài hát đang phát. Nói chung, các tệp LRC có cùng tên với tệp âm thanh tương ứng, chẳng hạn như audio.mp3 và audio.lrc. Các tệp LRC tương tự như các tệp phụ đề như [SRT](/vi/video/srt/).

## Định dạng tệp LRC - Thông tin thêm

Các tệp định dạng lời bài hát LRC được lưu dưới dạng tệp văn bản thuần túy và có thể được mở và chỉnh sửa trong tệp văn bản. Nội dung của tệp LRC chứa thông tin màu để hiển thị văn bản lời bài hát.

## Định dạng LRC

Có nhiều định dạng tệp LRC đã được phát triển theo thời gian. Này

### Định dạng LRC đơn giản

Thẻ Thời gian Dòng có định dạng [mm:ss.xx] trong đó mm là phút, ss là giây và xx là phần trăm của giây.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Định dạng Đơn giản Mở rộng

Nó bao gồm Khả năng thay đổi và chỉ định giới tính của lời bài hát bằng cách sử dụng M: Male, F: Female, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Định dạng LRC nâng cao

Định dạng LRC nâng cao là phiên bản mở rộng của định dạng LRC đơn giản. Nó thêm Thẻ thời gian từ ở định dạng<mm:ss.xx> ở cuối từ trước đó.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Người giới thiệu

* [Định dạng tệp lời bài hát LRC - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

