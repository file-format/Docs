
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp APKS - Lưu trữ bộ APK",
  "description":"Tìm hiểu về tệp APKS là gì?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Tệp APKS là gì?

Một tệp có phần mở rộng .apks là một tệp lưu trữ là tập hợp các tệp **APK** của gói Android. Mỗi tệp APK riêng lẻ trong tệp APKS được tạo để theo dõi các khía cạnh khác nhau của thiết bị. Chúng bao gồm kiến trúc, ngôn ngữ, mật độ màn hình và các tính năng khác của thiết bị. Các tệp APKS được tạo bởi **bundletool**. Nó được dùng để xây dựng Android App Bundle và chuyển đổi gói ứng dụng thành các APK khác nhau để triển khai trên các thiết bị.

## Định dạng tệp APKS - Thông tin khác

Tệp APKS được lưu dưới dạng tệp nén sử dụng định dạng tệp [ZIP](/vi/compression/zip/).

## Làm cách nào để tạo tệp APKS?

Khi Android App Bundle (AAB) sẵn sàng, hành vi của nó trên cửa hàng Google Play có thể được thử nghiệm để triển khai cho một thiết bị. Các tệp APKS có thể được tạo, cho mục đích này, từ các tệp AAB và được cài đặt trên các thiết bị thử nghiệm bằng [công cụ gói] Android của Google (https://developer.android.com/tools/bundletool). Nó cung cấp các công cụ dòng lệnh để tạo tệp lưu trữ APKS từ APK bằng cách sử dụng lệnh sau.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Để triển khai APK cho thiết bị, tệp APKS có thể được ký bằng thông tin ký thiết bị như sau.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Người giới thiệu

* [bundletool - dòng lệnh](https://developer.android.com/tools/bundletool)

