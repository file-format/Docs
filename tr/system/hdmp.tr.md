{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP Dosyası - Windows Yığın Dökümü Dosya Biçimi",
  "description":"HDMP dosya formatı ve HDMP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## HDMP dosyası nedir?

HDMP dosyası, bir uygulama veya program bir hata nedeniyle çöktüğünde sıkıştırılmamış bir bellek dökümüdür. Yalnızca Windows XP/Vista tarafından oluşturulur ve uygulamanın çöktüğü andaki durumunun bir dökümünü içerir. Sıkıştırılmamış olan HDMP dosyaları, raporlama amacıyla sıkıştırılan Minidump [MDMP](/tr/system/mdmp/) dosyalarına kıyasla diskte daha fazla yer kaplar.

HDMP dosyalarını **açmak** veya analiz etmek için kullanılabilecek uygulamalar, Windows için Hata Ayıklama araçlarına sahip Microsoft Visual Studio'yu içerir.

## HDMP Dosya Biçimi

HDMP dosyaları diske ikili dosyalar olarak depolanır ve uygun uygulamalar olmadan açılırsa herhangi bir fayda sağlamaz. Bunlar, hata oluştuğunda kaydedilen ilgili sistem verilerini içerir.

### HDMP ve MDMP Dosya Biçimleri arasındaki fark

HDMP sıkıştırılmamış bellek dökümü dosyalarıdır. Bunun aksine, MDMP, dosya boyutunu küçültmek için sıkıştırılan ve sorunu bildirmesi için Microsoft'a gönderilen mini döküm dosyalarıdır.

## Referans ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

