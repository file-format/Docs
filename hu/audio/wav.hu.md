{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "fájl", "kiterjesztés", "formátum", "audiocsere fájlformátum", "zene" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a WAV fájlformátumról és az API-król, amelyek WAV-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WAV - hullámforma hangfájl formátum",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Mi az a WAV fájl?

A WAV, a WAVE (Waveform Audio File Format) néven ismert, a Microsoft Resource Interchange File Format (RIFF) specifikációjának egy részhalmaza a digitális audiofájlok tárolására. A formátum nem alkalmaz tömörítést a bitfolyamon, és a hangfelvételeket különböző mintavételezési és bitsebességgel tárolja. Ez volt és az egyik szabványos formátum az audio CD-k számára. A Wave fájlok mérete nagyobb az új hangfájlformátumokhoz képest, mint például az [MP3](/hu/audio/mp3/), amelyek veszteséges tömörítést alkalmaznak a fájl méretének csökkentése érdekében, miközben megőrzik ugyanazt a hangminőséget. A WAV-fájlok azonban tömöríthetők az Audio Compression Manager (ACM) kodekekkel. Számos API és alkalmazás áll rendelkezésre, amelyek konvertálhatják a WAV fájlokat más népszerű audiofájlformátumokká.

**Tudtad?**
A FileFormat.com közreműködőjévé válhat, hogy a fájlformátum-közösséget naprakészen tartsa az eredményekről. Ha bármit meg kell osztania a WAV- vagy audiofájlformátumokkal kapcsolatban, az [Audio File Format News](https://news.fileformat.com/t/audio) szakaszban közzéteheti megállapításait, hogy az emberek naprakészek maradjanak.

## WAV fájlformátum ##

A WAVE fájlformátum, amely a Microsoft RIFF specifikációjának egy részhalmaza, egy fájlfejléccel kezdődik, amelyet adatdarabok sorozata követ. A WAVE-fájl egyetlen "WAVE"-darabbal rendelkezik, amely két részdarabból áll:

* egy "fmt" darab – az adatformátumot határozza meg
* egy "adat" darab – a tényleges mintaadatokat tartalmazza

### WAV fájl fejléc ###

A WAV (RIFF) fájl fejléce 44 bájt hosszú, és a következő formátumú:


|Pozíciók|Mintaérték|Leírás
---|---|---|
|1 - 4|"RIFF"|Riff fájlként jelöli meg a fájlt. A karakterek egyenként 1 bájt hosszúak.
|5 - 8|Fájlméret (egész szám)|A teljes fájl mérete - 8 bájt, bájtban (32 bites egész szám). Ezt általában a létrehozás után kell kitölteni.
|9 -12|"WAVE"|Fájltípus fejléc. A mi céljainkra ez mindig egyenlő a "HULLÁM"-val.
|13-16|"fmt "|Formázási darabjelölő. Tartalmazza a záró nullát
|17-20|16|A fent felsorolt formátumadatok hossza
|21-22|1|Formátum típusa (1 PCM) - 2 bájtos egész szám
|23-24|2|Csatornák száma - 2 bájtos egész szám
|25-28|44100|Mintavételi sebesség – 32 bájtos egész szám. Általános értékek: 44100 (CD), 48000 (DAT). Mintavételezési sebesség = Minták száma másodpercenként, vagy Hertz.
|29-32|176400|(Mintavételi sebesség * BitsPerSample * Csatornák) / 8.
|33-34|4|(BitsPerSample * csatornák) / 8,1 - 8 bites mono2 - 8 bites sztereó/16 bites mono4 - 16 bites sztereó
|35-36|16|Bit mintánként
|37-40|"data"|"adat" darabfejléc. Az adatszakasz elejét jelöli.
|41-44|Fájl mérete (adatok)|Az adatszakasz mérete.
|A 16 bites sztereó forrás mintaértékei fent vannak megadva.

## Referenciák ##

* [WAV – a Wikipedia által](https://en.wikipedia.org/wiki/WAV)

