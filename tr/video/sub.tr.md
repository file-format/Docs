{
"tarih": "2023-06-21",
  "keywords": [
"alt dosya",
"alt dosya nedir",
"MicroDVD altyazı dosyası örneği",
"Altyazı Uzantıları",
"Aboneliği Aç",
"Altyazı Dosya Türleri",
"SUB dosyası nasıl açılır",
"dosya",
"SUB dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SUB Dosya Formatı - MicroDVD Altyazı Dosyası",
  "description":"SUB formatı ve SUB dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"bağlantı başlığı": "ALT",
  "menu": {
    "docs": {
      "identifier": "video-sub",
      "parent": "video"
}
},
"sonmod": "2023-06-21"
}

## .SUB dosyası nedir?

SUB dosyası, videolarda altyazıları görüntülemek için kullanılan bir MicroDVD altyazı dosyası formatıdır ve genellikle .sub dosya uzantısına sahiptir. Bu dosyalar, her altyazı girişi için zamanlama bilgilerini ve metni içerir.

MicroDVD altyazı dosyaları, her altyazı girişinin birkaç satırdan oluştuğu basit metin tabanlı formatı kullanır. İlk satır, başlangıç ve bitiş zaman damgaları da dahil olmak üzere altyazının zamanlama bilgilerini içerir. Sonraki satırlar gerçek altyazı metnini içerir.

İşte bir MicroDVD altyazı dosyası örneği:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Altyazı Uzantıları

Altyazılar, bulundukları formata bağlı olarak çeşitli dosya uzantılarına sahip olabilir. Bazı yaygın altyazı dosya uzantıları şunları içerir:

- **.srt:** SubRip altyazı formatı. En yaygın kullanılan altyazı formatlarından biridir ve birçok medya oynatıcı ve video düzenleme yazılımı tarafından desteklenir.
- **.sub:** MicroDVD, SubViewer ve SubStation Alpha gibi farklı altyazı formatları tarafından kullanılabilen altyazı dosyası formatı.
- **.ass veya .ssa:** Gelişmiş SubStation Alpha veya SubStation Alpha altyazı formatı. Metin biçimlendirme, konumlandırma ve efektler gibi gelişmiş özellikleri destekler.
- **.vtt:** Web videolarında altyazıları görüntülemek için kullanılan WebVTT (Web Video Metin Parçaları) formatı. Genellikle HTML5 video oynatıcılarla kullanılır.
- **.idx/.sub:** DVD altyazıları tarafından kullanılan format. .idx dosyası zamanlama ve biçimlendirme bilgilerini içerirken, .sub dosyası gerçek altyazı metnini içerir.
- **.smi veya .sami:** Senkronize Erişilebilir Medya Değişim formatı. Genellikle Windows Media Player'da alt yazılar ve alt yazılar için kullanılır.

## Open Sub ne anlama geliyor?

Open Sub genellikle filmler ve TV şovları için birden fazla dilde altyazı sağlayan popüler bir çevrimiçi platform olan Publish anlamına gelir. Kullanıcı topluluğunun katkıda bulunduğu geniş bir altyazı dosyası koleksiyonu sunar. İstediğiniz film veya diziye ilişkin altyazıları aramak ve indirmek için LINK web sitesini (www.opensubtitles.org) ziyaret edebilirsiniz.

## Altyazı Dosya Türleri

Altyazı dosyaları, her biri kendi dosya türüne veya uzantısına sahip olan çeşitli formatlarda gelir. Aşağıda bazı yaygın altyazı dosya türleri verilmiştir:

- **SubRip Altyazı Formatı (.srt):** Bu, en yaygın kullanılan altyazı formatlarından biridir. SRT dosyaları, zaman damgaları ve karşılık gelen metinlerle birlikte altyazı girişlerini içeren düz metin dosyalarıdır.
- **SubViewer Altyazı Formatı (.sub):** SubViewer dosyaları SRT dosyalarına benzer, zaman damgaları ve metin içeren altyazı girişleri içerir, metin biçimlendirmesi ve renkler gibi ek özellikleri destekleyebilir.
- **SubStation Alpha (.ssa) ve Advanced SubStation Alpha (.ass):** Bu formatlar, metin formatlama, stil, konumlandırma ve animasyon efektleri gibi gelişmiş özellikleri destekler. SSA ve ASS dosyaları genellikle anime altyazıları için kullanılır.
- **MicroDVD Altyazı Formatı (.sub):** MikroDVD formatı .sub dosyalarını kullanır ve her altyazı girişi için zamanlama bilgisi ve metni içerir. Genellikle medya oynatıcılar ve video düzenleme yazılımlarıyla birlikte kullanılır.
- **DVD Altyazıları (.sub ve .idx):** DVD altyazıları genellikle iki dosyadan oluşur: altyazı metnini içeren .sub dosyası ve zamanlama ve biçimlendirme bilgilerini içeren .idx dosyası.
- **WebVTT (.vtt):** WebVTT, web videoları için kullanılan bir altyazı biçimidir, genellikle HTML5 video oynatıcılarla kullanılır ve temel biçimlendirme seçeneklerini destekler.
- **MPL2 Altyazı Formatı (.mpl):** MPL2 dosyaları, Unix benzeri sistemler için bir medya oynatıcı olan MPlayer ile birlikte kullanılır ve zaman damgaları ve metin içeren altyazı girişleri içerir.
- **iTunes Timed Text (.itt):** iTunes Timed Text dosyaları, Apple'ın iTunes ve diğer Apple platformlarındaki altyazılar için kullanılır. Metin stili ve konumlandırma gibi özellikleri desteklerler.
- **Teletekst Altyazı Formatı (.srt veya .txt):** Teletekst altyazıları televizyon yayınlarında yaygın olarak kullanılır. Genellikle .srt veya .txt uzantılı düz metin dosyaları olarak kaydedilirler.

## SUB dosyası nasıl açılır?

Aşağıdaki medya oynatıcılar SUB dosyasını altyazı parçası olarak açabilir.

- VideoLAN VLC medya oynatıcı
- MP oynatıcı

SUB dosyasını VLC oynatıcısında açmak için şu adımları izleyin

- VLC oynatıcısını açın ve videonuzu oynatın
- VLC Media Player menü çubuğundan **Altyazılar > Altyazı Dosyası Ekle....** öğesini seçin.
- SUB dosyasına gidin ve açın

SUB dosyasını düzenlemeniz gerekiyorsa, dosyayı Microsoft Notepad (Windows) veya Apple TextEdit (Mac) gibi herhangi bir metin düzenleyiciyle açabilirsiniz.

## Referanslar
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

