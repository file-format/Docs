{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Định dạng tệp lưu trữ có thể mở rộng",
  "description":"Tìm hiểu về định dạng tệp XAR và các API có thể tạo và mở tệp XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Tệp XAR là gì?

Tệp có phần mở rộng .xar (Định dạng lưu trữ mở rộng) là tệp lưu trữ UNIX có thể ở định dạng nén hoặc không nén. Nó cũng được sử dụng trên Mac OS để cài đặt các gói. XAR là mã nguồn mở và là một phần của Mac OS X 10.5 để sử dụng với trình duyệt Safari.

## Định dạng tệp XAR

Tệp [XAR](https://github.com/mackyle/xar/wiki/xarformat) có ba vùng chính.

* Tiêu đề
* Mục lục
* Đống

### Tiêu đề XAR

Tiêu đề XAR được cấu trúc như sau.

|Trường|Loại dữ liệu|Kích thước tính bằng byte|
---|---|---|
|Phép thuật|Unsigned Int 32|4|
|Size|Unsigned Int 16|2|
|Phiên bản|Unsigned Int 16|2|
|Độ dài TOC được nén|Unsigned Int 64|8|
|Độ dài TOC Không nén|Int không dấu 64|8|
|Tổng kiểm tra|Int không dấu 32|4|
|Tên thông báo tiêu hóa |Không chấm dứt||

Cấu trúc C của tiêu đề XAR có thể được định nghĩa như sau.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Lưu ý rằng tất cả các trường của tiêu đề (ma thuật, kích thước, phiên bản, toc_length_compressed, toc_length_uncompressed, cksum_alg) luôn được lưu trữ trong các tệp XAR theo thứ tự byte mạng (còn gọi là big endian).

### Mục lục XAR (TOC)

Mục lục là một tài liệu XML (và phải) được mã hóa dưới dạng UTF-8. Nó được lưu trữ ở phần đầu của tệp, giúp dễ dàng quét qua kho lưu trữ để giải nén từng tệp. Kho lưu trữ XAR cho phép bạn nén/mã hóa các tệp riêng lẻ trong kho lưu trữ một cách độc lập bằng cách sử dụng các lược đồ nén khác nhau, chẳng hạn như [GZIP](/vi/compression/gz/), [BZIP2](/vi/compression/bz2) và các lược đồ tương tự khác.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### đống

Heap bắt đầu ngay sau toc được nén. Đó là một đống dữ liệu phi cấu trúc được tham chiếu bởi TOC. Các giá trị Offset được liệt kê trong TOC bắt đầu từ phần đầu của heap. Các giá trị độ dài trong toc đề cập đến số byte thực tế được lưu trữ trong heap (được nén hay không) trong khi giá trị kích thước đề cập đến kích thước được giải nén của mục (sau khi giải nén nếu cần).

## Người giới thiệu

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://vi.wikipedia.org/wiki/Xar_(archiver))

