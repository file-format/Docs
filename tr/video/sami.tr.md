{
"tarih": "2023-05-16",
  "keywords": [
"sami dosyası",
"sami dosyası nedir",
"sami dosyası örneği",
"dosya",
"sami dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SAMI Dosya Formatı - Altyazılar ve Meta Veri Değişim Dosyası",
  "description":"SAMI dosyalarını oluşturabilen ve açabilen SAMI formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"sonmod": "2023-05-16"
}

## .SAMI dosyası nedir?

".sami" uzantılı bir dosya genellikle bir Altyazı ve Meta Veri Değişimi (SAMI) dosyasına atıfta bulunur. SAMI, videolarda altyazıları veya altyazıları görüntülemek için kullanılan bir altyazı biçimidir. Başlangıçta Microsoft tarafından Windows Media Player için geliştirildi.

SAMI dosyaları, altyazılar veya altyazılar için zamanlama bilgileri ve metin içeriği içerir ve bunların bir video oynatımıyla senkronize edilmesine olanak tanır. Format, yazı tipi stili, renk ve alt yazıların ekrandaki konumu gibi temel formatlama seçeneklerini destekler.

SAMI dosyaları genellikle düz metin dosyalarıdır ve bir metin düzenleyici kullanılarak açılabilir ve düzenlenebilir. Bir SAMI dosyasının içeriği tipik olarak dosya hakkında bilgi sağlayan bir başlık bölümünü ve ardından ilgili zamanlama ve metni içeren ayrı altyazı girişlerini içerir.

İşte bir SAMI dosyasının nasıl görünebileceğine dair bir örnek:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI dosyaları genellikle Windows Media Player veya VLC Media Player gibi altyazı görüntülemeyi destekleyen video oynatıcılar veya medya oynatıcılarla birlikte kullanılır. Oynatıcı, SAMI dosyasını okur ve altyazıları video içeriğiyle senkronize ederek izleyicilerin videoyu izlerken altyazıları okumasına olanak tanır.

## Desteklenen HTML etiketleri

SAMI (Altyazılar ve Meta Veri Değişimi) dosyaları, altyazıları biçimlendirmek ve şekillendirmek için sınırlı sayıda HTML benzeri etiketi destekler. SAMI tarafından desteklenen yaygın olarak kullanılan etiketlerden bazıları şunlardır:

- ''<SAMI> :`` SAMI dosyasının tamamını kapsayan kök öğe.
- ''<HEAD> :`` SAMI dosyası için başlık bilgilerini içerir.
<html>- ''<TITLE> :`` SAMI dosyasının başlığını belirtir. </html>
- ''<BODY> :`` Altyazı girişlerini ve zamanlama bilgilerini içerir.
- ''<SYNC> :`` Bir altyazı girişi için senkronizasyon noktasını temsil eder. Altyazının görüntülenmesi gereken zamanlamayı belirtir.
- ''<P> :`` Bir altyazının gerçek metin içeriğini kapsar. Genellikle bir içinde kullanılır<SYNC> engellemek.
<html>- `` <FONT>:`` Ekteki metin için yazı tipi özelliklerini tanımlar. Yazı tipi görünümünü değiştirmek için Renk, Yüz, Boyut ve Stil gibi özellikler kullanılabilir.</font>
- ''<BR> :`` Altyazıya satır sonu ekler.
<html>- `` <B>:`` Ekteki metni kalın harflerle gösterir.</b>
<html>- `` <I>:`` Ekteki metni italik olarak gösterir.</i>
<html>- `` <U>:`` Ekteki metni altı çizili hale getirir.</u>
- ''<C> :`` Altyazı metninin ekrandaki konumunu veya hizalamasını belirtir. Merkez, Orta, Sol, Sağ, Üst, Alt gibi nitelikleri ve bunların kombinasyonlarını destekler.
- ''<LANG> :`` Altyazı metninin dil kodunu belirtir. Altyazıların dilinin belirlenmesine yardımcı olur.

Bunlar SAMI dosyalarının desteklediği temel etiketlerden bazılarıdır. SAMI'nin tüm HTML etiketlerini ve niteliklerini desteklemediğini unutmamak önemlidir. Desteklenen etiketler, kapsamlı belge yapılandırması veya etkileşim sağlamak yerine öncelikle altyazıların şekillendirilmesine ve konumlandırılmasına odaklanır.

## Referanslar
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

