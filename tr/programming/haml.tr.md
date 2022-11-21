{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML Dosya Biçimi - Haml Kaynak Kod Dosyası",
  "description":"HAML dosya formatı ve HAML dosyası oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## HAML dosyası nedir?

HAML dosyası, [Haml](https://haml.info/) dilinde yazılmış kaynak kodunu içeren bir HTML soyutlama biçimlendirme dili dosyasıdır. ERB'nin (Ruby şablon betikleri) yerine kullanılabilir. HAML dosyası, bir web belgesinin HTML'sini oluşturmak için şablon kaynak kodunu içerir. ERB dosyaları, dosyanın uzantısı değiştirilerek app/views klasöründeki bu dosyaların Haml olarak değiştirilmesiyle değiştirilebilir. HAML dosyaları, Microsoft Notepad, Notepad++, Apple TextEdit gibi herhangi bir metin düzenleyiciyle açılabilir.

## HAML Dosya Biçimi

HAML dosyaları, diske düz metin dosyaları olarak kaydedilen kaynak dosyalardır. HAML sözdiziminde yazılmış kod içerir. HAML, kodu daha basit ve kolay hale getirmek için **<>** etiketlerini **%** işaretiyle değiştirir. ERB dosyaları, aşağıdaki basit örnekte gösterildiği gibi, HAML tarafından değiştirilebilir.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Örneği

Aşağıda bir örnek Hello World HAML örneği verilmiştir.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
bu da aşağıdaki HTML çıktısına dönüşür.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referanslar

* [HAML - Github](https://github.com/haml/haml)

