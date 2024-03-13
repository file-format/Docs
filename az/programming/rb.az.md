{
  "date": "2023-05-29",
  "keywords": [
"rb faylı",
"rb faylı nədir",
"ruby skriptini rb faylında necə işlətmək olar",
"rb faylı nə ehtiva edir",
"rb faylının formatı nədir",
"fayl",
"rb fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "RB Fayl Format - Ruby Mənbə Kodu Faylı",
  "description": "RB faylları yarada və aça bilən RB formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb-az",
      "parent": "programming"
}
},
  "lastmod": "2023-05-29"
}

## RB faylı nədir?

.rb fayl uzantısı adətən Ruby proqramlaşdırma dili faylları ilə əlaqələndirilir. Ruby sadəliyi və oxunaqlılığı ilə tanınan dinamik, obyekt yönümlü proqramlaşdırma dilidir.

.rb faylı Ruby mənbə kodunu ehtiva edir, Ruby tərcüməçisi və ya Ruby inkişaf mühiti tərəfindən icra edilə bilər. Bu fayllar tez-tez siniflərin, metodların, dəyişənlərin və digər Ruby kod konstruksiyalarının təriflərini ehtiva edir.

## Ruby skriptini RB faylında necə işə salmaq olar?

.rb faylında saxlanılan Ruby skriptini işə salmaq üçün sisteminizdə quraşdırılmış Ruby tərcüməçisinə ehtiyacınız olacaq. Budur example.rb adlı faylda saxlanılan Ruby skriptinin əsas nümunəsi:

```
# example.rb

# Define a method to calculate the square of a number
def square(number)
  number * number
end

# Call the square method with an argument
result = square(5)

# Print the result
puts "The square of 5 is: #{result}"
```

Bu skripti işə salmaq üçün siz komanda xəttini və ya terminalınızı aça, example.rb faylının yerləşdiyi qovluğa gedə və sonra Ruby tərcüməçisindən istifadə edə bilərsiniz:

```
ruby example.rb
```

Yuxarıdakı əmrin yerinə yetirilməsi skripti işlədəcək və çıxış konsolda görünəcək:

```
The square of 5 is: 25
```

Bu sadə bir nümunədir, lakin .rb faylları tam hüquqlu Ruby proqramlarını qurmağa imkan verən siniflər, modullar və idarəetmə strukturları daxil olmaqla daha mürəkkəb kodu ehtiva edə bilər.

## RB faylında nə var?

.rb faylının xüsusi məzmunu onun məqsədindən və onu yazan proqramçıdan asılı olaraq dəyişə bilər. Bununla belə, ümumiyyətlə, .rb faylı Ruby tərcüməçisinin başa düşə və icra edə biləcəyi bir sıra təlimatlardan ibarət Ruby mənbə kodunu ehtiva edir.

Ruby faylında tapa biləcəyiniz bəzi ümumi elementlər bunlardır:

- **Şərhlər:** Ruby həm tək sətirli, həm də çox sətirli şərhləri dəstəkləyir. Şərhlər izahlı qeydlər əlavə etmək və ya xüsusi kod sətirlərini icradan çıxarmaq üçün istifadə olunur. Onlar # simvolu ilə işarələnir.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **Dəyişən bəyannamələri:** Ruby dinamik tipli dildir, ona görə də dəyişənlərin açıq tip bəyannaməsinə ehtiyac yoxdur. Siz təyinetmə operatorundan (=) istifadə edərək dəyişənlərə qiymətlər təyin edə bilərsiniz.

- **Metodlar:** Ruby xüsusi tapşırıqları yerinə yetirən təkrar istifadə edilə bilən kod blokları olan metodları müəyyən etmək üçün `def` açar sözündən istifadə edir.

- **Siniflər və Obyektlər:** Ruby obyekt yönümlü bir dildir və siniflər obyekt planlarını müəyyən etmək üçün istifadə olunur. Obyektlər siniflərin nümunələridir və atributları (nümunə dəyişənləri) və davranışları (nümunə üsulları) ola bilər.

- **Control Structures:** Ruby proqramda icra axınına nəzarət etmək üçün şərti ifadələr (əgər, else, elsif, istisna olmaqla), looplar (while, until, for, every) və daha çox kimi müxtəlif idarəetmə strukturlarını təmin edir.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## RB faylının formatı nədir?

.rb faylının formatı düz mətndir, adətən UTF-8 və ya ASCII kodlaşdırması ilə kodlanır. O, Ruby proqramlaşdırma dili ilə müəyyən edilmiş spesifik sintaksis və strukturu izləyir.

## RB faylının MIME növü nədir?

- `tətbiq/x-ruby`

## İstinadlar
* [Ruby (programming language)](https://en.wikipedia.org/wiki/Ruby_(programming_language))
