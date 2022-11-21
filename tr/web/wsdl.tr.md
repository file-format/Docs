{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL Dosya Biçimi - Web Hizmetleri Açıklama Dili Dosyası",
  "description":"WSDL dosyasının ne olduğu ve WSDL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## WSDL dosyası nedir?

WSDL dosyası, Web hizmetlerini açıklamak için XML dilinde yazılmış bir Web Hizmetleri Açıklama Dili dosyasıdır. Evrensel olarak kabul edilen bir formatta dış dünyaya bağlantı için uç noktalar veya arayüzler hakkında bilgi içerir. [WSDL dosya biçimi belirtimleri](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (W3C.org tarafından korunur), sahip olmak için veri alışverişi için veri akışlarının yayınlanmasına ilişkin koşulları tanımlar. bağlantı noktaları ve uç noktalar üzerinden uzaktan uygulama erişimi.

## WSDL Dosya Biçimi - Daha Fazla Bilgi

WSDL dosyaları, insanlar tarafından okunabilen ve içeriğini görüntülemek için herhangi bir metin düzenleyicide açılabilen XML dosyaları olarak kaydedilir.

## WSDL Hizmet Açıklaması

WSDL 2.0 dosya biçimi belirtimleri, WSDL hizmetini iki aşamadan oluşacak şekilde tanımlar:

- Soyut sahne
- Beton sahne

Açıklamanın ve bağımsız endişe tasarımlarının yeniden kullanılabilirliği bir Web hizmeti tarafından yönetilir. Bu, hizmet tarafından kullanılan türler (veri türü tanımları), mesajlar (iletilen veriler), işlemler (eylemler) ve protokoller dahil olmak üzere birkaç farklı türde öğe kullanılarak elde edilir. Bunların hepsi soyut düzeyde yönetilir. Aktarım ve kablo biçimi ayrıntılarının bağlanması, ortak bir arabirim uygulamak için uç noktaları bir arada gruplandıran bağlama tarafından belirlenir.

### WSDL hizmetleriyle arayüz oluşturmak için hangi teknolojiler kullanılabilir?

ASP.NET, C/C++ ve Java uygulamaları dahil olmak üzere WSDL hizmetleriyle arayüz oluşturmak için birkaç farklı teknoloji kullanılabilir.

## WSDL Örneği

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

Bu örnekte, portType "glossaryTerms", "setTerm" adlı tek yönlü bir işlemi tanımlar.

## Referanslar

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL dosya biçimi özellikleri](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

