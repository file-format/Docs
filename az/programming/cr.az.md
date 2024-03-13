{
  "date" : "2024-03-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR Fayl - Crystal Source Code - .cr fayl nədir və onu necə açmaq olar?",
  "description" : "CR Crystal Source Code Faylı və onun necə açılacağını öyrənin.",
  "linktitle" : "CR",
  "menu" : {
    "docs" : {
      "identifier" : "programming-cr-az",
      "parent" : "programming"
}
},
  "lastmod" : "2024-03-08"
}

## CR faylı nədir?

CR faylı adətən Crystal proqramlaşdırma dilinin mənbə kodu faylına istinad edir. Crystal Ruby-dən ilhamlanmış sintaksisi olan statik tipli, tərtib edilmiş bir dildir. CR faylının nəyi ehtiva edə biləcəyinə dair sadə bir nümunə:

```
# This is a comment
class Greeter
  def initialize(@name : String)
  end

  def greet
    puts "Hello, #{@name}!"
  end
end

greeter = Greeter.new("World")
greeter.greet
```

Crystal yüksək performans və növ təhlükəsizliyi təklif edən Ruby-yə bənzər sintaksisi olan statik tipli, tərtib edilmiş proqramlaşdırma dilidir. O, paralelliyi, metaproqramlaşdırmanı dəstəkləyir və təhlükəsizliyi vurğulayır. Kristal çarpaz platformadır və böyüyən kitabxanalar və çərçivələr ekosisteminə malikdir.

## CR faylını necə açmaq olar?

CR faylını açmaq üçün siz Kristal sintaksisinin işıqlandırılmasını və redaktəsini dəstəkləyən istənilən mətn redaktorundan və ya inteqrasiya olunmuş inkişaf mühitindən (IDE) istifadə edə bilərsiniz. Budur bəzi ümumi seçimlər:

1.  **Visual Studio Kodu**: Sintaksis vurğulanması və digər dil xüsusiyyətləri üçün Crystal Language genişləndirilməsini quraşdırın.
    
2.  **Atom**: Kristal dil dəstəyi üçün dil-kristal paketini quraşdırın.
    
3.  **Sublime Text**: Sintaksis vurğulamaq və digər Kristala xas xüsusiyyətlər üçün Crystal Language paketindən istifadə edin.
    
4.  **Vim**: Crystal sintaksisinin vurğulanması və redaktə dəstəyi üçün vim-kristal kimi plaqini quraşdırın.
    
5.  **Emacs**: Kristal sintaksisinin işıqlandırılması və redaktə imkanları üçün kristal rejimi kimi paket quraşdırın.
    

Bu redaktorlardan və ya IDE-lərdən birini quraşdırdıqdan sonra siz sadəcə olaraq hər hansı digər mətn faylı kimi `.cr` faylını aça bilərsiniz və siz Crystal mənbə koduna baxa və redaktə edə biləcəksiniz.

## İstinadlar
* [Crystal (programming language)](https://en.wikipedia.org/wiki/Crystal_(programming_language))
