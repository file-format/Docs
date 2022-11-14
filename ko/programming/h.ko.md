{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","ah 파일이란","h 파일을 여는 방법", "확장자", "파일", "h 파일","h 파일 형식", "h 파일 확장자", "H 파일 예"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ 헤더 파일 형식",
  "description":"H 파일을 만들고 열 수 있는 H 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## H 파일이란?

**h 파일 확장명**으로 저장된 파일은 C/C++ 파일에서 변수, 상수, 함수 선언을 포함하는 헤더 파일입니다. 이들은 이러한 기능의 실제 구현을 포함하는 [C++](/ko/programming/cpp/) 구현 파일에 의해 참조됩니다. .h 헤더 파일에는 매크로 정의와 같은 추가 정보도 포함될 수 있습니다. 이러한 헤더 파일은 `#include` 지시문을 사용하여 C/C++ 파일에서 참조됩니다.

새 C++ 프로젝트에는 일반적으로 모든 컴파일 체인의 시작점인 **stdafx.h** 파일이라는 이름의 특수 헤더 파일이 포함되며 모든 헤더 파일은 이 단일 파일에 포함될 수 있습니다. .h 파일은 모든 텍스트 편집기, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ 컴파일러 및 기타 여러 응용 프로그램에서 열 수 있습니다.

## .H 파일 형식

.h 파일은 구문을 정의하기 위한 고유한 규칙이 있는 일반 텍스트 파일입니다. 헤더 파일에는 다음 정보가 포함될 수 있습니다.

**`변수`** - 객체 지향 프로그래밍(OOP)의 경우 클래스 헤더 파일에는 구현 소스 코드 파일에서 액세스할 수 있는 모든 클래스 수준 변수의 정의가 포함됩니다.
**`메소드 선언`** - 모든 메서드 선언은 여러 구현 파일에서 액세스할 수 있도록 .h 헤더 파일에 포함됩니다.
**`비인라인 함수 정의`** - 헤더 파일에는 인라인이 아닌 메서드의 정의도 포함될 수 있습니다.
**`Message Maps`** - 헤더 파일에는 MFC 소스 코드 구현의 경우 메시지 맵도 포함될 수 있습니다. 이러한 경우 메시지 맵은 버튼, 체크박스, 라디오 버튼 등과 같은 UI 요소에 연결된 기능 구현에 연결됩니다.


### 헤더 가드

헤더 파일은 다른 헤더 파일을 추가한 결과로 동일한 파일에 여러 선언이 포함되는 복잡한 오류를 일으킬 수 있습니다. 이 중복 정의는 컴파일러 오류를 발생시킵니다. 이 문제 상황은 아래와 같이 조건부 컴파일 지시문인 헤더 가드라는 메커니즘을 통해 피할 수 있습니다.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
이 헤더를 사용하여 전처리기는 `ANY_UNIQUE_NAME_HERE`가 이미 정의되었는지 여부를 확인합니다. 헤더가 동일한 파일에 반복적으로 포함되면 헤더의 내용은 무시됩니다.

## H 파일 예

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

## 참고문헌

* [헤더 파일러 - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

