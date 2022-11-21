{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg dosyası", "apkg dosya biçimi", "apkg dosya türü", "dosya", "tür", "APKG dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Destesi Dosya Biçimi",
  "description" :"APG dosyası nedir ve bunları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## APKG dosyası nedir?

.apkg uzantılı bir dosya, bilgi kartı tabanlı bir öğrenme programı olan [Anki](https://ankiweb.net/about) yazılım uygulamasında kullanılmak üzere oluşturulmuş bir bilgi kartı destesidir. Anki uygulamasında yüklenip görüntülenecek [HTML](/tr/web/html/) metni içerir ve ayrıca görsel ve işitsel öğrenme için resimlere ve seslere sahip olabilir. Anki, kullanıcıların kendi Anki bilgi kartı destelerini oluşturmalarına ve diğer kullanıcıların bilgi kartı destelerini içe aktarmalarına olanak tanır.

## APKG Dosya Biçimi

Anki kart desteleri, web sayfaları oluşturmak için ünlü ve yaygın bir dil olan HTML ile yazılmış şablonlardan oluşturulur. Güverte kartlarının stili, web sayfalarını tasarlamak için kullanılan dil olan CSS kullanılarak yapılır. Stil, aşağıdakilere yönelik değişiklikleri içerir:

* font-family - Kartta kullanılacak fontun adı.
* yazı tipi boyutu - Yazı tipinin piksel cinsinden boyutu.
* text-align - Metnin ortaya mı, sola mı yoksa sağa mı hizalanması gerektiğini tanımlar.
* renk - "mavi", "kırmızı" gibi basit renk adları veya HTML renk kodları olabilen metnin rengini tanımlar.
* background-color - Kartın arka plan rengini tanımlar

Stil bilgileri tüm kartlar arasında paylaşılır ve bir değişiklik yapıldığında tüm kartları etkiler. Aşağıdaki örnek, ilki hariç tüm kartlarda sarı bir arka plan kullanacaktır:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Bir Anki kartında yeniden boyutlandırılan görüntüler aşağıdaki gibi kontrol edilebilir.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript'i Anki kartlarına gömme

Kart şablonları kullanılarak [Javascript](/tr/web/js/) bir Anki kartına gömülebilir. Ancak, Javascript'in ileri düzeyde olması nedeniyle desteği sağlanmamaktadır. Ayrıca, işleme cihazları, Javascript'in uygulama etkilerini kartta farklı gösterebilir, bu da uygulamanın tüm cihazlarda test edilmesi ihtiyacını doğurur. Window.alert gibi belirli Javascript özellikleri, yazdığınız Javascript kodunda hata ayıklamayı zorlaştırır.

## Referanslar ##

* [Anki Belgeleri](https://docs.ankiweb.net/intro.html)

