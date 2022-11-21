---
date: 2019-12-13
keywords: flac, flac dosya formatı, .flac uzantısı, flac dosyası, flac vs mp3
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLAC dosya formatı ve FLAC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: FLAC Dosya Biçimi
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## FLAC dosyası nedir?

FLAC (Free Lossless Audio Codec), Xiph.Org Foundation tarafından geliştirilen kayıpsız bir sıkıştırma ses kodlama formatıdır. FLAC, .flac uzantısıyla kaydedilen telifsiz bir açık biçimdir. FLAC algoritması kullanılarak sıkıştırılan dijital ses, genellikle boyut olarak yüzde 50 ila 70'e düşürülür. FLAC dosyalarının sıkıştırılmış hali, orijinal ses dosyalarının aynı kopyasına açılabilir.

## FLAC dosya Biçimi

Bu, FLAC bit akışına genel bir bakıştır.

- **fLaC işaretçisi**: Bu işaret, akışın başına eklenir. Bunu bir veya daha fazla meta veri bloğu takip eder.
- **Meta veri blokları**: 128 çeşit meta veri bloğu FLAC tarafından desteklenir; şu anda aşağıdakiler tanımlanmıştır.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **ÇERÇEVE**: Ses verileri bir veya daha fazla ses çerçevesinden oluşur.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## FLAC Dosya Biçiminin Kısa Tarihi

Josh Coalson, FLAC'ı geliştirmeye 2000 yılında başladı. FLAC'ın ilk sürümü 20 Temmuz 2001'de yayınlandı. FLAC, 20 Ocak 2003'te Xiph.Org bayrağı altında birleştirildi. 1.3.0 sürümünün 26 Mart 2013'te piyasaya sürülmesi.

## FLAC Projesinin Bileşimi

FLAC projesi aşağıdakilerden oluşur:

- Akış formatları.
- Akış için basit kap formatı (FLAC).
- libFLAC: Referans kodlayıcılar, kod çözücüler ve meta veri arayüzü kitaplığı.
- libFLAC++: libFLAC için nesne yönelimli bir sarıcı.
- flac: FLAC akışlarını kodlamak ve kodunu çözmek için bir komut satırı programı.
- metaflac: FLAC için bir komut satırı meta veri düzenleyicisi.
- Winamp, XMMX, vb. gibi müzik çalarlar için giriş eklentileri.
- Ogg konteyner formatı (Ogg FLAC).

## FLAC Tasarımı

Müziğin yoğunluğuna ve genliğine bağlı olarak, sıkıştırılmış dosyanın boyutu orijinal dosyadan %80 daha küçük olabilir.

### Kaynak Kodlayıcı ###

- Yalnızca tamsayı örneklerini destekler, kayan noktayı desteklemez. Örnek başına 4 ila 32 bit PCM bit çözünürlüğünü ve 1 Hz ila 65.535 Hz örnekleme hızını işleyebilir. FLAC kodlaması örnek başına 24 bit ile sınırlıdır.
- Sıkıştırmayı artırmak için kanallar arası korelasyonlardan yararlanmak üzere kanallar gruplandırılabilir.
- CRC sağlama toplamları, bozuk çerçeveleri tanımlamak için kullanılır.
- Ses örneklerinin dönüştürülmesi için FLAC doğrusal tahmin kullanır.

### Meta veri ###

- FLAC, ReplayGain'i destekler (sesteki yüksekliği algılamak ve normalleştirmek için kullanılır).
- FLAC, etiketleme için Vorbis yorumlarında kullanılan sistemin aynısını kullanır.
- libFLAC, çoğu FLAC uygulaması tarafından kodlama/kod çözme için kullanılır.
- libFLAC API, temel FLAC bit akışından soyutlamayı artırmak için akışlar, aranabilir akışlar ve dosyalar halinde düzenlenmiştir.

### Sıkıştırma ###

libFLAC, 0'dan 8'e kadar sıkıştırma düzeylerini kullanır; burada 0 en hızlı ve 8 en yavaş sıkıştırma düzeyidir. Sıkıştırılmış dosyalar, hız ve boyut arasında değiş tokuş olmasına rağmen her zaman kayıpsızdır.

## FLAC'a karşı MP3
MP3 kayıplı bir sıkıştırma formatıdır, yani sıkıştırmayı uyguladıktan sonra boyutunu küçültmek için sesin bir kısmını kesebilir. Oysa FLAC kayıpsız bir dosya formatıdır, bu da sesi en saf haliyle duyabileceğiniz anlamına gelir. Daha önce kayıpsız dosya formatları, FLAC kadar fazla alan verimli olmayan CDA veya WAV idi. Aşağıdaki tablo, bazı önemli terimler için bu iki biçim arasındaki karşılaştırmayı gösterecektir:

|Terim|FLAC|MP3|
---|---|---|
|**Veri Kalitesi**|Ses verisi kaybı yok| Ses verileri sıkıştırılırken bazı veriler kaybolabilir |
|**Boyut**|Kayıplı biçimlere kıyasla daha büyük dosya boyutu. Bu nedenle daha büyük depolama kapasitesine ihtiyacınız var | Daha küçük dosya boyutu, küçük depolama alanı olan kompakt ses cihazlarında çalmaya uygundur |
|**Donanım gereksinimleri**| Yüksek kaliteli ses donanımına ve büyük depolama kapasitesine ihtiyacınız var |Büyük ses kitaplıkları daha küçük bir depolama alanına kaydedilebilir. Müzik çalarlar veya cep telefonları gibi elde taşınan cihazlar için uygundur|
|**İnternet üzerinden dağıtım**|Büyük dosya boyutu nedeniyle internet üzerinden kolayca dağıtılamaz |Kompakt dosya boyutu, internet üzerinden dağıtımı kolaylaştırır|
|**Uyumluluk**|Gezegendeki her cihazla hemen hemen uyumlu olan en popüler müzik ve ses dinleme codec'i Yeni nesil PC'ler, telefonlar, AV alıcıları, blu-ray oynatıcılar, Roku veya Fire TV gibi akış cihazları ile uyumlu|

## Referanslar ##

- [FLAC - Vikipedi](https://en.wikipedia.org/wiki/FLAC)

