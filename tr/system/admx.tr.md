{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX Dosyası - Grup İlkesi Yönetim Şablonu Dosya Biçimi",
  "description":"ADMX dosya formatı ve ADMX dosyalarının nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADMX dosyası nedir?

ADMX dosyası, bir gruptaki bilgisayar grubunu yöneten Microsoft Windows Grup İlkesi yazılımı tarafından kullanılan bir ilke yapılandırma dosyasıdır. XML tabanlı bir yönetim şablonu dosyasıdır ve Windows Vista Service Pack 1 ile birlikte sunulmuştur. ADMX dosyaları, kullanıcı hesapları, işletim sistemi yapılandırmaları ve uygulamalar için yapılandırma ayarlarını içerir. ADMX dosyaları, birçok bilgisayar sisteminin merkezi yönetimine yönelik yapılandırmaları depolamak ve dağıtmak için kullanılır.

Herhangi bir XML uyumlu, herhangi bir metin düzenleyiciyi veya Microsoft Grup İlkesi Nesne Düzenleyicisini kullanarak ADMX dosyaları oluşturabilir veya düzenleyebilirsiniz.

## ADMX Dosya Formatı - Daha Fazla Bilgi

ADMX dosyaları, insanlar tarafından okunabilen evrensel [XML](/tr/web/xml/) dosya formatında saklanır. Çok dilli bir dosya formatıdır ve farklı dillerdeki sistem yöneticilerinin aynı ADMX dosyalarıyla çalışmasına olanak tanır. ADMX dosyaları, unicode formatlı bir metin dosyası formatı olan eski [ADM](/tr/system/adm/) dosya formatının yerini aldı. ADMX dosyaları, belirli bir Grup İlkesi ayarı değiştirildiğinde değiştirilecek kayıt defteri anahtarlarını belirtir.

### ADMX dosyasıyla ne yapabilirim?

ADMX dosyaları, bir grubun parçası olan kullanıcı bilgisayarlarına hangi eylemlere izin verileceğini tanımlar. Grup ilkesi, Active Directory yazılımıyla birlikte belirlenen kuralları uygular. ADMX dosyaları, etki alanında merkezi bir konum olan Windows işletim sistemindeki merkezi depodan yönetilir.

Bir çalışma ortamında dağıtılan bir ADMX dosyası, yöneticilerin aşağıdaki gibi politikaları uygulamasına olanak sağlayabilir:

* İnternet kullanımını kontrol edin
* Belirli dosya türlerinin indirilmesi
* Sistemlerde çıkarılabilir cihazların kullanımı

## Referanslar

* [Yönetim Şablonu Dosyaları - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Yönetim Şablonu Dosyalarını Yönetme](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

