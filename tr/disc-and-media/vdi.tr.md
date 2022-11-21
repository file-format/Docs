{
  "date" : "2021-08-11",
  "keywords" :[ "vdi dosyası", "vdi dosya biçimi", "vdi dosyası nedir", "dosya", "vdi örneği", "vdi dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VDI dosya formatı ve VDI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"VDI - VirtualBox Sanal Disk İmaj Dosyası",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## .vdi dosyası nedir?
.vdi uzantılı bir dosya bir sanal disk görüntüsüdür; Oracle'ın VirtualBox adlı açık kaynaklı masaüstü sanallaştırma programına özgü. VDI dosyaları, VirtualBox sanal makinesini başlatmak için kullanılır. VM'ler, kullanıcıların tek bir bilgisayarda ek işletim sistemleri veya programlar çalıştırmasına izin verir. Bu nedenle, VDI dosyalarının yararı, kullanıcıların bu disk görüntü dosyalarını sabit disklerine kaydedebilmeleri ve ihtiyaç duyduklarında öykünücüler kullanarak çalıştırabilmeleridir.

## VDI dosya formatı
Virtual Disk Image (VDI), kurumsal sınıf bir sanallaştırma ürünü olan VirtualBox olarak bilinen, aktif olarak geliştirilmiş, açık kaynaklı bir Oracle VM için birincil disk dosyası biçimidir. VDI dosya biçimi, diğer sanallaştırma programları kullanılarak kolayca çalıştırılabilen taşınabilir bir disk görüntüsü oluşturmak için tasarlanmıştır. Hem dinamik olarak ayrılmış hem de sabit boyutlu depolamayı destekler. Halihazırda veri içeriyor olsa bile bir görüntü dosyasını oluşturulduktan sonra genişletmenize olanak tanır.

### Disk sanallaştırma
Sistem, sabit diskleri VDI disk görüntüsü biçiminde taklit eder. Bir VirtualBox VM, Microsoft Virtual PC veya VMware'de oluşturulmuş eski disklerin yanı sıra kendi yerel biçimini kullanabilir. VirtualBox ayrıca sanal sabit diskler olarak kullanarak iSCSI hedeflerine bağlanma ve ana bilgisayarda ham bölümleme yeteneğine sahiptir. VirtualBox, IDE (PIIX4 ve ICH6 denetleyicileri), SATA (ICH8M denetleyicisi), sabit sürücülerin takılabileceği SAS denetleyicileri ve SCSI öykünür.

Destek, VirtualBox'ın 2.2.0 sürümünden itibaren Açık Sanallaştırma Formatı (OVF) için mevcuttur. Hem ana bilgisayara bağlı fiziksel aygıtlar hem de ISO görüntüleri, CD veya DVD sürücüleri olarak monte edilebilir.
VirtualBox varsayılan olarak VESA uyumlu özel bir sanal grafik kartı aracılığıyla grafikleri destekler.

### Ethernet için sanallaştırma desteği
VirtualBox, bir Ethernet ağ bağdaştırıcısı için aşağıdaki Ağ Arabirim Kartlarını sanallaştırır:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Masaüstü (82540EM)
- Intel Pro/1000 MT Sunucusu (82545EM)
- Intel Pro/1000 T Sunucusu (82543GC)
- Paravirtualized ağ bağdaştırıcısı (virtio-net)

Öykünülmüş ağ kartları, konuk işletim sisteminin bir parçası olarak mevcut olduğundan, ağ donanımı için sürücü aramaya ve yüklemeye gerek kalmadan konuk işletim sistemlerinin çalışmasını sağlar. Özel bir yarı sanallaştırılmış ağ bağdaştırıcısı, belirli bir donanım arabirimiyle eşleşme gereksinimini azaltarak ağ performansını artırır. Bu nedenle misafirlikte özel sürücü desteği gerektirir.


## Referanslar

* [VirtualBox - Wikipedia'dan](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


