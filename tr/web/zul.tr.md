{
  "date" : "2021-05-24",
  "keywords" :["zul", "Dosya", "Uzantı", "Dosya Formatı", "Dosya Uzantısı", "aç"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK Kullanıcı Arayüzü Dosyası",
  "description":"ZUL dosya formatı ve ZUL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ZUL dosyası nedir?

.zul uzantılı bir dosya, Kullanıcı Arayüzü Biçimlendirme Dili (ZUML) ile oluşturulan bir web dosyasıdır ve kullanıcı arayüzü öğeleri için tanımları içerir. Ajax ve Java sınıfları, sunucu tarafı dosyaları geliştirmek için [XML](/tr/web/xml/) tabanlı ZUML kullanımını destekler. ZUL dosya formatı, JavaScript veya AJAX bilgisi olmadan web ve mobil uygulamalar oluşturmanıza olanak sağlayan bir UI çerçevesi olan ZK tarafından geliştirilmiştir.

## ZUL Dosya Biçimi

ZUL dosyaları, kullanıcı arabirimi oluşturmak için farklı öğelerden oluşan XML tabanlıdır. ZK yükleyici, bir bileşen oluşturmak için her bir XML öğesini kullanır. Sayfa başlığı, açıklama vb. gibi sayfa öğelerinin genel olarak işlenmesi, ZUML'nin her bir XML işleme talimatı tarafından açıklanır.

### ZUL Örneği

Aşağıdaki ZUML kodu örneğinde, ilk satır sayfa başlığını belirtir, ikinci satır başlık ve kenarlıklı bir kök bileşen oluşturur ve üçüncü satır etiketli bir düğme ve bir olay dinleyicisi oluşturur.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL şeması http://www.zkoss.org/2005/zul/zul.xsd adresinden indirilebilir.
## Referanslar

* [ZUL - ZK Tarafından](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL Şeması](http://www.zkoss.org/2005/zul/zul.xsd)

