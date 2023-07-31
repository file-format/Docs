{
  "date" : "2019-10-11",
  "keywords" :[ "h",".h","ahファイルとは","hファイルの開き方","拡張子","ファイル","hファイル","hファイル形式","hファイル拡張子", "Hファイルの例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ ヘッダー ファイル形式",
  "description":"H ファイル形式と,H ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## H ファイルとは何ですか?

**h ファイル拡張子** で保存されたファイルは、変数、定数、および関数の宣言を含めるために C/C++ ファイルで使用されるヘッダー ファイルです。これらは、これらの関数の実際の実装を含む [C++](/programming/cpp/) 実装ファイルによって参照されます。 .h ヘッダー ファイルには、マクロ定義などの追加情報を含めることもできます。これらのヘッダー ファイルは、`#include` ディレクティブを使用して C/C++ ファイルで参照されます。

通常、新しい C++ プロジェクトには、すべてのコンパイル チェーンの開始点となる **stdafx.h** ファイルという名前の特別なヘッダー ファイルが含まれており、すべてのヘッダー ファイルをこの 1 つのファイルに含めることができます。 .h ファイルは、任意のテキスト エディタ、Eclipse IDE、Microsoft Visual Studio IDE、Borland C++ コンパイラ、およびその他の多くのアプリケーションで開くことができます。

## .H ファイル形式

.h ファイルは、構文を定義するための独自の規則を持つプレーン テキスト ファイルです。ヘッダー ファイルには、次の情報を含めることができます。

**`Variables`** - オブジェクト指向プログラミング (OOP) の場合、クラス ヘッダー ファイルには、実装ソース コード ファイル全体でアクセス可能なすべてのクラス レベル変数の定義が含まれます。
**`メソッド宣言`** - すべてのメソッド宣言は、複数の実装ファイルからアクセスできるように .h ヘッダー ファイルに含まれています。
**`非インライン関数定義`** - ヘッダー ファイルには、非インライン メソッドの定義を含めることもできます。
**`メッセージ マップ`** - MFC ソース コード実装の場合、ヘッダー ファイルにもメッセージ マップを含めることができます。このような場合、メッセージ マップは、ボタン、チェックボックス、ラジオ ボタンなどの UI 要素にリンクされている機能の実装にリンクされています。


### ヘッダーガード

ヘッダー ファイルは、他のヘッダー ファイルを追加した結果、同じファイルに複数の宣言が含まれる複雑なエラーを発生させる可能性があります。この重複した定義により、コンパイラ エラーが発生します。この問題は、以下に示す条件付きコンパイル ディレクティブであるヘッダー ガードと呼ばれるメカニズムによって回避できます。

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
このヘッダーを使用して、プリプロセッサは `ANY_UNIQUE_NAME_HERE` が既に定義されているかどうかを確認します。ヘッダーが同じファイルに繰り返し含まれている場合、ヘッダーの内容は無視されます。

## H ファイルの例

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

## 参考文献

* [ヘッダー ファイラー - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

