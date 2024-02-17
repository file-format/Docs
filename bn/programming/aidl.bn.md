{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL ফাইল - অ্যান্ড্রয়েড ইন্টারফেস সংজ্ঞা ভাষা ফাইল",
  "description":"উদাহরণ সহ AIDL ফাইল ফরম্যাট কী এবং এআইডিএল ফাইল তৈরি এবং খুলতে পারে এমন APIগুলি সম্পর্কে জানুন৷",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-bn",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## একটি AIDL ফাইল কি?

একটি এআইডিএল (অ্যান্ড্রয়েড ইন্টারফেস ডেফিনিশন ল্যাঙ্গুয়েজ) ফাইল অ্যান্ড্রয়েড ডেভেলপারদের বিভিন্ন অ্যাপের মধ্যে যোগাযোগ স্থাপন করতে দেয়। প্রোগ্রামিং ইন্টারফেসের উপর ভিত্তি করে, ক্লায়েন্ট এবং পরিষেবা উভয়ই ইন্টারপ্রসেস কমিউনিকেট (আইপিসি) ব্যবহার করে যোগাযোগ করতে সম্মত হয়। এআইডিএল ফাইলে এই ইন্টারফেসগুলি সংজ্ঞায়িত করার জন্য [Java](/programming/java/) সোর্স কোড রয়েছে এবং অ্যাপগুলির মধ্যে যোগাযোগের জন্য চুক্তি রয়েছে৷

আপনি গুগল অ্যান্ড্রয়েড স্টুডিও বা মাইক্রোসফ্ট নোটপ্যাড এবং নোটপ্যাড++ এর মতো টেক্সট এডিটর দিয়ে AIDL ফাইল খুলতে পারেন।

## এআইডিএল ফাইল ফরম্যাট - আরও তথ্য

AIDL হল টেক্সট ফাইল যাতে অ্যাপের মধ্যে যোগাযোগের জন্য ইন্টারফেস থাকে। Android OS একটি প্রক্রিয়াকে অন্য প্রক্রিয়ার মেমরি অ্যাক্সেস করার অনুমতি দেয় না। এটি অন্তর্নিহিত অপারেটিং সিস্টেম বোঝার জন্য এবং বিকাশকারীর জন্য যোগাযোগ কাঠামোর প্রক্রিয়া স্থাপনের জন্য প্রক্রিয়াগুলিকে তাদের বস্তুগুলিকে আদিমগুলিতে বিভক্ত করতে পরিচালিত করে।

### কোন ডেটা টাইপ এআইডিএল দ্বারা সমর্থিত?

এআইডিএল ডিফল্টরূপে নিম্নলিখিত ডেটা প্রকারগুলিকে সমর্থন করে৷

 * জাভা প্রোগ্রামিং ভাষার সমস্ত আদিম প্রকার (যেমন int, long, char, বুলিয়ান ইত্যাদি)
 * স্ট্রিং
 * CharSequence
 * তালিকা
 * মানচিত্র

## এআইডিএল ফাইলের উদাহরণ

নিম্নলিখিত একটি উদাহরণ AIDL ফাইল.

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
## তথ্যসূত্র

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

