{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Age of Empires 2 Genişletme Tekrarı MGX dosya formatı ve MGX dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "MII Dosyası - Wii Sanal Avatar Dosya Formatı",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-tr",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## .MII dosyası nedir?

MII dosyası, sanal avatarları Nintendo Wii oyun konsolunda depolamak için kullanılan sanal bir avatar dosyası formatıdır. Bu dosyalar avatarın görünümü, hareketleri, animasyonları gibi bilgileri içerir. Wii'deki oyunlarda, sosyal ağ uygulamalarında ve diğer yazılımlarda kullanılabilirler. Bir MII dosyası ayrıca avatarla ilgili cinsiyet, saç rengi, ten rengi, yüz özellikleri ve göz tipi gibi diğer özellikleri de içerir.

[My Avatar Editor](https://rc24.xyz/goodies/mii/) kullanarak bir MII dosyasını açabilirsiniz.

## MII Dosya Formatı

MII dosya formatı [Wii Brew](https://wiibrew.org/wiki/Mii_data) üzerinde ayrıntılı olarak tanımlanmıştır. MII dosyasındaki dizeler, big-endian olan Unicode biçiminde (UTF-16) saklanır.

### MI Blok

MII dosya verileri Wiimote'ta iki blok halinde saklanır. Her bloğun uzunluğu 750 bayttır ve 2 baytlık CRC, toplam 752 bayttır. Her blok, MII dosya formatı için sihirli sayı gibi görünen 4 baytlık bir değerle ('RNCD') başlar.

## MII Dosyaları Nasıl Oluşturulur?

Nintendo Wii için avatar oluşturmanın birkaç farklı yolu vardır:

1. `Wii'de yerleşik Mii kanalını kullanma:` Bu kanal, yüz özellikleri, vücut şekli ve giyim dahil olmak üzere çeşitli araçları kullanarak özel avatarlar oluşturmanıza olanak tanır. Avatarınızı oluşturduktan sonra onu bir Mii dosyası olarak kaydedebilir ve Wii'deki oyunlarda ve diğer yazılımlarda kullanabilirsiniz.

1. `Nintendo 3DS'de Mii Maker uygulamasını kullanma:` Mii Maker uygulaması, Nintendo 3DS'nizdeki dokunmatik ekranı ve kamerayı kullanarak özel avatarlar oluşturmanıza olanak tanır. Avatarınızı oluşturduktan sonra onu bir Mii dosyası olarak kaydedebilir ve kablosuz bağlantı yoluyla Wii'nize aktarabilirsiniz.

1. Üçüncü taraf yazılımı kullanma:' Bazı geliştiriciler Wii için özel avatarlar oluşturmanıza olanak tanıyan yazılımlar oluşturdular. Bu yazılım genellikle bilgisayarda kullanılmak üzere tasarlanmıştır ve avatarı Wii'nize aktarmak için ek adımlar gerektirebilir.

1. `Önceden hazırlanmış avatarları kullanma:` Wii'deki bazı oyunlar ve diğer yazılımlar, kullanabileceğiniz önceden hazırlanmış avatarlarla birlikte gelebilir.

Her durumda, avatarınızı Wii'de oluşturup kaydetmek için bir Nintendo hesabınızın olması gerekir.

## Referanslar

* [Avatar Düzenleyicim](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


