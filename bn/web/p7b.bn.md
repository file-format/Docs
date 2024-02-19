{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "P7B - PKCS 7 সার্টিফিকেট ফাইল",
  "description": "P7C ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি P7C ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7b-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি P7B ফাইল কি?

একটি P7B ফাইল হল একটি নিরাপত্তা শংসাপত্র ফাইল যাতে একটি ব্যক্তি বা ডিভাইস প্রমাণীকরণের জন্য নিরাপদ ডিজিটাল শংসাপত্র রয়েছে। একটি [.cer](/web/cer/) সার্টিফিকেট ফাইলের মতো, একটি P7B ফাইল ফাইলে ডান ক্লিক বিকল্প ব্যবহার করে ইনস্টল সার্টিফিকেট বিকল্প ব্যবহার করে ইনস্টল করা যেতে পারে। P7B CER ফাইল ফরম্যাটের চেয়ে ভিন্ন ফর্ম্যাটিং বিকল্প ব্যবহার করে। এটিতে এক বা একাধিক X.509 ডিজিটাল সার্টিফিকেট ফাইল রয়েছে যা base64 (ASCII) এনকোডিং ব্যবহার করে। P7B ফাইলগুলি একটি [ZIP](/compression/zip/) ফাইল হিসাবে গৃহীত হয় বা শংসাপত্র কর্তৃপক্ষ থেকে প্রাপ্ত হয়৷

## P7B ফাইল ফরম্যাট

P7B ফাইলগুলি প্লেইন ASCII ফাইল হিসাবে সংরক্ষণ করা হয় যা যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে। এটিতে পাবলিক কী রয়েছে যা একটি এনকোডেড স্ট্রিং যা পঠনযোগ্যতার দৃষ্টিকোণ থেকে অর্থহীন।

### P7B ফাইল ফরম্যাটের উদাহরণ

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## তথ্যসূত্র ##

* [পাবলিক কী ক্রিপ্টোগ্রাফি](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [কিভাবে P7C ফাইল তৈরি করবেন?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


