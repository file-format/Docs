{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "RJS", "Ruby Javascript Dosyası"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript Dosyası",
  "description":"RJS dosya biçiminin ne olduğunu ve RJS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## RJS dosyası nedir?

.rjs uzantılı bir dosya, Ruby kodu ile JavsScript'in birleşimidir ve Rails geliştiricilerinin Ruby'yi kullanarak dinamik JavaScript kodu üretmesine olanak tanır. Ruby kodu, Java işlevlerine gömülüdür ve sunucuda Ruby motorunun çalışmasını gerektiren web sunucusunda derlenir. RJS, [RHTML](/tr/web/rhtml/) ile benzerdir; tek fark, yanalın [HTML](/tr/web/html/) içinde Ruby kodu içermesi, Javascript işlevlerinde ise Ruby kodu içermesidir.

## RJS Dosya Biçimi

RJS dosyaları, diğer herhangi bir betik veya programlama dili gibi düz metin olarak kodlanmıştır. İstemci tarafından böyle bir sayfa istendiğinde, Ruby kodu sunucuda yürütülür ve istemcinin tarayıcısına yalnızca HTML ve Javascript kodu döndürülür. RJS dosyasının sözdizimi, Ruby ve JavaScript sözdiziminin birleşimine benzer, öyle ki JavaScript işlevlerine yalnızca Ruby kodu gömülüdür.

### RJS Örneği

Aşağıdaki örnek, basit bir Ruby kodunu bağımsız olarak gösterir ve ardından bir JavaScript işlevine gömülür.

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
ve RubyJS aşağıdadır:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referanslar

* [RJS](https://github.com/makevoid/rjs)

