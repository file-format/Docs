{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PEM ফাইল - গোপনীয়তা উন্নত মেল সার্টিফিকেট ফাইল বিন্যাস",
  "description": "PEM ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি PEM ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pem-bn"
    }
  },
  "lastmod": "2022-09-14"
}

## একটি PEM ফাইল কি?

একটি PEM ফাইল হল একটি নিরাপত্তা শংসাপত্র ফাইল যা একটি ওয়েব সার্ভার এবং একটি ব্রাউজারের মধ্যে একটি নিরাপদ যোগাযোগ চ্যানেল স্থাপন করতে ব্যবহৃত হয়। এটি Base64-এনকোডেড এবং এতে একটি ব্যক্তিগত কী, সার্ভার শংসাপত্র, এবং/অথবা অন্যান্য শংসাপত্রের সংমিশ্রণ থাকতে পারে। PEM ফাইলগুলি ব্যবহারের ক্ষেত্রে .der সার্টিফিকেট ফাইলের অনুরূপ কিন্তু বাইনারি ডেটার পরিবর্তে Base64-এনকোডেড পাঠ্য হিসাবে সংরক্ষণ করা হয়৷ অন্যান্য অনুরূপ সার্টিফিকেট ফাইল ফরম্যাটের মধ্যে রয়েছে [.cer](/web/cer/) এবং [.crt](/web/crt/) ফাইল।

যে অ্যাপ্লিকেশনগুলি **PEM ফাইলগুলি খুলতে পারে** সেগুলির মধ্যে Microsoft Notepad এবং Apple TextEdit এর মতো পাঠ্য সম্পাদক অন্তর্ভুক্ত রয়েছে৷

## PEM ফাইল ফরম্যাট

PEM হল একটি ধারক ফাইল বিন্যাস যা ডেটা সংরক্ষণ করতে ব্যবহৃত ফাইলের গঠন এবং এনকোডিং প্রকারকে সংজ্ঞায়িত করে। PEM ফাইলগুলিকে Base64-এনকোডেড ফাইল ফর্ম্যাট হিসাবে ডিস্কে সংরক্ষণ করা হয় যা মানুষের পাঠযোগ্য নয়। স্ট্যান্ডার্ড সংজ্ঞায়িত করে যে একটি PEM ফাইল দিয়ে শুরু হয়:

```
-----BEGIN <type>-----
```
এবং এর সাথে শেষ হয়:
```
-----END <type>-----
```

এর ভিতরের অন্য সব কন্টেন্ট হল base64 এনকোড করা (বড় হাতের এবং ছোট হাতের অক্ষর, সংখ্যা, +, এবং /)। একটি একক PEM ফাইলে একাধিক ব্লক থাকতে পারে যা অন্যান্য প্রোগ্রাম দ্বারা ব্যবহার করা যেতে পারে। যদি একটি PEM ফাইলে একাধিক শংসাপত্র থাকে, প্রতিটি শংসাপত্র পৃথক ব্লক দ্বারা নিম্নলিখিত হিসাবে পৃথক করা হয়:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### PEM ফাইলের উদাহরণ

সার্টিফিকেট ব্লক সহ একটি PEM ফাইল সাধারণত নিম্নলিখিত মত দেখায়:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

RSA সহ একটি PEM ফাইল নিম্নলিখিত মত শুরু হয়।

```
-----BEGIN RSA PRIVATE KEY-----
```

## তথ্যসূত্র ##

* [পাবলিক কী ক্রিপ্টোগ্রাফি](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [কিভাবে P7C ফাইল তৈরি করবেন?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


