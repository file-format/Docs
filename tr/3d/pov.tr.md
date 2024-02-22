
{
  "date": "2023-01-05",
  "keywords": [
"bakış açısı dosyası",
"pov dosya biçimi",
"pov dosyası nedir",
"dosya",
"bakış açısı örneği",
"pov dosya uzantısı",
"eklenti",
"biçim"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "POV dosya formatı ve POV dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title": "POV - Görüş Dosyasının Kalıcılığı",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-trv"
}
},
  "lastmod": "2023-01-05"
}

## .POV dosyası nedir?

POV dosyası, POV-Ray ışın izleme yazılımına ilişkin talimatları içeren düz metin dosyasıdır. Bu talimatlar POV-Ray'e özgü özel bir kodlama dilinde yazılmıştır. 3 boyutlu nesneler, malzemeler, ışıklandırma ve sahnenin görünümünü tanımlayan diğer özellikler de dahil olmak üzere, oluşturulacak sahneyi belirtir. POV dosyaları, POV-Ray'e özel özel bir kodlama dili kullanır ve karmaşık ve ayrıntılı 3D sahneler oluşturmak için kullanılabilir. POV dosyasının dosya uzantısı genellikle .pov veya .povraydir. POV-Ray'de bir POV dosyasını açtığınızda, yazılım dosyadaki talimatları okur ve bunları sahnenin işlenmiş bir görüntüsünü oluşturmak için kullanır.

.pov dosyaları genellikle sanatçılar ve tasarımcılar tarafından film, televizyon, video oyunları ve pazarlama materyalleri dahil olmak üzere çeşitli uygulamalara yönelik 3D grafikler ve animasyonlar oluşturmak için kullanılır.

## POV Dosya Formatı

**.pov dosyası** genellikle önceden tanımlanmış renk, doku ve sahnede kullanılabilecek diğer kaynaklardan oluşan kitaplıkları dahil etmek için kullanılan bir dizi **#include** ifadesiyle başlar. Daha sonra dosya, bir dizi blok kullanarak sahnenin nesnelerini, malzemelerini ve diğer özelliklerini tanımlar. Bir .pov dosyasında belirtebileceğiniz birçok başka türde nesne, malzeme ve başka özellik vardır ve daha karmaşık ve ayrıntılı sahneler oluşturmak için döngüleri ve koşullu ifadeleri kullanabilirsiniz.

## POV için Yazılım Uygulamaları

.pov dosya formatı POV-Ray ışın izleme yazılımı tarafından kullanılır, dolayısıyla .pov dosyalarını açmaya yönelik birincil uygulama POV-Ray yazılımının kendisidir. POV-Ray'in en son sürümünü https://www.povray.org/ adresindeki resmi web sitesinden indirebilirsiniz.

POV-Ray'e ek olarak, .pov dosyalarını açabilen ve düzenleyebilen bir dizi başka uygulama da vardır:

- BRL-CAD: .pov dosyalarını içe ve dışa aktarabilen açık kaynaklı bir 3D modelleme yazılımı
- MeshLab: .pov dosyalarını içe ve dışa aktarabilen bir 3D ağ işleme yazılımı
- Blender: .pov dosyalarını içe ve dışa aktarabilen popüler bir açık kaynaklı 3D grafik yazılımı

.pov dosyalarını açabilen başka yazılım uygulamaları da olabilir; bu nedenle, bir .pov dosyasını yukarıdaki uygulamalarla açamıyorsanız bir dosya görüntüleme veya dönüştürme aracı kullanmayı deneyebilirsiniz.

## Bakış Açısı Örneği

Örneğin, burada tek mavi silindirli bir sahneyi tanımlayan örnek bir .pov dosyası verilmiştir:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Bu örnekte, kamera bloğu kameranın sahnedeki konumunu ve yönünü belirtir, 'light_source' bloğu bir ışık kaynağı bildirir ve konumunu ve rengini belirtir ve 'silindir' bloğu bir silindir nesnesini bildirir ve uç noktalarını belirtir, yarıçap ve malzeme özellikleri. Bu .pov dosyasını POV-Ray yazılımında açtığınızda, tek bir mavi silindirin görüntüsü oluşturulacaktır.

## Referanslar
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Belgeler POV-Ray Web Sitesi](http://www.povray.org/documentation/)

