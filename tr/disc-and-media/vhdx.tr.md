{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VHDX dosya formatı ve VHDX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"VHDX Dosya Formatı - VHDX dosyası nedir?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## VHDX dosyası nedir?

VHDX dosyası, Virtual Hard Disk v2 dosya biçimindeki bir disk görüntü dosyasıdır. Belirli bir işletim sistemi gerektiren yazılımın veya çalıştırılan yazılımın test edilmesi için herhangi bir normal makine gibi yüklenebilen ve kullanılabilen eksiksiz bir işletim sistemi içerir. Bir VHDX, tam bir disk görüntüsü olmasına rağmen tek bir dosyada saklanır. Parallels Desktop, Windows Virtual Machine ve Virtual Box gibi sanal makine yazılımları, disk görüntüsünü yükleyebilir ve açabilir.

VHDX dosyası, Hyper-V Manager ile [VHD](/tr/disc-and-media/vhd/) dosyasına veya VirtualBox ile [VDI](/tr/disc-and-media/vdi/) dosyasına dönüştürülebilir.

## VHDX Dosya Biçimi - Daha Fazla Bilgi

VHDX dosya biçimi ayrıntıları tamamen belgelenmiştir ve çevrimiçi olarak [VHDX Dosya Biçimi Spesifikasyonları](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) adresinde mevcuttur. ) Microsoft Dokümantasyonunda. VHD biçiminin bir uzantısıdır ve gelişmiş yetenekler içerir. VHDX dosya biçimi, sanal sabit disk ve sanal sabit disk dosya katmanlarında bulunan ek özellikler sağlar. Daha optimize edilmiştir ve depolama donanımı yapılandırması ve yetenekleri için daha iyi sonuçlar verir. VHDX dosyaları açılabilir

### VHDX'te Sanal Sabit Disk Desteği

Üç tür sanal sabit diski destekler.

1. **Sabit Sanal Sabit Disk** - Ayrılmış sabit veri boyutuna sahip sanal sabit disk. Sanal sabit diskin boyutu, verilerin eklenmesi veya çıkarılmasıyla değişmez.

1. **Dinamik Sanal Sabit Disk** - Dinamik disk boyutuna sahip sanal sabit disk. Boyutu her zaman kendisine yazılan gerçek veriler ve meta veriler kadar büyüktür. Dosya boyutu, veriler eklendikçe veya verilerden kaldırıldıkça dinamik olarak artar.

1. **Differencing Virtual Hard Disk** (Differencing Virtual Hard Disk**) - Bir üst sanal sabit disk dosyasına kıyasla, bir dizi değiştirilmiş blok olarak sanal sabit diskin akımını temsil eder.

## Referanslar

* [VHDX Dosya Biçimi Özellikleri](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - Wikipedia'dan](https://en.wikipedia.org/wiki/VHD_(file_format))

