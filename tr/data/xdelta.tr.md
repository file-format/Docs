{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA Dosyası - xdelta Diferansiyel Dosyası - .xdelta dosyası nedir ve nasıl açılır?",
  "description" : "xdelta Diferansiyel Dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-tr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .XDELTA dosyası nedir?

XDELTA dosya formatı, diğer iki dosya arasındaki ikili farklılıkları tutar ve iki dosya arasındaki farkların hesaplanmasını ve bu farklılıkların kompakt bir formatta kodlanmasını içeren, delta kodlamaya yönelik bir komut satırı yardımcı programı olan xdelta aracı tarafından oluşturulur. XDELTA dosyaları, orijinal dosya ile güncellenen dosya arasındaki değişiklikleri veya farklılıkları temsil eden ikili verileri depolar. Bir XDELTA dosyasındaki ikili veriler, bir dosyayı (orijinal) başka bir dosyaya (güncellenmiş veya yamalı sürüm) dönüştürmek için gereken değişiklikleri temsil eder.

XDELTA dosyaları, oyun topluluğunda video oyunlarına yönelik değişiklikleri (modları) dağıtmak için sıklıkla kullanılır. Bu modlar, kozmetik değişikliklerden oyun mekaniğindeki önemli değişikliklere kadar her şeyi içerebilir. XDELTA dosyaları, kullanıcıların orijinal oyun dosyalarını XDELTA dosyasında belirtilen değişikliklerle yamalayarak bu değişiklikleri oyun kurulumlarına uygulamalarına olanak tanır.

## xdelta

xdelta', delta kodlama ve kod çözme için kullanılan bir komut satırı yardımcı programıdır; öncelikle iki dosya arasında genellikle delta yamaları veya xdelta yamaları olarak adlandırılan ikili yamalar oluşturmak ve uygulamak için kullanılır; Bu yamalar, orijinal dosya ile değiştirilmiş veya güncellenmiş sürüm arasındaki farkları temsil eder ve özellikle bant genişliği veya depolama alanının sınırlı olduğu senaryolarda güncellemelerin verimli dağıtımına olanak tanır.

İşte 'xdelta'nın ana işlevlerine kısa bir genel bakış:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

xdelta', yazılım güncellemelerini dağıtmak, video oyunlarına yama uygulamak ve gömülü cihazlar veya ağ cihazlarındaki sistem dosyalarını güncellemek gibi çeşitli senaryolarda yaygın olarak kullanılır. Bant genişliği kullanımını ve depolama gereksinimlerini en aza indirirken dosya güncellemelerini yönetmek için esnek ve etkili bir yol sağlar.

## xdeltaui

xdeltaui, XDELTA yamalarını yönetmeye ve uygulamaya yönelik bir grafik kullanıcı arayüzü (GUI) uygulamasıdır. xdelta gui, kullanıcıların XDELTA dosyalarıyla etkileşim kurması ve bunları karşılık gelen orijinal dosyalara uygulaması, etkili bir şekilde yama uygulaması veya güncellemesi için kullanıcı dostu bir arayüz sağlar.

Metin tabanlı komutlarla çalışan xdelta'nın komut satırı sürümünün aksine, xdeltaui, özellikle komut satırı arayüzlerine aşina olmayan veya grafiksel araçları tercih eden kullanıcılar için XDELTA dosyalarını işlemek için daha sezgisel bir yol sunar.

Xdeltaui ile kullanıcılar genellikle orijinal dosyayı seçme, XDELTA yama dosyasını seçme ve güncellenmiş dosyayı oluşturmak için yama uygulama gibi görevleri gerçekleştirebilir. Bu, özellikle video oyunlarına veya diğer yazılım uygulamalarına yönelik modların veya güncellemelerin yüklenmesinde yararlı olabilir.

## xdelta İndir

Linux sistemlerinde 'xdelta'yı yüklemek için 'apt', 'yum' veya 'dnf' gibi paket yöneticilerini kullanabilirsiniz. Örneğin Ubuntu'da aşağıdaki komutu kullanabilirsiniz:

```
sudo apt-get install xdelta3
```

## xdelta nasıl kullanılır

xdelta'yı kullanmak için genellikle şu genel adımları uygulamanız gerekir:

1.  **İndirin ve Kurun**: Öncelikle sisteminizde 'xdelta'nın kurulu olduğundan emin olun. Resmi web sitesinden, paket yöneticilerinden veya diğer güvenilir kaynaklardan indirebilirsiniz.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Yama Oluşturma**:
    
- Komut satırı arayüzünüzü açın (terminal veya komut istemi).
- Bir yama oluşturmak için 'xdelta' komutunu uygun seçeneklerle birlikte kullanın. Temel sözdizimi şöyledir:
               
''
xdelta deltası<original_file><updated_file><patch_output_file>
''
        
 Değiştir<original_file> `orijinal dosyanın yolu ile birlikte,`<updated_file> ` güncellenen dosyanın yolunu içeren ve `<patch_output_file> ` yama dosyası için istenen adla.
- Örnek:
               
''
xdelta delta orijinal_dosyası güncellenmiş_dosya yaması.xdelta
''
        
4.  **Yama Uygulama**:
    
- Orijinal dosyanın ve yama dosyasının mevcut olduğundan emin olun.
- Komut satırı arayüzünüzü açın.
- Yamayı uygulamak için uygun seçeneklerle birlikte 'xdelta' komutunu kullanın. Temel sözdizimi şöyledir:
        
      
''
xdelta yaması<original_file><patch_file><output_file>
''
        
 Değiştir<original_file> `orijinal dosyanın yolu ile birlikte,`<patch_file> ` yama dosyasının yolu ile birlikte ve `<output_file> ` çıktı dosyası için istenen adla.
- Örnek:
                
''
xdelta yaması orijinal_dosya yaması.xdelta güncellenmiş_dosya
''
        
5.  **Yardımı Görüntüleme**: Belirli seçenekler veya komutlarla ilgili yardıma ihtiyacınız varsa, kullanım bilgilerini ve mevcut seçenekleri görüntülemek için xdelta komutunu --help seçeneğiyle birlikte kullanabilirsiniz.
    
## XDELTA dosyası nasıl açılır

XDELTA dosyaları doğrudan açılmaya yönelik değildir. Bir oyuna veya başka bir dosyaya XDELTA yaması uygulamak istiyorsanız, birden fazla platformla uyumlu olan xdelta'yı veya Windows kullanıcıları için özel olarak tasarlanmış xdelta kullanıcı arayüzünü kullanma seçeneğiniz vardır.

## Referanslar
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


