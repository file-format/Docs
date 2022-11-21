{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml dosyası", "dhtml dosya biçimi", "dhtml dosya türü", "dosya", "tür", "dhtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Dinamik HTML Dosya Biçimi",
  "description":"DHTML dosya formatı ve DHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## DHTML dosyası nedir?

.dhtml uzantılı bir dosya, bir web sayfasının dinamik içeriğini oluşturmak için kullanılan dinamik bir [HTML](/tr/web/html/) dosyasıdır. DHTML'de oluşturulan bir web öğesi olaya dayalıdır ve sayfanın yeniden yüklenmesini gerektirmez. Çoğu durumda, bir web sayfasının açılır menüler, kayan katmanlar, rollover düğmeleri ve diğer dinamik içerik gibi dinamik içeriklerini oluşturmak için bir DHTML dosyası kullanılır. Hayatınızda neredeyse her gün farenizi bir menü öğesinin üzerine getirdiğinizde dinamik html öğeleriyle karşılaşırsınız ve bu, daha fazla alt menü seçeneği açar. DHTML, dinamikliği elde etmek için [HTML](/tr/web/html/), [Javascript](/tr/web/js/), HTML DOM, HTML Events ve [CSS](/tr/web/css/) gibi web teknolojilerinden yararlanır. elemanların davranışı.

## DHTML Dosya Biçimi

DHTML dosyaları, web öğelerinin dinamik davranışını uygulamak için DHTML kodu içeren düz metin dosyalarıdır.


### DHTML DOM'u

DHTML Belge nesne Modeli (DOM), aşağıdaki resimde gösterildiği gibi öğeler, nitelikler ve metin içeren bir ağaç yapısı olan HTML DOM'u temel alır.

{{< figure src="../dhtml.png" alt="HTML DOM'u" >}}

"Belge" düğümü, farklı işlevleri uygulamak üzere çeşitli işlevleri çağırmak için kullanılabilir. Aşağıdaki örnek, DHTML'deki JavaScript'in document.write() yöntemini kullanır.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Bu kod, tarayıcıda çıktı almak için "Merhaba Dünya" metnini yazar.

### DHTML Etkinlikleri

|S.No.|Olay|Olay|
---|---|---|
|1|onaport|Kullanıcı sayfayı veya medya dosyasını yüklemeyi durdurduğunda gerçekleşir.|
|2|onblur|Kullanıcı bir HTML nesnesinden ayrıldığında oluşur.|
|3|onchange|Kullanıcı bir nesnenin değerini değiştirdiğinde veya güncellediğinde oluşur.|
|4|onclick|Herhangi bir kullanıcı bir HTML öğesini tıkladığında oluşur veya tetiklenir.|
|5|ondblclick|Kullanıcı bir HTML öğesini iki kez birlikte tıkladığında oluşur.|
|6|odaklanma|Kullanıcı bir HTML öğesine odaklandığında gerçekleşir. Bu olay işleyici, onblur'un karşısında çalışır.|
|7|onkeydown|Kullanıcı klavye cihazında bir tuşa bastığında tetiklenir. Bu olay işleyici tüm anahtarlar için çalışır.|
|8|onkeypress|Kullanıcılar klavyede bir tuşa bastığında tetiklenir. Bu olay işleyici, tüm anahtarlar için tetiklenmez.|
|9|onkeyup|Kullanıcı bir nesneye veya öğeye bastıktan sonra klavyeden bir tuşu bıraktığında meydana gelir.|
|10|onload|Bir nesne tamamen yüklendiğinde oluşur.|
|11|onmousedown|Kullanıcı bir HTML öğesi üzerinde farenin düğmesine bastığında oluşur.|
|12|onmousemove|Kullanıcı imleci bir HTML nesnesi üzerinde hareket ettirdiğinde oluşur.|
|13|onmouseover|Kullanıcı imleci bir HTML nesnesi üzerine getirdiğinde oluşur.|
|14|onmouseout|Fare işaretçisi bir HTML öğesinin dışına taşındığında oluşur veya tetiklenir.|
|15|onmouseup|Bir HTML öğesi üzerinde fare düğmesi bırakıldığında oluşur veya tetiklenir.|
|16|onreset|Kullanıcı tarafından formu sıfırlamak için kullanılır.|
|17|onselect|Bir web sayfasında içerik veya metin seçildikten sonra oluşur.|
|18|onsubmit|Form gönderildikten sonra kullanıcı bir butona tıkladığında tetiklenir.|
|19|onunload|Kullanıcı bir web sayfasını kapattığında tetiklenir.|

## Referanslar

* [Dinamik HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

