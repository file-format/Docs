{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE Dosyası - Gaussian Cube Dosyası - .cube dosyası nedir ve nasıl açılır?",
  "description" : "Gauss Küp Dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-tr-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## CUBE dosyası nedir?

Gaussian Cube dosyası (.cube) olarak da bilinen CUBE dosya formatı, hesaplamalı kimyada moleküler verileri, özellikle kuantum kimyası hesaplamalarından kaynaklanan elektron yoğunluğu bilgilerini depolamak için kullanılır. Bu format genellikle başlangıçtan itibaren elektronik yapı hesaplamalarını gerçekleştirmek için yaygın olarak kullanılan **Gaussian yazılım paketi** ile ilişkilendirilir.

Gaussian Cube dosyaları, kuantum kimyası hesaplamaları yoluyla elde edilen, tipik olarak elektron yoğunluğunu veya moleküllerin diğer özelliklerini temsil eden üç boyutlu verileri saklar. Dosya, meta verileri (köken, her eksen boyunca veri noktalarının sayısı ve aralık gibi) içeren başlık bölümünü ve ardından uzaydaki her ızgara noktasında ilgilenilen özelliği (örneğin elektron yoğunluğu) temsil eden sayısal değerlerin ızgarasını içerir.

Gauss Küp dosyası (.cube), belirli yapıya sahip bir düz metin dosyasıdır. Başlık, moleküler sistem ve veri ızgarası hakkında bilgi içerir ve veri değerleri, üç boyutlu ızgara formatında düzenlenir. Gaussian Cube dosyaları genellikle moleküler görselleştirme yazılımı kullanılarak moleküler özellikleri görselleştirmek için kullanılır. **VMD (Görsel Moleküler Dinamik)** veya **PyMOL** gibi programlar, moleküler yüzeyleri, elektron yoğunluğunu veya hesaplanan diğer özellikleri görüntülemek için Gaussian Cube dosyalarını okuyabilir.

## Gauss Küp dosyasının basitleştirilmiş örneği:

''''
Küp Dosyası Örneği
Gaussian tarafından oluşturuldu
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0.10000000000000000E+01 0.0000000000000000E+00 0.0000000000000000E+00
  50 0,00000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,00000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0.123456789E+02 0.123456789E+02 0.123456789E+02 0.123456789E+02 0.123456789E+02
    ... (her ızgara noktasındaki elektron yoğunluğuna ilişkin veri değerleri)
''''

## Gaussian Hakkında

Gaussian, kuantum kimyası ve hesaplamalı kimya için bir yazılım uygulamaları paketidir. Gaussian'ın ana odak noktası, moleküllerin elektronik yapısının incelenmesine yönelik son derece doğru ancak hesaplama açısından yoğun yaklaşımlar olan ab initio kuantum kimyası yöntemleridir. Yazılım, moleküler özellikleri tahmin etmek, reaksiyon mekanizmalarını incelemek ve moleküler yapıları keşfetmek dahil olmak üzere çeşitli uygulamalar için araştırma ve akademik ortamlarda yaygın olarak kullanılmaktadır.

## NWChem Hakkında

NWChem, yüksek performanslı kuantum kimyası simülasyonları için tasarlanmış açık kaynaklı bir hesaplamalı kimya yazılımıdır. Hartree-Fock ve yoğunluk fonksiyonel teorisi gibi başlangıçtan itibaren yöntemleri kullanır, kümeler üzerinde verimli hesaplamalar için paralel hesaplamayı destekler ve hesaplamalı kimya, biyokimya ve malzeme bilimi dahil olmak üzere çeşitli bilimsel alanlarda uygulamalar bulur. NWChem, araştırmacıların çeşitli kimyasal sistemleri incelemesine olanak tanıyan çok yönlülüğüyle tanınır ve açık kaynak yapısı, topluluk katkılarını ve özelleştirmeyi teşvik eder.

## VMD Hakkında

Visual Molecular Dynamics'in kısaltması olan VMD, moleküler dinamik (MD) yörüngelerin yanı sıra statik moleküler yapıları görüntülemek, analiz etmek ve canlandırmak için güçlü ve yaygın olarak kullanılan moleküler görselleştirme programıdır. Özellikle hesaplamalı kimya, moleküler biyoloji ve yapısal biyoinformatik alanlarında popülerdir. VMD, moleküllerin ve moleküler komplekslerin yüksek kaliteli 3 boyutlu görüntülerini sağlayarak moleküler yapıları görselleştirmede mükemmeldir. Çeşitli moleküler dosya formatlarını destekler.

## PyMOL Hakkında

PyMOL, moleküler yapıların üç boyutlu görselleştirilmesi için kullanılan bir moleküler görselleştirme sistemi ve yazılım aracıdır. Özellikle yapısal biyoloji, biyoinformatik ve hesaplamalı kimya alanlarında popülerdir. PyMOL, moleküler yapıların yüksek kaliteli 3 boyutlu görüntülerini sunarak kullanıcıların biyolojik makromoleküllerin şekillerini, yüzeylerini ve etkileşimlerini görselleştirmesine ve keşfetmesine olanak tanır.

## CUBE dosyası nasıl açılır?

CUBE dosyası aşağıdaki programlar kullanılarak açılabilir ve referans alınabilir.

- **NWChem** (Ücretsiz) (Windows, MAC, Linux) için

## Referanslar
* [Gauss Küp Dosya Formatı](https://paulbourke.net/dataformats/cube/)
