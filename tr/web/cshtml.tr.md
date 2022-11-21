{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml dosyası", "cshtml dosya biçimi", "cshtml dosya türü", "dosya", "tür", "cshtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor Web Sayfası",
  "description":"CSHTML dosya formatı ve CSHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## CSHTML dosyası nedir?

.cshtml uzantılı bir dosya, sunucu tarafında Razor Markup motoru tarafından web sayfası dosyalarını kullanıcının tarayıcısına işlemek için kullanılan bir [C#](/tr/programming/cs/) HTML dosyasıdır. Bu sunucu tarafı kodlaması, standart ASP.NET sayfasına benzer ve web sayfası tarayıcıya yazılırken anında dinamik web içeriği oluşturulmasını sağlar. Sunucu, oluşturulan sayfayı tarayıcıya göndermeden önce sayfanın içindeki sunucu tarafı kodunu yürütür. Veritabanlarına erişme ve karmaşık görünümleri işleme gibi karmaşık görevler. CSHTML dosyaları Microsoft Visual Studio kullanılarak oluşturulabilir ve programlanabilir.

## CSHTML Dosya Biçimi

CSHTML dosyaları, Razor biçimlendirme motoru tarafından belirtilen sözdizimini izleyen metin dosyalarıdır. Razor hem C# hem de VB.NET'i destekler ve öğrenmesi ve kullanması klasik ASP ve ASP.NET'ten daha kolaydır. w3schools, Razor'un [C# ve VB.NET söz dizimi](https://www.w3schools.com/asp/razor_syntax.asp) kodlaması için basit ama etkili bir kılavuza sahiptir.

### CSHTML Örneği

Razor için bir CSHTML dosyasında kullanılan C# Kodu örneği aşağıdadır.

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

Razor için eşdeğer VB.NET kodu aşağıdaki gibidir.

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

## Referanslar

* [Razor Söz Dizimi Referansı - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

