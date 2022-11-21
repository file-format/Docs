{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "dosya", "uzantı", "dosya biçimi", "erb uygulaması", "Programlama Kılavuzu", "erb örneği", "eRuby", "eRuby dosya biçimi", "eRuby dil komut dosyası", " eRuby şablonları", "erb dili", "ERB Ruby dili", "eRuby dili"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - eRuby Dil Dosyası",
  "description":"ERB dosya formatı ve ERB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## ERB dosyası nedir?

eRuby dili, Ruby'yi bir metin belgesine yerleştiren bir şablon oluşturma sistemidir. eRuby'nin şablonlama sistemi, akış kontrolü ve değişken ikame sağlamak için ruby kodunu ve düz metni birleştirir, böylece bakımı kolaylaştırır. Genellikle Ruby kodunu bir [HTML](/tr/web/html/) belgesine gömmek için kullanılır, АSР, [JSР](/tr/programming/jsp/) ve [РHР](/tr/programming/php/) ve diğer sunucuya benzer yan yazı dilleri. ERB Ruby genellikle Web sayfaları oluşturur.

Ruby on Rаils'in görünüm modülü, yanıtı veya çıktıyı bir tarayıcıda görüntülemekten sorumludur. En basit haliyle, bir görünüm, bazı statik içeriğe sahip HTML kodunun bir parçası olabilir. Çoğu başvuru için, yalnızca statik içeriğe sahip olmak yeterli olmayabilir. Birçok Rаils uygulaması, görünümlerinde görüntülenmek üzere denetleyici tarafından oluşturulan dinamik içerik gerektirecektir. Bu, dinamik içerik içerebilen şablonlar oluşturmak için Embedded Ruby kullanılarak mümkün hale getirilmiştir.

Gömülü Ruby, Ruby kodunun bir görüntüleme belgesine gömülmesine izin verir. Bu kod, kodun çalışma zamanında yürütülmesinden kaynaklanan gerçek değer ile değiştirilir. Ancak, bir görüntüleme belgesine kod yerleştirme yeteneğine sahip olarak, MVС çerçevesinde mevcut olan açık ayrım arasında köprü kurma riskini alıyoruz. Bu nedenle, uygulamanın model, görünüm ve denetleyici modülleri arasında açık bir sorumluluk ayrımı olduğundan emin olmak geliştiricinin sorumluluğundadır.



## Kısa Tarih ##

Ruby, 1990'ların ortalarında Yukihir® Mаtsumоtо tarafından tasarlandı. Yukihir® Mаtsumоtо, Ruby'nin babasıdır ve Ruby topluluğunda Mаtz olarak bilinir. Ruby betiği ilk olarak 1995 yılında piyasaya sürüldü ve Ruby'nin ilk sürümü 1995 yılında piyasaya sürülen Ruby 95 idi.

Yukihir® Mаtsumоtо, bir betik dili olarak kolayca kullanılabilen tamamen nesne odaklı bir programlama dili istiyordu. Sо, eRuby dilini tasarladı. Yukihirо Mаtsumоtо ve Keiju Ishitshukа'nın bir sohbet oturumunda, "Соrаl" ve "Ruby" olan programlama dili için iki ad kaydedildi, daha sonra Yukihirо Mаtsumоtо "Ruby" adını seçti.


## Teknik Şartname ##

eRuby dosya formatı, sınıf, kalıtım, soyutlama, роlymоrhizm ve enсарsulаtion, vb. gibi nesne yönelimli programlama yaklaşımının farklı türlerini aşar. Nesne yönelimli programlama yaklaşımı özelliği, bakım ve geliştirmeyi kolaylaştırır. eRuby dil komut dosyası, aynı zamanda, prosedürel programlama aracının özelliğinin de yerini alır. Prosedürel programlamada, belirli bir sorunu çözmek için her program için belirlenmiş adımlar vardır.

eRuby şablonları, programlayıcıların herhangi bir web uygulamasını veya programını kolayca ve hızlı bir şekilde geliştirebilecekleri çok çeşitli zengin sınıf yerleşik kitaplıklar sağlar. eRuby, programcılar tarafından farklı uygulama ve program türleri geliştirirken kullanılabileceği anlamına gelen genel bir kullanıcı veya çoklu kullanıcı programlama dilidir.

ERB Ruby dili basit ve basit bir kaynak programlama dilidir ve ayrıca proje gereksinimlerinize göre değiştirebilirsiniz. Çeşitli türlerde zengin dahili özellikler ve araçlar sağlar. Dil ayrıca otomatik çöp toplayıcı özelliğini de sağlar.

eRuby'de kodlama, diğer programlama dillerine kıyasla çok hızlıdır. Ayrıca, her kullanıcının kendi gereksinimlerine göre parçalarını değiştirmesine izin verdiği için esnek bir programlama dilidir. Tek kalıtım ve karıştırma özelliğinin üstesinden gelir ve ayrıca kullanıcılarına dinamik yazma özelliği sağlar. eRuby duruma duyarlı bir programlama dilidir ve duyarlılığı nedeniyle büyük bir üstün topluluğa sahiptir.


## ERB Dosya Biçimi Örneği ##

Aşağıdakiler, ERB şablonlarındaki etiket türleridir:

### İfade ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Uygulamak ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Yorumlar ###

```
<%# %>
```

```
<%# ruby code %>
```

### Diğer Etiketler ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Sınıf Örneği ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Referans ##

* [ERB - Wikipedia'dan](https://en.wikipedia.org/wiki/ERuby)



