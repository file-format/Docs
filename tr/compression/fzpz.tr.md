{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ Dosya Formatı - Fritzing Parça Dosyası",
  "description":"FZPZ dosyasının ne olduğu ve FZPZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Bir FZPZ dosyası nedir?

Bir FZPZ dosyası, devre prototipleme ve tasarım uygulaması **Fritzing** ile oluşturulan bir elektronik devre tasarımında kullanılan bir bileşen/parçadır. Bir [FZP](/tr/cad/fzp/) dosyası ve Fritzing'in genel bölümünü açıklayan dört [SVG](/tr/image/svg/) görüntüsü içeren sıkıştırılmış bir arşivdir. Bu dosyaları kullanmanın avantajı, kullanıcıların FZPZ dosyalarını yeniden kullanılabilirlik açısından birbirleriyle paylaşabilmeleridir. FZPZ parçalarının paylaşımı, daha büyük PCB tasarımlarını hızlı bir şekilde oluşturmak için devre parçalarının entegre edilmesine yardımcı olur.

## FZPZ Dosya Biçimi - Daha Fazla Bilgi

FZPZ dosyaları sıkıştırılmış [ZIP](/tr/compression/zip/) arşivleri olarak diske kaydedilir. Uzantıyı .fzpz'den .zip'e yeniden adlandırabilir ve dosyaları arşivden çıkarmak için WinZIP gibi herhangi bir standart açma yardımcı programını kullanabilirsiniz.

### FZPZ Dosya Yapısı Bilgileri

Belirtildiği gibi, bir FZPZ dosyası, baskılı devre kartında kullanılan bir parçanın temsili için birden fazla dosya içeren bir arşiv dosyasıdır. FZPZ aşağıdaki dosyaları içerir:

* "Dört SVG dosyası" - parçanın devre tahtası, şematik, PCB ve simge görüntülerini temsil eden
* `FZP dosyası` - Parçanın özellikleri, bağlayıcıları ve veri yolları hakkında bilgi içeren bir XML dosyası

Dosyalar genellikle aşağıdaki gibi adlandırılır.

* parça.dosya.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Referanslar ##

* [fzpz uzantılı yeni parçalar](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

