{
  "date": "2023-05-15",
  "keywords": [
"csx faylı",
"csx faylı nədir",
"csx faylında nə var",
"csx faylının formatı nədir",
"fayl",
"csx fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CSX Fayl Format - Visual C# Script",
  "description": "CSX faylları yarada və aça bilən CSX formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx-az",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## CSX faylı nədir?

Visual C# Script (həmçinin CSX kimi tanınır) Microsoft-un .NET ekosistemində Roslyn skript mühərriki tərəfindən istifadə edilən fayl formatıdır. CSX faylları ayrıca tərtib addımına ehtiyac olmadan birbaşa icra edilə bilən C# kodunu ehtiva edir.

CSX formatı Microsoft ekosisteminə xasdır və ümumi proqramlaşdırmada geniş istifadə olunan fayl formatı deyil. CSX faylları tez-tez tez prototipləşdirmə və ya skript funksiyasının tələb olunduğu ssenarilərdə istifadə olunur. Onlar sizə tam hüquqlu tərtib edilmiş proqram yaratmaqla müqayisədə C# proqramlarını daha yüngül formada yaratmağa və işlətməyə imkan verir.

CSX fayllarını icra etmək üçün siz C# kodunu işlətmək üçün interaktiv mühit təmin edən .NET Interactive Notebooks kimi alətlərdən istifadə edə bilərsiniz. C# genişləndirilməsi və .NET Core SDK ilə Visual Studio Kodu da CSX faylları ilə işləmək üçün istifadə edilə bilər.

## CSX faylında nə var?

CSX (C# Script) faylı birbaşa icra oluna bilən C# kodunu ehtiva edir. O, dəyişən bəyannamələri, funksiyalar, siniflər və digər proqramlaşdırma konstruksiyaları kimi istənilən etibarlı C# kodunu daxil edə bilər.

CSX faylında nələrin ola biləcəyinə dair bir nümunə:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX fayllarına kodun funksionallığını dəstəkləmək üçün idxal bəyanatları, xarici kitabxana istinadları və digər C# dili xüsusiyyətləri də daxil ola bilər. Kod kompilyasiyaya ehtiyac olmadan anında təfsir edilir və icra olunur, bu da onu skript və sürətli prototipləmə tapşırıqları üçün uyğun edir.

## What is the format of CSX file?

CSX (C# Script) formatı sadə mətn əsaslı formatı izləyir. Onu adi C# mənbə kodu fayllarından (.cs) fərqləndirmək üçün adətən .csx fayl uzantısına malikdir.

CSX faylları hər hansı mətn redaktoru və ya C# sintaksisinin vurğulanmasını dəstəkləyən inteqrasiya edilmiş inkişaf mühitindən (IDE) istifadə etməklə redaktə edilə bilər. CSX faylı hazır olduqdan sonra o, .NET Interactive Notebooks, .NET Core komanda xətti interfeysi (CLI) və ya C# skript dəstəyi ilə IDE kimi alətlərdən istifadə etməklə icra oluna bilər.

## İstinadlar
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

