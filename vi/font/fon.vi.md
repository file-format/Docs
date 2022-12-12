{
  "date" : "2020-08-20",
  "keywords" :[ "tập tin fon", "định dạng tập tin fon", "tệp fon là gì", "tập tin", "ví dụ fon", "phần mở rộng tập tin fon","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Tệp thư viện phông chữ",
  "description":"Tìm hiểu về định dạng tệp FON và các API có thể tạo và mở tệp FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Tệp FON là gì?

Tệp có phần mở rộng .fon là thư viện phông chữ Microsoft Windows 3.x thực sự là một tệp thi hành nhưng được đổi tên thành .fon. Bản thân nó là một tập hợp các tệp [.fnt](/vi/font/fnt/) và các ứng dụng tham chiếu nó trong khi truy cập phông chữ hệ thống. Đó là lý do tại sao nó hoạt động như một tệp tài nguyên. Nó có thể được mở trên hệ điều hành Windows bằng ứng dụng Microsoft Windows Font View.

## Định dạng tệp FON

Tệp FON chứa tài nguyên phông chữ và có định dạng tệp Tài nguyên (.res). Định dạng tệp .res chỉ định tiêu đề tệp cũng như thông số kỹ thuật của phần dữ liệu. .fnt cũng là tệp dữ liệu tài nguyên được bao gồm trong tệp tài nguyên. Các tệp FON có định dạng tệp nhị phân và có loại MIME ứng dụng/octet-stream.

Tài nguyên phông chữ, không giống như các loại tài nguyên khác, không được thêm vào tài nguyên của ứng dụng. Thay vào đó, chúng được thêm vào tệp EXE và đổi tên thành tệp .fon, dẫn đến tệp thư viện thay vì ứng dụng. Nhiều phông chữ riêng lẻ tạo thành các thành phần của một nhóm phông chữ trong đó mỗi nhóm tuân theo cấu trúc nhóm tài nguyên. Tài nguyên phông chữ sử dụng các cấu trúc nhóm tài nguyên này. Tiêu đề nhóm có tất cả thông tin cần thiết để truy cập một phông chữ cụ thể từ nhóm. Tài nguyên thành phần phông chữ có định dạng sau.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/vi/font/fnt/) file)
```
Một tệp tài nguyên .rc có thể có các khai báo tài nguyên hỗn hợp. Các nhóm phông chữ có thể ở bất kỳ đâu trong tệp tài nguyên và không cần phải liền kề nhau. Các chương trình tạo tệp .RES phải thêm mục nhập thủ công của FONTDIR. Sau đây là cấu trúc của tiêu đề nhóm.

```
[Tiêu đề tài nguyên thông thường (loại = 7)]

WORD NumberOfFonts; // Tổng số trong tệp .RES
```     
The remaining data is repeated for every font in the .RES file.

```
phông chữ WORdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfĐi lên;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfTrọng lượng;
BYTE dfCharSet;
TỪ dfPixWidth;
TỪ dfPixHeight;
BYTE dfPitchAndFamily;
TỪ dfAvgWidth;
TỪ dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
TỪ dfWidthByte;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserve;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

