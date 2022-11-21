{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FZP dosya formatı ve FZP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"FZP Dosya Formatı - Fritzing XML Parça Açıklama Dosyası",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## .fzp dosyası nedir?

Bir FZP dosyası, [Fritzing](https://fritzing.org/) elektronik devre prototipleme ve tasarım uygulaması tarafından oluşturulan bir XML dosyasıdır. [XML](/tr/web/xml/) dosya biçiminde parçanın özellikleri, bağlayıcıları ve veriyolları hakkında bilgi içerir. FPZ dosyaları, Fritzing'de bağımsız olarak kullanılamaz. Bunun yerine, FZPZ arşiv dosyasının bir parçası olarak içe aktarılırlar.

## FZP Dosya Biçimi - Daha Fazla Bilgi

FZP dosyaları, parçanın özellikleri, bağlayıcıları ve veri yolları hakkında bilgi içeren XML dosyalarıdır. Bunlara ek olarak FZP dosyaları ayrıca FZP dosyasının başlığı, açıklaması, yazarı ve yayınlanma tarihi hakkında bilgiler içerir. Bir Fritzing parça dosyası dışa aktarıldığında, Fritzing uygulaması bir FZP dosyası ve dört [SVG](/tr/image/svg/) dosyası içeren bir [FZPZ](/tr/compression/fzpz/) sıkıştırılmış arşiv oluşturur.

[FZP dosya biçimi belirtimleri](https://github.com/fritzing/fzp/blob/master/docs/README.md) Github by Fritzing'de mevcuttur.

## FZP Dosya Yapısı Örneği

Tipik bir FZP dosyası aşağıdaki XML yapısına sahiptir.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Referanslar

* [FZP Dosya Biçimi Özellikleri](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [fzpz uzantılı yeni parçalar](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

