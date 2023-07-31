{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ Dosya Biçimi - Sıkıştırılmış SYS Dosyası",
  "description":"SY_ dosya formatı ve SY_ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## SY_ dosyası nedir?

SY_ dosyası, yazılım yükleyicileri tarafından yükleyici içinde paketlenen yükleme dosyalarının boyutunu azaltmak için kullanılan sıkıştırılmış bir .sys dosyasıdır. Bu, yükleyicinin genel boyutunu azaltır. SY_ dosyaları, bir veya daha fazla sıkıştırılmış dosyayı genişleten Microsoft Expand komut satırı yardımcı programı kullanılarak genişletilebilir.

## SY_ Dosya Biçimi - Daha Fazla Bilgi

SY_ dosyaları diske sıkıştırılmış ikili dosyalar olarak kaydedilir. Ancak, dahili dosya biçimleri herkese açık değildir. Microsoft Expand komut satırı yardımcı programı, aşağıdaki komut satırlarından birini kullanarak SY_ dosyalarını genişletebilir.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Genişletildiğinde, SY_ dosyaları [SYS](https://docs.fileformat.com/system/sys/) dosyasına dönüştürülür.

SY_ dosyaları, EX_ ve DL_ dosyalarına benzer.

## Referanslar

* [StuffIt - Wikipedia Tarafından](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Genişlet](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

