{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML Dosya Biçimi - Bean İşaretleme Dili Dosyası",
  "description":"BML dosya formatı ve BML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## BML dosyası nedir?

.bml uzantılı bir dosya, Java uygulamalarını desteklemek için Java sınıflarını depolayan bir Bean İşaretleme Dili dosyasıdır. Bu, Java nesnelerine ve yöntemlerine erişim sağlar ve Java sınıflarını kullanarak yeni işlevler oluşturmaya gerek yoktur. Yararlı görevleri gerçekleştirmek için bileşenlerin birbirine nasıl bağlandığını belirtir. BML, yapıları ve bileşen ilişkilerini açıklamak için IBM alphaWorks tarafından geliştirilmiştir. BML dosyaları, Web Tarayıcıları, Microsoft Notepad ve Notepad++ gibi herhangi bir metin düzenleyici kullanılarak açılabilir ve görüntülenebilir.

## BML Dosya Biçimi

IBM alphaworks web sitesi, BML'nin iki uygulamasını sağlamıştır. İlk uygulama, istenen fasulye hiyerarşisini oluşturmak için bir BML betiğini 'oynatan' bir yorumlayıcıdır. İkinci uygulama, herhangi bir BML betiğini yansımasız Java kodunda derleyen bir derleyicidir. Bu, uygulamanın bileşenler arası yapısının, bu özel amaç için tasarlanmış bir dil kullanılarak yakalanmasına ve onu 'normal' Java koduna derleme yeteneğinin eklenmesine olanak sağlaması açısından avantajlıdır.

## BML Etiketleri

BML dilinde kullanılan bazı etiketlerin açıklamaları aşağıdadır:

###<bean> etiket:

bu<bean> eleman, yeni çekirdekler oluşturmak veya fasulyeleri adıyla aramak için kullanılır. bu<bean> etiketi şu biçimdedir:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Etiketteki "id", JavaBean için nesne kaydıyla ilişkilendirilir.

###<string> etiket

string etiketinin kullanılmasının iki yolu vardır:

1. Boş olmayan bir dizi oluşturmak için:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Boş bir dizi oluşturmak için:

```
<string/>
```
## Referanslar

* [XML ile Nesne Yönelimli Mesajlaşma](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Fiziksel İşaretleme Dili](http://web.mit.edu/mecheng/pml/standards.htm)
* [Bean İşaretleme Dili](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

