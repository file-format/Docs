{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST Dosya Biçimi- reStructuredText Dosyası",
  "description":"RST dosya formatı ve RST dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## RST dosyası nedir?

Bir RST dosyası, öncelikle Python programlama topluluğunda kullanılan bir teknik dokümantasyon dosyası biçimidir. Dokümantasyon oluşturmak için düz metin belgelerine stiller ve biçimlendirme uygulayan reStructuredText biçimlendirme dilinde yazılmış bir metin dosyasıdır. RST dosyaları, uygulamanın teknik belgelerini oluşturmak için Python programları kodundaki yorumları ve diğer bilgileri kullanır. Ancak bunlar, basit web sayfalarına ve [e-Kitaplara](/tr/e-kitap/) dönüştürülebilen metinler de içerebilir. RST dosyalarını açmak için Github Atom, GNU Emacs (platformlar arası), Microsoft Notepad (Windows), Apple TextEdit (Mac) ve Vim (Linux) gibi metin editörleri kullanılabilir.

## RST Dosya Biçimi

RST dosyaları, reStructuredText biçimlendirme dilinde yazılmış kod içerir. Java için Javadoc'a benzer Python için bir dizi araç sağlayan Python Doc-SIG'nin (Documentation Special Interest Group) Docutils projesinin bir parçasıdır. RST dosya formatı için ayrıştırıcı, Docutils'e gömülüdür ve program belgelerine biçimlendirmek için Python programlarından bilgi çıkarabilir.

### reStructuredText RST Örneği

Aşağıdaki gibi RST dosya formatında yazılmış örnek bir metin alalım.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Bu metin Docutils gibi bir rST işlemciye girildiğinde, çıktı aşağıdaki gibidir.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referans ##

* [reStructuredText - Wikipedia'dan](https://en.wikipedia.org/wiki/ReStructuredText)

