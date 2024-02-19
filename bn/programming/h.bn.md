{
  "date": "2019-10-11",
  "keywords": [
    "h",
    ".h",
    "what is a h file",
    "how to open h file",
    "extension",
    "file",
    "h file",
    "h file format",
    "h file extension",
    "H File Example"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "H - C/C++ হেডার ফাইল ফরম্যাট",
  "description": "H ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি H ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-bn"
    }
  },
  "lastmod": "2021-05-07"
}

## একটি H ফাইল কি?

**h ফাইল এক্সটেনশন** দিয়ে সংরক্ষিত একটি ফাইল হল একটি হেডার ফাইল যা C/C++ ফাইলগুলিতে ভেরিয়েবল, ধ্রুবক এবং ফাংশনগুলির ঘোষণা অন্তর্ভুক্ত করতে ব্যবহৃত হয়। এগুলিকে [C++](/programming/cpp/) বাস্তবায়ন ফাইল দ্বারা উল্লেখ করা হয় যাতে এই ফাংশনগুলির প্রকৃত বাস্তবায়ন রয়েছে৷ A .h হেডার ফাইলে অতিরিক্ত তথ্য যেমন ম্যাক্রো সংজ্ঞা অন্তর্ভুক্ত থাকতে পারে। এই হেডার ফাইলগুলি C/C++ ফাইলগুলিতে `#include` নির্দেশিকা ব্যবহার করে উল্লেখ করা হয়।

একটি নতুন C++ প্রজেক্টে সাধারণত **stdafx.h** ফাইল নামে একটি বিশেষ হেডার ফাইল থাকে যা সমস্ত সংকলন চেইনের সূচনা বিন্দু এবং সমস্ত হেডার ফাইল এই একক ফাইলে অন্তর্ভুক্ত করা যেতে পারে। A.h ফাইল যেকোন টেক্সট এডিটর, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ কম্পাইলার এবং অন্যান্য অনেক অ্যাপ্লিকেশন দিয়ে খোলা যেতে পারে।

## .এইচ ফাইল ফরম্যাট

A.h ফাইল হল প্লেইন টেক্সট ফাইল যার সিনট্যাক্স সংজ্ঞায়িত করার নিজস্ব নিয়ম রয়েছে। হেডার ফাইলে নিম্নলিখিত তথ্য থাকতে পারে।

**`ভেরিয়েবল`** - অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং (OOP) এর ক্ষেত্রে, একটি ক্লাস হেডার ফাইলে সমস্ত ক্লাস লেভেল ভেরিয়েবলের সংজ্ঞা থাকে যা বাস্তবায়ন সোর্স কোড ফাইল জুড়ে অ্যাক্সেসযোগ্য।
**`পদ্ধতি ঘোষণা`** - সমস্ত পদ্ধতি ঘোষণা .h হেডার ফাইলে অন্তর্ভুক্ত করা হয়েছে যাতে একাধিক বাস্তবায়ন ফাইল জুড়ে অ্যাক্সেসযোগ্য।
**`নন-ইনলাইন ফাংশন সংজ্ঞা`** - হেডার ফাইলে একটি নন-ইনলাইন পদ্ধতির সংজ্ঞাও থাকতে পারে।
**`মেসেজ ম্যাপ`** - একটি হেডার ফাইলে MFC সোর্স কোড বাস্তবায়নের ক্ষেত্রে বার্তা মানচিত্রও থাকতে পারে। এই ধরনের ক্ষেত্রে, বার্তা মানচিত্রগুলি কার্যকারিতা বাস্তবায়নের সাথে সংযুক্ত থাকে যা UI উপাদান যেমন বোতাম, চেকবক্স, রেডিও বোতাম ইত্যাদির সাথে সংযুক্ত থাকে।


### হেডার গার্ড

হেডার ফাইলগুলি জটিল ত্রুটিগুলি বাড়াতে পারে যেখানে অন্যান্য হেডার ফাইলগুলি যোগ করার ফলে একই ফাইলে একাধিক ঘোষণা অন্তর্ভুক্ত করা হয়। এই ডুপ্লিকেট সংজ্ঞা কম্পাইলার ত্রুটি বাড়ায়। এই সমস্যাযুক্ত পরিস্থিতি হেডার গার্ড নামক একটি পদ্ধতির মাধ্যমে এড়ানো যেতে পারে যা নীচে দেখানো হিসাবে শর্তসাপেক্ষ সংকলন নির্দেশিকা।

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
এই হেডারের সাহায্যে, প্রিপ্রসেসর পরীক্ষা করে যে `ANY_UNIQUE_NAME_HERE` ইতিমধ্যেই সংজ্ঞায়িত করা হয়েছে কিনা। শিরোনাম বারবার একই ফাইলে অন্তর্ভুক্ত করা হলে, শিরোনামের বিষয়বস্তু উপেক্ষা করা হবে।

## H ফাইলের উদাহরণ

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## তথ্যসূত্র

* [হেডার ফাইলার - মাইক্রোসফট](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


