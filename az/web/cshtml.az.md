{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"cshtml faylı",
"cshtml fayl formatı",
"cshtml fayl növü",
"fayl",
"növü",
"cshtml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML - ASP.NET Razor Veb səhifəsi",
  "description": "CSHTML fayl formatı və CSHTML fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-azl"
}
},
  "lastmod": "2021-04-29"
}

## CSHTML faylı nədir?

.cshtml uzantısı olan fayl istifadəçinin brauzerinə veb-səhifə fayllarını göstərmək üçün Razor İşarələmə mühərriki tərəfindən server tərəfində istifadə edilən [C#](/programming/cs/) HTML faylıdır. Bu server tərəfində kodlaşdırma standart ASP.NET səhifəsinə bənzəyir və veb-səhifə brauzerə yazılarkən dinamik veb məzmunu yaratmağa imkan verir. Yaradılan səhifəni brauzerə göndərməzdən əvvəl server səhifə daxilində server tərəfi kodunu yerinə yetirir. Verilənlər bazasına daxil olmaq və mürəkkəb görünüşləri göstərmək kimi mürəkkəb tapşırıqlar. CSHTML faylları Microsoft Visual Studio istifadə edərək yaradıla və proqramlaşdırıla bilər.

## CSHTML fayl formatı

CSHTML faylları Razor işarələmə mühərriki tərəfindən qeyd olunan sintaksisə əməl edən mətn fayllarıdır. Razor həm C#, həm də VB.NET-i dəstəkləyir və onu öyrənmək və istifadə etmək klassik ASP və ASP.NET ilə müqayisədə asandır. w3schools Razorun [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kodlaşdırılması üçün sadə, lakin effektiv bələdçiyə malikdir.

### CSHTML Nümunəsi

Aşağıda Razor üçün CSHTML faylında istifadə edilən C# Kod nümunəsidir.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Razor üçün ekvivalent VB.NET kodu aşağıdakı kimidir.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## İstinadlar

* [Razor Sintaksis Referansı - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


