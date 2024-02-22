{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "MCR dosya formatı ve MCR dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title": "MCR - Minecraft Bölge Dosya Formatı",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-trr"
}
},
  "lastmod": "2022-12-14"
}

## .MCR dosyası nedir?

Minecraft MCR dosya formatı, Minecraft tarafından bir Minecraft Dünyasının arazi parçalarını depolamak için kullanılan bir veri formatıdır. Popüler açık kaynaklı oyun motoru Minecraft Forge'un geliştiricileri tarafından geliştirilen NBT (Adlandırılmış İkili Etiket) formatını temel alır. MCR dosya türü en başta tanıtıldı ve daha sonra [MCA file format](/game/mca/) ile değiştirildi.

## MCR Dosya Formatı

MCR dosya formatı, her biri belirli bir veri türünü içeren bir dizi adlandırılmış ikili etiket olarak yapılandırılmıştır. Üst düzey etiket, tek bir oyun seviyesine ait tüm verileri içeren Seviye etiketidir. Level etiketinin içinde, oyun dünyası hakkında bilgi depolayan Veri etiketi ve dünyayla ilgili verileri depolayan Varlıklar ve TileEntities etiketleri gibi farklı türde verileri depolayan başka adlandırılmış etiketler vardır. sırasıyla dünyadaki oyun nesneleri ve karo varlıkları.

## MCR Dosya Formatının içinde ne var?

Minecraft MCR dosya formatında bölge, oyun dünyasının 32x32 blokluk alanıdır. MCR formatı, verileri daha verimli yönetmek ve oyun seviyelerinin daha hızlı yüklenmesine ve kaydedilmesine olanak sağlamak için oyun dünyasını bölgelere ayırır. Her bölge ayrı bir dosyada saklanır ve MCR dosya formatı, her bölgenin oyun dünyasındaki konumunu tanımlamak için bir koordinat sistemi kullanır. Bir bölgenin koordinatları, bölgenin sol alt köşesindeki blok koordinatları ile belirlenir. Örneğin, koordinatları (-1,0) olan bir bölge, oyun dünyasının başlangıç noktasından bir bölge sola ve sıfır bölge aşağıya yerleştirilecektir.

## MCR Dosya Formatı Özellikleri

MCR dosya formatı spesifikasyonları kamuya açıktır. MCR formatının dayandığı NBT formatının spesifikasyonları Minecraft Forge web sitesinde mevcuttur. Ek olarak [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format), MCR dosya formatı hakkında, yapısı ve desteklediği çeşitli veri türleri de dahil olmak üzere ayrıntılı bilgilere de sahiptir.

### MCR Dosyalarındaki Sıkıştırılmış Veriler

Minecraft MCR dosya formatı sıkıştırmayı destekler. MCR dosya formatı, verilerin sıkıştırılmış biçimde saklanmasına izin veren [NBT format](https://minecraft.fandom.com/wiki/NBT_format) temeline dayanır. Bu, MCR dosyalarının boyutunun azaltılmasına ve bunların aktarılmasının ve saklanmasının daha verimli olmasına yardımcı olur. Bu, MCR dosya formatının önemli bir özelliğidir çünkü oyuncuların büyük Minecraft World arazi verilerini başkalarıyla paylaşmasına olanak tanır.

## Referanslar

* [Minecraft Dünya Düzenleyicisi](https://www.mcedit.net/)

* [Minecraft Hakkında](https://www.minecraft.net/)

* [Bölge Dosya Formatı](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT Formatı](https://minecraft.fandom.com/wiki/NBT_format)


