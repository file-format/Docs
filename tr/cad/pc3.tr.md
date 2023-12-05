{
"tarih": "2023-05-09",
  "keywords": [
"pc3 dosyası",
"pc3 dosyası nedir",
"AutoCAD'de pc3 dosyası nasıl oluşturulur",
"pc3 dosyasının formatı nedir",
"pc3 dosyası ne içeriyor",
"dosya",
"pc3 dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "PC3 Dosya Formatı - AutoCAD Plotter Yapılandırma Dosyası",
  "description":"PC3 dosyalarını oluşturabilen ve açabilen PC3 formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3",
      "parent": "cad"
}
},
"sonmod": "2023-05-09"
}

## PC3 dosyası nedir?

AutoCAD'deki bir PC3 dosyası, yazılımda kullanılmak üzere yazıcı veya çizici ayarlarını içeren bir Çizici Yapılandırma dosyasıdır.

Yeni çizici konfigürasyonu oluşturduğunuzda, AutoCAD yazıcı veya çizici hakkında gerekli tüm bilgileri PC3 dosyasında saklar. Buna kağıt boyutları, kenar boşlukları, çözünürlük ve kullandığınız yazıcı veya çiziciye özel diğer ayarlar dahildir.

AutoCAD'de bir yazıcıyı veya çiziciyi kolayca kurmak ve yapılandırmak için PC3 dosyasını kullanabilirsiniz. PC3 dosyasını kullanmak için, bunu Grafik iletişim kutusundaki mevcut çizici yapılandırmaları listesinden seçmeniz yeterlidir.

Ayrıca mevcut PC3 dosyasının ayarlarını değiştirerek veya AutoCAD'deki Plotter Manager'ı kullanarak sıfırdan yeni PC3 dosyası oluşturarak özel PC3 dosyaları oluşturabilirsiniz.

## AutoCAD'de PC3 dosyası nasıl oluşturulur?

AutoCAD'de çizici yapılandırma dosyası (PC3) oluşturmak için şu adımları izleyin:

1. **Plotter Manager'ı açın:** Komut satırına "PLOTTERMANAGER" yazın veya şeritteki "Output" sekmesine gidin ve "Plotter Manager" panelinden "Plotter Manager"ı seçin.
2. **"Çizici Ekleme Sihirbazı"na tıklayın:** Bu, yeni çizici yapılandırma dosyası oluşturma sürecinde size yol gösterecek bir sihirbazı başlatacaktır.
3. **Plotter üreticisini ve modelini seçin:** Sihirbaz, listeden yazıcınızın veya çizicinizin üreticisini ve modelini seçmenizi isteyecektir. Yazıcınız veya çiziciniz listede yoksa "Bilgisayarım"ı seçip sürücü dosyasına göz atabilirsiniz.
4. **Bir bağlantı noktası seçin:** Yazıcınızın veya çizicinizin bağlı olduğu bağlantı noktasını seçin. Emin değilseniz yazıcınız veya çizicinizle birlikte gelen belgelere bakın.
5. **Çizici yapılandırmasını belirtin:** Sihirbaz, çiziciniz için kağıt boyutu, çözünürlük ve renk derinliği gibi çeşitli ayarları belirtmenizi isteyecektir. Bu seçenekleri yazıcınız veya çiziciniz için doğru şekilde ayarladığınızdan emin olun.
6. **Çizici yapılandırmasını kaydet:** Tüm ayarları belirledikten sonra sihirbaz, yeni çizici yapılandırmanıza bir ad vermenizi isteyecektir. Bu, sihirbaz tarafından belirtilen klasörde yeni PC3 dosyası oluşturacaktır.
7. **Yeni çizici yapılandırmasını kullanın:** AutoCAD'de yeni çizici yapılandırmasını kullanmak için, "Plot" iletişim kutusuna gidin, mevcut çizici yapılandırmaları listesinden yeni çizici yapılandırmanızı seçin ve ardından grafiğinizi şu şekilde ayarlayın: olağan.

Bu kadar! Artık AutoCAD'de çizimlerinizi yazdırmak veya çizmek için kullanabileceğiniz yeni bir çizici yapılandırma dosyası (PC3) oluşturdunuz.

## PC3 dosyasının formatı nedir?

PC3 dosya formatı, Autodesk'in AutoCAD yazılımı tarafından kullanılan özel bir dosya formatıdır. Kağıt boyutu, renk derinliği, çözünürlük ve diğer seçenekler de dahil olmak üzere belirli çizici veya yazıcıya yönelik yapılandırma ayarlarını içerir.

PC3 dosyası genellikle AutoCAD kurulum dizinindeki "Plotter Konfigürasyonu" klasöründe saklanır ve tutarlı yazdırma ve çizim ayarlarının sağlanması için kullanıcılar veya bilgisayarlar arasında kolayca paylaşılabilir.

PC3 dosyası esas olarak, verileri depolamak ve değiştirmek için makine tarafından okunabilen bir format olan XML verilerini içeren bir metin dosyasıdır. Metin düzenleyiciyi veya XML düzenleyiciyi kullanarak PC3 dosyasının içeriğini görüntüleyebilir ve düzenleyebilirsiniz, ancak çizici yapılandırmasında değişiklik yapmak için AutoCAD'deki Çizici Yöneticisini kullanmanız önerilir; çünkü bu, ayarların doğru şekilde biçimlendirilmesini ve yazılımla uyumlu olmasını sağlayacaktır.

## PC3 dosyası ne içeriyor?

AutoCAD'deki bir PC3 dosyası, belirli aygıta veya sürücüye özel yazıcı veya çizici yapılandırma ayarlarını içerir. Bu ayarlar AutoCAD tarafından çizimlerinizi doğru bir şekilde yazdırmak veya çizmek ve istediğiniz gibi görünmelerini sağlamak için kullanılır.

PC3 dosyasında saklanabilecek ayarlardan bazıları şunlardır:

- **Kağıt boyutu:** Bu, yazdırma veya çizim için kullanılacak kağıdın A4, Letter veya Özel gibi boyutunu belirtir.
- **Çizim alanı:** Bu, tüm düzen veya yalnızca belirli bir pencere gibi çizimin çizilecek kısmını belirtir.
- **Çizim ölçeği:** Bu, çizimin yazdırılacağı veya çizileceği ölçeği belirtir; örneğin 1:100 veya 1/4"=1'-0".
- **Çizgi kalınlığı:** Bu, çizimdeki çizgilerin kalınlığını belirtir; bu, yazdırıldığında veya çizildiğinde nasıl görüneceğini etkiler.
- **Renk derinliği:** Bu, siyah beyaz veya tam renkli gibi yazdırma veya çizim için kullanılacak renk sayısını belirtir.
- **Çözünürlük:** Bu, çizimin yazdırılacağı veya çizileceği çözünürlüğü belirtir; bu, çizimin ne kadar keskin ve ayrıntılı görüneceğini etkiler.
- **Diğer seçenekler:** PC3 dosyasında baskı kalitesi, yönlendirme, kenar boşlukları, gölgeleme ve daha fazlası gibi ayarlanabilecek birçok başka seçenek vardır.

Yazıcınız veya çiziciniz için doğru ayarları içeren PC3 dosyasını oluşturup kullanarak, çizimlerinizin doğru ve tutarlı kalitede yazdırılmasını veya çizilmesini sağlayabilirsiniz.

## Referanslar
* [AutoCAD'de PC3](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)

