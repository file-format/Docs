{
  "date": "2019-10-11",
  "keywords": [
    "crt",
    "crt file",
    "crt file format",
    "crt file type",
    "file",
    "type",
    "what is an crt file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CRT - নিরাপত্তা শংসাপত্র ফাইল বিন্যাস",
  "description": "CRT ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CRT ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-crt-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি CRT ফাইল কি?

.crt এক্সটেনশন সহ একটি ফাইল হল একটি নিরাপত্তা শংসাপত্র ফাইল যা নিরাপদ ওয়েবসাইটগুলি ওয়েব সার্ভার থেকে ব্রাউজারে নিরাপদ সংযোগ স্থাপনের জন্য ব্যবহার করে। নিরাপদ ওয়েবসাইটগুলি ডেটা স্থানান্তর, লগইন, পেমেন্ট কার্ড লেনদেন এবং সাইটে সুরক্ষিত ব্রাউজিং প্রদান করা সম্ভব করে। আপনি একটি নিরাপদ ওয়েবসাইট খুললে, আপনি ঠিকানা বারে একটি লক আইকন দেখতে পাবেন৷ আপনি যদি এটিতে ক্লিক করেন, আপনি ইনস্টল করা শংসাপত্রের বিবরণ দেখতে পারেন। আন্তর্জাতিক কোম্পানি যেমন Verisign এবং Thawte এই SSL সার্টিফিকেট বিতরণ করে।

## CRT ফাইল ফরম্যাট

CRT ফাইলগুলি ASCII ফরম্যাটে এবং সার্টিফিকেট ফাইলের বিষয়বস্তু দেখতে যেকোনো পাঠ্য সম্পাদকে খোলা যেতে পারে। এটি X.509 সার্টিফিকেশন স্ট্যান্ডার্ড অনুসরণ করে যা শংসাপত্রের গঠন সংজ্ঞায়িত করে। এটি ডেটা ক্ষেত্রগুলিকে সংজ্ঞায়িত করে যা SSL শংসাপত্রে অন্তর্ভুক্ত করা উচিত। CRT বেস64 ASCII এনকোড করা ফাইলের সার্টিফিকেটের PEM ফর্ম্যাটের অন্তর্গত।

### PEM ফাইলের কাঠামো

একটি PEM ফাইলে একাধিক শংসাপত্র থাকতে পারে। এই ধরনের ক্ষেত্রে, PEM ফাইলের প্রতিটি শংসাপত্র নিম্নলিখিত কাঠামো অনুসরণ করে।

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### CRT ফাইল ফরম্যাটের উদাহরণ

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## তথ্যসূত্র ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

