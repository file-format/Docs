{
  "date" : "2023-01-31",
  "keywords" :["çalıştırma dosyası", "çalıştırma dosyası nedir", "dosya", "çalıştırma dosyası nasıl açılır", "çalıştırma dosyası uzantısı", "uzantı"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"RUN dosya formatı ve RUN dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" :"RUN Dosya Formatı - Linux Çalıştırılabilir Dosyası",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## .RUN dosyası nedir?

.run dosya formatı, Linux ortamında yazılım veya uygulama yükleyicilerini dağıtmak için yaygın olarak kullanılır. Yazılımı yüklemek için dosyayı yürütülebilir hale getirmeniz gerekir; bu işlem aşağıdaki komut kullanılarak yapılabilir:

```bash
chmod +x file_name.run 
```

Daha sonra aşağıdaki komutu kullanarak dosyayı çalıştırabilirsiniz:

```bash
./file_name.run 
```

Yükleme işlemi, yüklemeye çalıştığınız belirli dosya ve programa bağlı olarak değişebilir.

.run dosya formatı, Linux ortamında yazılım veya uygulama yükleyicilerini dağıtmak için kullanılan bir tür kabuk komut dosyasıdır. İkili dosyalar, kitaplıklar ve yapılandırma dosyaları da dahil olmak üzere yazılımı yüklemek için gereken her şeyi içeren bağımsız bir pakettir.

.run dosyalarının da kötü amaçlı kod içerebileceğini unutmamak önemlidir; bu nedenle, dosyayı çalıştırmadan önce dosyanın kaynağını doğrulamak ve virüslere karşı taramak her zaman iyi bir fikirdir.

Ayrıca, bazı .run dosyalarının çalıştırılması ve kurulması için kök ayrıcalıkları gerekebilir; bu nedenle, dosyayı yükseltilmiş izinlerle çalıştırmak için "sudo" komutunu kullanmanız gerekebilir:

```bash
sudo ./filename.run
```

## RUN dosyası nasıl açılır?

Bir .run dosyasını açmak için onu yürütülebilir hale getirmeniz gerekir; bunu "chmod" komutuyla yapabilirsiniz:

```bash
chmod +x filename.run 
```

Dosya yürütülebilir hale getirildikten sonra şunu yazarak çalıştırabilirsiniz:

```bash
./filename.run
```

Bir .run dosyasını çalıştırmak, onu bir metin düzenleyicide açmakla aynı şey değildir. Bir .run dosyasını çalıştırmak, bir programın yüklenmesinden komut dosyasının çalıştırılmasına kadar her şey olabilecek talimatlarını yürütür. Bir .run dosyasının içeriğini görüntülemek için dosyayı nano veya vim gibi bir metin düzenleyicide açmanız gerekir:

```
nano filename.run
```
veya
```
vim filename.run
```

## Referanslar
* [Ubuntu'da .bin ve .run Dosyaları Nasıl Çalıştırılır](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


