{
  "date" : "2019-10-11",
  "keywords" :[ "एच", ".एच", "आह फाइल क्या है", "एच फाइल कैसे खोलें", "एक्सटेंशन", "फाइल", "एच फाइल", "एच फाइल फॉर्मेट", "एच फाइल एक्सटेंशन", "एच फ़ाइल उदाहरण"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एच - सी/सी++ हैडर फाइल फॉर्मेट",
  "description":"एच फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एच फ़ाइल बना और खोल सकते हैं।",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## एच फाइल क्या है?

**H फ़ाइल एक्सटेंशन** के साथ सहेजी गई फ़ाइल एक हेडर फ़ाइल है जिसका उपयोग C/C++ फ़ाइलों में वेरिएबल, स्थिरांक और फ़ंक्शन की घोषणा को शामिल करने के लिए किया जाता है। इन्हें [C++](/hi/ प्रोग्रामिंग/cpp/) कार्यान्वयन फाइलों द्वारा संदर्भित किया जाता है जिसमें इन कार्यों का वास्तविक कार्यान्वयन होता है। .h हेडर फ़ाइल में अतिरिक्त जानकारी जैसे मैक्रो परिभाषाएँ भी शामिल हो सकती हैं। इन शीर्षलेख फ़ाइलों को `#include` निर्देश का उपयोग करके C/C++ फ़ाइलों में संदर्भित किया जाता है।

एक नई सी ++ परियोजना में आमतौर पर **stdafx.h** फ़ाइल नाम से एक विशेष शीर्षलेख फ़ाइल होती है जो सभी संकलन श्रृंखलाओं के लिए प्रारंभिक बिंदु है और सभी शीर्षलेख फ़ाइलों को इस एकल फ़ाइल में शामिल किया जा सकता है। .h फ़ाइल को किसी भी टेक्स्ट एडिटर, एक्लिप्स आईडीई, माइक्रोसॉफ्ट विज़ुअल स्टूडियो आईडीई, बोरलैंड सी ++ कंपाइलर और कई अन्य अनुप्रयोगों के साथ खोला जा सकता है।

## एच फ़ाइल स्वरूप

एक .h फ़ाइल सादा पाठ फ़ाइल है जिसके सिंटैक्स को परिभाषित करने के अपने नियम हैं। शीर्षलेख फ़ाइलों में निम्न जानकारी हो सकती है।

**`Variables`** - ऑब्जेक्ट ओरिएंटेड प्रोग्रामिंग (OOP) के मामले में, एक क्लास हेडर फ़ाइल में सभी क्लास लेवल वेरिएबल्स की परिभाषाएँ होती हैं जो कार्यान्वयन स्रोत कोड फ़ाइलों में पहुँच योग्य होती हैं
**`मेथड्स डिक्लेरेशन`** - सभी मेथड्स डिक्लेरेशन को .h हेडर फाइल्स में शामिल किया जाता है ताकि मल्टीपल इम्प्लीमेंटेशन फाइल्स में एक्सेस किया जा सके।
**`गैर-इनलाइन फ़ंक्शन परिभाषाएं`** - हेडर फ़ाइलों में गैर-इनलाइन विधियों की परिभाषाएं भी हो सकती हैं।
**`संदेश मैप्स`** - एमएफसी स्रोत कोड कार्यान्वयन के मामले में हेडर फ़ाइल में संदेश मानचित्र भी हो सकते हैं। ऐसे मामले में, संदेश मानचित्र कार्यक्षमता कार्यान्वयन से जुड़े होते हैं जो यूआई तत्वों जैसे बटन, चेकबॉक्स, रेडियो बटन इत्यादि से जुड़े होते हैं।


### हैडर गार्ड

शीर्षलेख फ़ाइलें जटिल त्रुटियों को बढ़ा सकती हैं जहां अन्य शीर्षलेख फ़ाइलों को जोड़ने के परिणामस्वरूप एक ही फ़ाइल में एकाधिक घोषणाएं शामिल की जाती हैं। यह डुप्लिकेट परिभाषाएँ कंपाइलर त्रुटियों को बढ़ाती हैं। इस समस्याग्रस्त स्थिति को हेडर गार्ड नामक एक तंत्र के माध्यम से टाला जा सकता है जो सशर्त संकलन निर्देश हैं जैसा कि नीचे दिखाया गया है।

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
इस शीर्षलेख के साथ, प्रीप्रोसेसर यह जांचता है कि क्या `ANY_UNIQUE_NAME_HERE` पहले से परिभाषित किया गया है। यदि हेडर को एक ही फाइल में बार-बार शामिल किया जाता है, तो हेडर की सामग्री को नजरअंदाज कर दिया जाएगा।

## एच फ़ाइल उदाहरण

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

## संदर्भ

* [हेडर फाइलर्स - माइक्रोसॉफ्ट](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

