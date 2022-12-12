{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp AIDL - Tệp ngôn ngữ định nghĩa giao diện Android",
  "description":"Tìm hiểu về định dạng tệp AIDL với ví dụ và các API có thể tạo và mở tệp AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Tệp AIDL là gì?

Tệp AIDL (Ngôn ngữ định nghĩa giao diện Android) cho phép các nhà phát triển Android thiết lập giao tiếp giữa các ứng dụng khác nhau. Dựa trên giao diện lập trình, cả máy khách và dịch vụ đều đồng ý giao tiếp bằng giao tiếp liên quá trình (IPC). Tệp AIDL chứa mã nguồn [Java](/vi/programming/java/) để xác định các giao diện này và hợp đồng giao tiếp giữa các ứng dụng.

Bạn có thể mở tệp AIDL bằng Google Android Studio hoặc bất kỳ trình soạn thảo văn bản nào như Microsoft Notepad và Notepad++.

## Định dạng tệp AIDL - Thông tin khác

AIDL là các tệp văn bản chứa các giao diện để giao tiếp giữa các ứng dụng. Hệ điều hành Android không cho phép một tiến trình truy cập vào bộ nhớ của tiến trình khác. Điều này dẫn đến các quy trình chia các đối tượng của chúng thành các đối tượng nguyên thủy để hiểu hệ điều hành cơ bản và thiết lập quy trình cấu trúc giao tiếp cho nhà phát triển.

### Loại Dữ liệu nào được AIDL hỗ trợ?

AIDL hỗ trợ các loại dữ liệu sau đây theo mặc định.

* Tất cả các kiểu nguyên thủy trong ngôn ngữ lập trình Java (chẳng hạn như int, long, char, boolean, v.v.)
* Sợi dây
* Trình tự Char
* Danh sách
* Bản đồ

## Ví dụ về tệp AIDL

Sau đây là một tệp AIDL mẫu.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Người giới thiệu

* [Ngôn ngữ định nghĩa giao diện Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

