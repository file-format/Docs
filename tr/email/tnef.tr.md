{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"TNEF dosya formatı ve TNEF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## TNEF dosyası nedir?

Aktarım Tarafsız Kapsülleme Formatı (TNEF), Mesajlaşma Uygulama Programlama Arayüzü'ne (**MAPI**) dayalı e-posta eklerini kapsüllemek için Microsoft'a özel bir formattır. Microsoft Outlook ve Microsoft Exchange Server, TNEF'i tamamen desteklerken daha sonra TNEF'in kodunu MAPI'ye çözer ve biçimlendirilmiş postaları görüntüler. TNEF kodlamasına sahip bir e-posta ekinde MIME tipi MS-TNEF bulunur ve winmail/win.dat olarak depolanır. Winmail .dat dosyasındaki ek, aşağıdaki bilgileri içerir:


|Mesaj|OLE nesneleri|Outlook özellikleri
---|---|---|
|<ul><li> Orijinal mesaj ekleri</li><li> Orijinal biçimlendirilmiş sürüm</li><li> yazı tipleri, metin boyutları ve metin renkleri</li></ul> |<ul><li> gömülü resimler</li><li> katıştırılmış Office belgeleri</li></ul> |<ul><li> özel formlar</li><li> oylama düğmeleri</li><li> toplantı istekleri</li></ul>


TNEF'i desteklemeyen diğer e-posta hizmetleri, TNEF formatlı mesajlar için düz metin sunar. Outlook, mesajın zengin bir biçimini TNEF dosyalarına (OLE) veya belirli Outlook özelliklerine (formlar, yoklama düğmeleri ve konferans istekleri) katıştırır. Outlook e-posta istemcisi içinde açık TNEF kodlamasını onaylamak mümkün değildir, ancak, bir e-postayı göndermek için RTF formatını seçmek, dolaylı olarak TNEF kodlamasını kolaylaştırır.

## TNEF Dosya Biçimi

TNEF veri algoritması, zengin hiyerarşik mesaj özelliklerinden düzleştirilmiş bir yapı oluşturur. Bu düzleştirilmiş yapılar daha sonra belirli özelliklerden oluşan bir seri veri akışını temsil etmek için kullanılır.

Özelliklerin gruplar halinde oluştuğu veya birden çok değere sahip olduğu bazı durumlarda akış, belirli bir veri hizalamasını zorunlu kılmak için sayımlar ve dolgular içerebilir. Bu algoritmanın kullanımının avantajlı olduğu ayırt edici bir durum, destekleyici olmayan bir mesajlaşma ortamındadır. Bu tür ortamlarda, zengin bir mesaj özelliği, bir TNEF Yazıcısı tarafından bir seri veri akışına kodlanır. Ayrıca, temeldeki TNEF'e ait olmayan özellikler iletim sırasında kapsüllenebilir. Bu kapsüllenmiş özellikler daha sonra orijinal mesajın tüm özelliklerinin istemci uygulamasına sunulmasını sağlamak için bir TNEF yoluyla kod çözülerek kullanılabilir hale getirildi.

TNEF'te tüm sayısal veri türleri küçük-endian'dır ve boyutları bir bayttan büyüktür. Bu sayısal değerlerin küçük olmayan platformlarda işlenmesi, doğru değerleri elde etmek için uygun dönüşümlerin yapılmasını gerektirir. Dize değerleri, [RFC5234] özelliklerine göre Artırılmış Backus-Naur Formu (ABNF) formatında temsil edilir. Dize boş karakterle sona erdiğinde, o da dahil edilir; örneğin, "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="TNEF Dosya Biçimi" >}}

## TNEF Öznitelikleri ve İşleme kuralları ##

TNEF'teki veri akışı, eski bir sürüm numarası, bir imza, bir ilkel anahtar değeri ve kod sayfasını temsil eden bir öznitelik ile başlar. Bu kod sayfası, kodlayıcı ANSI niteliklerini ve özelliklerini kaydettiğinde oluşturulur. Bundan sonra akış, önce mesaj özniteliklerinin ardından ek özniteliklerinin sıralandığı bir öznitelikler dizisi haline geldi. attMsgProps, attAttachment ve attRecipTable gibi özel niteliklerde farklı mesaj ve ek özellikleri bulunur. TNEF akışında görünen öznitelikler, bunları mesaj özellikleriyle birleştirmek için gerekli yapıyı, mesaj özelliklerini ve dönüştürmeleri içerir. Her öznitelik, uygulamaya göre bir kimlik, özniteliğin boyutu ve verileri, bir sağlama toplamı ve bir seviyeden oluşur.

## Protokoller ve Diğer Algoritmalarla İlişki ##

Zengin mesaj formatını görüntülemek için zayıf mekanizmaya sahip sistemler, aktarım için doğal olarak TNEF veri algoritmasına ihtiyaç duyar. ms-TNEF ortam türünü kullanan algoritmanın çıktısı, bir ek dosyasından (winmail.dat) ve [RFC2045] içinde belirtilen MIME'nin bir gövde kısmından oluşur. Düz metin mesaj gövdesi, [MSDN-UAF] spesifikasyonuna göre UUENCODE kullanılarak iletilir ve bu mesaj gövdesi veya eşdeğer yöntemin kodu alıcı tarafta çözülür. Ayrıca TNEF, SMTP, POP3, IMAP4 gibi farklı internet protokollerini ve RFC2045 standardına göre MIME'yi entegre edenleri kullanarak mesaj verilerini iletebilir.

## Uygulanabilirlik Beyanı ##

Basit mesaj iletimine ek olarak, TNEF'in orijinal uygulaması, mesaj sınıflarını kullanmak ve taşıma protokolünde orijinal desteği olmayan ek özellikleri desteklemek için oluşturulacaktı. Bu uygulama, günümüzde modern mesajlaşma istemcilerinin kullandığı zengin mesaj özelliklerinin ve adlandırılmış özelliklerin iletimi için daha da geliştirildi. Orijinal uygulamaya uygunluk için orijinal öznitelik sözdizimi korunur ve özel bir öznitelik yeni mesaj özelliklerini ayrı tutar.

## Referanslar

* [Transport Nötr Kapsülleme Biçimi](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Exchange Server'daki e-posta adresleri ve adres defterleri](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Aktarım Tarafsız Kapsülleme Biçimi (TNEF) Veri Algoritması](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

