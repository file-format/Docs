{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Tệp liên hệ ảo",
  "description":"Tìm hiểu về định dạng tệp VCF và các API có thể tạo và mở tệp VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VCF là gì?

VCF (Định dạng thẻ ảo) hoặc vCard là định dạng tệp kỹ thuật số để lưu trữ thông tin liên hệ. Định dạng này được sử dụng rộng rãi để trao đổi dữ liệu giữa các ứng dụng trao đổi thông tin phổ biến. Hầu hết các hệ điều hành như Windows và MacOS đều có các ứng dụng mặc định để tạo và mở các tệp này. Một tệp VCF có thể chứa thông tin liên hệ của một hoặc nhiều liên hệ. Tệp VCF thường chứa thông tin như tên, địa chỉ, số điện thoại, email, ngày sinh, ảnh và âm thanh của người liên hệ cùng với một số trường khác. Được hỗ trợ bởi các ứng dụng email và dịch vụ, không xảy ra tình trạng mất dữ liệu trong quá trình chuyển danh bạ qua định dạng vCard. Loại phương tiện cho định dạng tệp VCF là văn bản/vcard.

## Định dạng tệp VCF

Các tệp VCF có bản chất là văn bản và con người có thể đọc được. Chúng có thể được mở trong các trình soạn thảo văn bản như Notepad trên Microsoft Windows và TextEdit trên MacOS. Tuy nhiên, nếu có một hình ảnh trong tệp, nó sẽ không hiển thị trong trình soạn thảo văn bản.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) cung cấp hỗ trợ cho mở các tệp VCF cũng như chuyển đổi sang một số định dạng khác, chẳng hạn như định dạng [MSG](/vi/email/msg/) phổ biến. Định dạng tệp VCF được cải tiến theo thời gian từ phiên bản 2.1 đến 4.0 bổ sung thông tin chi tiết vào định dạng tệp. Định dạng này cũng được sử dụng để xuất danh bạ điện thoại và sau đó nhập vào một thiết bị khác.

{{< figure src="../VCF.png" alt="Định dạng tệp VCF" >}}

### VCF 2.1 Ví dụ

Sau đây là một ví dụ về phiên bản 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Ví dụ về VCF 3.0

Sau đây là một ví dụ về phiên bản 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Ví dụ về VCF 4.0

Sau đây là một ví dụ về phiên bản 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Người giới thiệu

* [VCF - Theo Wikipedia](https://en.wikipedia.org/wiki/VCard)

