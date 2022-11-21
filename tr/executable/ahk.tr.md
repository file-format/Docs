{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AHK dosya formatı ve AHK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"AHK Dosya Biçimi- AutoHotkey Komut Dosyası",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## .ahk dosyası nedir?

AHK dosyası, Microsoft Windows'ta görevlerin otomasyonu için kullanılan AutoHotkey yazılım uygulamasıyla oluşturulan bir komut dosyasıdır. Anlık eylemleri gerçekleştirmek için kullanılabilecek kısayol tuşlarını kullanan görevlerin otomasyonu için talimatlar içerir. Dosya AutoHotkey tarafından yürütülür ve tüm eylemler sırayla gerçekleştirilir. AHK dosyaları, kısayol tuşları kullanılarak tanımlanan kısayol tuşlarını kullanarak karmaşık görevleri gerçekleştirecek kadar güçlüdür. AHK dosyaları, Microsoft Notepad ve Notepad ++ gibi metin düzenleyicilerle açılabilir.

## AHK Dosya Biçimi

AHK dosyaları diske düz metin dosyaları olarak kaydedilir ve AutoHotkey tarafından yürütülebilen kod satırları içerir. AutoHotkey ücretsiz, açık kaynaklı bir betik dilidir ve kullanıcıların form doldurma, otomatik tıklama, makro çalıştırma vb. işlemleri gerçekleştirmek için basitten karmaşığa betikler oluşturmasına olanak tanır. En azından bir AHK dosyası tek bir eylem gerçekleştirip ardından çıkabilir. .

AHK'yi [Exe](/tr/executable/exe/) dosyalarına dönüştürmek için kullanılabilecek araçlar mevcuttur.

### AHK Örneği

Aşağıdaki örnek, Microsoft Not Defteri'ni çalıştırmak veya zaten çalışıyorsa öne getirmek için Win+Z tuşunu kullanır.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Bir AHK dosyasını nasıl oluştururum?

Bir AHK dosyası oluşturmak için aşağıdaki adımlar kullanılabilir. Bunlar, AutoHotkey'in makinede zaten yüklü olduğunu varsayar.

* Masaüstünüze sağ tıklayın.
* Menüde "Yeni" öğesini bulun.
* "Yeni" menüsünden "AutoHotkey Script"e tıklayın.
* Komut dosyasına yeni bir ad verin.
* Masaüstünüzde yeni oluşturulan dosyayı bulun ve sağ tıklayın.
* "Komut Dosyasını Düzenle"ye tıklayın.
* Bir pencere açılmalıdır, muhtemelen Not Defteri.
* Dosya 'yı kaydet.

## Referanslar

* [AutoHotkey](https://www.autohotkey.com/)
* [Toplu dosya - Wikipewdia tarafından](https://en.wikipedia.org/wiki/Batch_file)

