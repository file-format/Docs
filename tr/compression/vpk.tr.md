{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK Dosyası - PlayStation Vita Uygulama Paketi Dosya Biçimi",
  "description":"VPK dosya formatı ve VPK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## VPK dosyası nedir?

.vpk uzantılı bir dosya, Sony PlayStation Vita oyun konsoluna üçüncü taraf uygulamaları yüklemek için kullanılan sıkıştırılmış bir arşiv paketi dosyasıdır. Bu dosyalar yalnızca, PS Vita ve PSTV'nin özelleştirilmiş kullanıcı tarafından oluşturulan içeriği kullanmasını sağlayan, HENkaku'nun jailbreak Vita PlayStation'ına yüklenebilir. Bir VPK arşiv dosyası, [PNG](/tr/image/png/) dosyaları gibi görüntüler, [.bin](/tr/disc-and-media/bin/) gibi ayar dosyaları ve [XML](/tr/web/xml/) dosya biçimindeki tüm yapılandırmalar.

## VPK Dosya Biçimi

VPK dosyaları standart sıkıştırılmış [ZIP](/tr/compression/zip/) arşivleri olarak diske kaydedilir. Bunlar, Vita Gaming Console'a yüklenecek üçüncü taraf uygulamaları için birden çok klasör ve diğer ilişkili dosyalar içerebilir. VPK paket dosyasının içeriğini görüntülemek için, uzantısını .vpu'dan .zip'e yeniden adlandırın ve WinZip veya WinRAR gibi standart açma yardımcı programlarını kullanarak içeriği çıkarın.

Valvesoftware, [VPK dosya formatı](https://developer.valvesoftware.com/wiki/VPK_File_Format) hakkında, geliştiricinin bakış açısından referans alınabilecek ayrıntılı bilgilere sahiptir.

## VPK dosyaları nasıl kurulur?

VPK dosyaları, VPK.exe komut satırı yardımcı programından yüklenebilir. Windows işletim sisteminde, dosyalar, tüm paketlenmiş dosyaları içeren bir \*.vpk döndüren vpk.exe dosyasına bırakılabilir. Alternatif olarak, komut satırı aracı aşağıdaki gibi kullanılabilir.

### VPK Oluşturun ve Dosyaları Ekleyin

```
vpk <dirname>
```

### VPK Dosyalarını Çıkarın

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Görüntüleyici

* [VRF VPK Görüntüleyici](https://github.com/SteamDatabase/ValveResourceFormat)

## Referanslar

* [VPK Dosya Biçimi](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK Dosyaları](https://developer.valvesoftware.com/wiki/VPK)

