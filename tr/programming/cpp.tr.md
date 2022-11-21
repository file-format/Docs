{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "dosya", "uzantı", "dosya formatı", "C++", "Programlama Dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ Kaynak Kod Dosyası",
  "description":"CPP dosya formatı ve CPP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## C++ dosyası nedir?

CPP dosya uzantılı dosyalar, C++ programlama dilinde yazılmış uygulamalar için kaynak kodlu dosyalardır. Tek bir C++ projesi, uygulama kaynak kodu olarak birden fazla CPP dosyası içerebilir. Böyle bir proje, başlık (.h) dosyasında bildirilen yöntemlerin tüm tanımlarını içerdiklerinden CPP dosyaları olarak bilinen farklı dosya türlerinden oluşur. Bir bütün olarak C++ projesi, bir bütün olarak derlendiğinde yürütülebilir bir uygulamayla sonuçlanır.

## CPP Dosya Yapısı

Bir CPP dosya yapısı, başlık dosyalarına kıyasla basittir. Böyle bir uygulama dosyasının temel amacı, arabirimi uygulamadan ayırmaktır. Bu, bir başlık dosyasındaki tüm üye işlevlerin bildirimleri ve CPP dosyası içindeki ayrıntılarıyla sonuçlanır. Bir CPP uygulama dosyası, bir uygulama yazmak için basit bir dosya veya bir sınıf uygulaması olarak kullanılabilir.

### Bağımsız Uygulama

Bir CPP dosyası, bağımsız bir uygulama olarak kullanıldığında, başlık dosyasında yöntem bildirimi gerekmeden içindeki tüm uygulamaları içerebilir. Böyle bir uygulama, uygulama girişinin isteğe bağlı kullanıcı girişini bağımsız değişken olarak alan bir ana yöntemle yönetildiği uygulama dosyasında tanımlanan tüm yöntemlerden oluşur. Ayrıca, dosyada bildirilen herhangi bir yöntem tarafından kullanılacak C++ Standart Kitaplığından herhangi bir kitaplığı da içerebilir.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Sınıf Uygulaması

Nesne Yönelimli Programlamada (OOP), sınıf tanımı olarak bir CPP dosyası kullanılır. Böyle bir durumda, tüm sınıf veri üyeleri ve üye işlevleri başlık dosyası içinde bildirilir. Her başlık dosyası, standart kitaplık yöntemlerine de başvurabilir. Sınıf tanımı CPP dosyası, dosyanın başlangıcındaki bir içerme ifadesindeki başlık dosyasına atıfta bulunur. Çoğunlukla yazılım geliştiriciler, böyle bir sınıf uygulama dosyasının başına, dosyanın gerçek içeriği, yazarın ayrıntıları ve uygulama tarihi hakkında bilgi sağlayan yorumlar ekler. Bu gibi durumlarda, başlık uygulama dosyalarının adları aynı olmalıdır. Böyle bir başlık ve uygulama dosyası örneği aşağıdaki gibidir.

### Başlık dosyası

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP Uygulama Dosyası

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referanslar

* [Sınıf Uygulaması - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Class_implementation_file)

