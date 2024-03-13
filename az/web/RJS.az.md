{
  "date": "2021-05-24",
  "keywords": [
"rjs",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"RJS",
"Ruby Javascript Faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RJS - Ruby Javascript faylı",
  "description": "RJS fayl formatı və RJS faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "RJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-RJ-azS"
}
},
  "lastmod": "2021-05-24"
}

## RJS faylı nədir?

.rjs uzantısı olan fayl Ruby kodu və JavsScript-in birləşməsidir ki, Rails tərtibatçılarına dinamik JavaScript kodu yaratmaq üçün Ruby-dən istifadə etməyə imkan verir. Ruby kodu Java funksiyalarına daxil edilmişdir və Ruby mühərrikinin serverdə işləməsini tələb edən veb serverdə tərtib edilmişdir. RJS [RHTML](/web/rhtml/) ilə oxşardır; yeganə fərq odur ki, yanal [HTML](/web/html/)-də Ruby kodunu, Javascript funksiyalarında isə Ruby kodunu ehtiva edir.

## RJS fayl formatı

RJS faylları hər hansı digər skript və ya proqramlaşdırma dili kimi düz mətnlə kodlanır. Müştəri tərəfindən belə bir səhifə tələb edildikdə, Ruby kodu serverdə yerinə yetirilir və müştərinin brauzerinə yalnız HTML və Javascript kodu qaytarılır. RJS faylının sintaksisi Ruby və JavaScript sintaksisinin birləşməsinə bənzəyir ki, JavaScript funksiyalarına yalnız Ruby kodu daxil edilib.

### RJS nümunəsi

Aşağıdakı nümunə müstəqil olaraq sadə Ruby kodunu göstərir və sonra JavaScript funksiyasına daxil edilir.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
və aşağıdakı RubyJS-dir:
```Ruby
# here you go!

foo = -> { "bar" }
```
## İstinadlar

* [RJS](https://github.com/makevoid/rjs)


