{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","ah dosyası nedir","h dosyası nasıl açılır", "uzantı", "dosya", "h dosyası","h dosya formatı", "h dosya uzantısı", "H Dosya Örneği"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ Başlık Dosyası Biçimi",
  "description":"H dosya formatı ve H dosyasını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## H dosyası nedir?

**h dosya uzantısıyla** kaydedilen bir dosya, C/C++ dosyalarında değişkenlerin, sabitlerin ve işlevlerin bildirimini içermek için kullanılan bir başlık dosyasıdır. Bunlara, bu işlevlerin gerçek uygulamasını içeren [C++](/tr/programming/cpp/) uygulama dosyaları tarafından başvurulur. Bir .h başlık dosyası, Makro tanımları gibi ek bilgiler de içerebilir. Bu başlık dosyalarına C/C++ dosyalarında '#include' yönergesi kullanılarak başvurulur.

Yeni bir C++ projesi genellikle tüm derleme zincirleri için başlangıç noktası olan **stdafx.h** dosyası adında özel bir başlık dosyası içerir ve tüm başlık dosyaları bu tek dosyaya dahil edilebilir. Bir .h dosyası herhangi bir metin düzenleyici, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ derleyici ve diğer birçok uygulama ile açılabilir.

## .H Dosya Biçimi

.h dosyası, sözdizimini tanımlamak için kendi kurallarına sahip düz metin dosyasıdır. Başlık dosyaları aşağıdaki bilgileri içerebilir.

**`Değişkenler`** - Nesne Yönelimli Programlama (OOP) durumunda, bir sınıf başlık dosyası, uygulama kaynak kodu dosyalarından erişilebilen tüm sınıf düzeyindeki değişkenlerin tanımlarını içerir
**`Metot Bildirimi`** - Tüm yöntem bildirimleri, birden çok uygulama dosyasında erişilebilmesi için .h başlık dosyalarına dahil edilmiştir.
**`Satır İçi Olmayan İşlev Tanımları`** - Başlık dosyaları, satır içi olmayan yöntemlerin tanımlarını da içerebilir.
**`Message Maps`** - Bir başlık dosyası, bir MFC kaynak kodu uygulaması durumunda mesaj haritaları da içerebilir. Bu durumda, mesaj haritaları, düğme, onay kutusu, radyo düğmeleri vb. gibi UI öğelerine bağlı olan işlevsellik uygulamasına bağlıdır.


### Başlık Muhafızları

Başlık dosyaları, diğer başlık dosyalarının eklenmesinin bir sonucu olarak aynı dosyaya birden çok bildirimin dahil edildiği karmaşık hatalara neden olabilir. Bu yinelenen tanımlar, derleyici hatalarına neden olur. Bu problemli durum, aşağıda gösterildiği gibi koşullu derleme direktifleri olan başlık koruması adı verilen bir mekanizma ile önlenebilir.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Bu başlık ile ön işlemci, "ANY_UNIQUE_NAME_HERE" öğesinin zaten tanımlanıp tanımlanmadığını kontrol eder. Başlık aynı dosyaya tekrar tekrar dahil edilirse, başlığın içeriği göz ardı edilir.

## H Dosya Örneği

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

## Referanslar

* [Başlık Dosyalayıcıları - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

