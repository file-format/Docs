{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","ไฟล์ ah คืออะไร","วิธีเปิดไฟล์ h", "นามสกุล", "ไฟล์", "ไฟล์ h","รูปแบบไฟล์ h", "นามสกุลไฟล์ h", "ตัวอย่างไฟล์ H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ส่วนหัว H - C/C++",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ H และ API ที่สามารถสร้างและเปิดไฟล์ H",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## ไฟล์ H คืออะไร??

ไฟล์ที่บันทึกด้วย **นามสกุลไฟล์ h** เป็นไฟล์ส่วนหัวที่ใช้ในไฟล์ C/C++ เพื่อรวมการประกาศตัวแปร ค่าคงที่ และฟังก์ชัน ไฟล์เหล่านี้อ้างอิงโดยไฟล์การใช้งาน [C++](/th/programming/cpp/) ที่มีการใช้งานจริงของฟังก์ชันเหล่านี้ ไฟล์ส่วนหัว .h ยังสามารถรวมข้อมูลเพิ่มเติม เช่น คำจำกัดความของมาโคร ไฟล์ส่วนหัวเหล่านี้ถูกอ้างอิงในไฟล์ C/C++ โดยใช้คำสั่ง `#include`

โปรเจ็กต์ C++ ใหม่มักจะมีไฟล์ส่วนหัวพิเศษโดยใช้ชื่อไฟล์ **stdafx.h** ที่เป็นจุดเริ่มต้นสำหรับกลุ่มการคอมไพล์ทั้งหมด และไฟล์ส่วนหัวทั้งหมดสามารถรวมอยู่ในไฟล์เดียวนี้ได้ ไฟล์ .h สามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความ, Eclipse IDE, Microsoft Visual Studio IDE, คอมไพเลอร์ Borland C++ และแอปพลิเคชันอื่นๆ อีกมากมาย

## รูปแบบไฟล์ .H

ไฟล์ .h เป็นไฟล์ข้อความธรรมดาที่มีกฎของตัวเองสำหรับการกำหนดไวยากรณ์ ไฟล์ส่วนหัวสามารถมีข้อมูลต่อไปนี้

**`Variables`** - ในกรณีของ Object Oriented Programming (OOP) ไฟล์ส่วนหัวของคลาสประกอบด้วยคำจำกัดความของตัวแปรระดับคลาสทั้งหมดที่สามารถเข้าถึงได้จากไฟล์ซอร์สโค้ดการใช้งาน
**`การประกาศเมธอด`** - การประกาศเมธอดทั้งหมดจะรวมอยู่ในไฟล์ส่วนหัว .h เพื่อให้เข้าถึงได้จากไฟล์การใช้งานหลายไฟล์
**`Non-Inline Function Definitions`** - ไฟล์ส่วนหัวสามารถมีคำจำกัดความของเมธอดที่ไม่ใช่ในบรรทัดได้
**`แมปข้อความ`** - ไฟล์ส่วนหัวยังสามารถมีแมปข้อความในกรณีที่ใช้ซอร์สโค้ด MFC ในกรณีดังกล่าว แมปข้อความจะเชื่อมโยงกับการใช้งานฟังก์ชันซึ่งเชื่อมโยงกับองค์ประกอบ UI เช่น ปุ่ม ช่องทำเครื่องหมาย ปุ่มตัวเลือก เป็นต้น


### เฮดเดอร์การ์ด

ไฟล์ส่วนหัวสามารถทำให้เกิดข้อผิดพลาดที่ซับซ้อนซึ่งการประกาศหลายรายการรวมอยู่ในไฟล์เดียวกันอันเป็นผลมาจากการเพิ่มไฟล์ส่วนหัวอื่นๆ คำจำกัดความที่ซ้ำกันนี้ทำให้เกิดข้อผิดพลาดของคอมไพเลอร์ สถานการณ์ที่เป็นปัญหานี้สามารถหลีกเลี่ยงได้ผ่านกลไกที่เรียกว่า header guard ซึ่งเป็นคำสั่งการรวบรวมแบบมีเงื่อนไขดังที่แสดงด้านล่าง

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
ด้วยส่วนหัวนี้ ตัวประมวลผลล่วงหน้าจะตรวจสอบว่า `ANY_UNIQUE_NAME_HERE` ถูกกำหนดไว้แล้วหรือไม่ หากรวมส่วนหัวไว้ในไฟล์เดียวกันซ้ำๆ เนื้อหาของส่วนหัวจะถูกละเว้น

## ตัวอย่างไฟล์ H

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

## อ้างอิง

* [ไฟล์ส่วนหัว - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

