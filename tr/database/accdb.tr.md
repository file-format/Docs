{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDB dosya formatı ve ACCDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"ACCDB Dosya Biçimi - Microsoft Access 2007 Veritabanı Dosyası",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## ACCDB dosyası nedir?

.accdb uzantılı bir dosya, kullanıcı verilerini tablolarda depolayan bir Microsoft Access 2007 veritabanı dosyasıdır. Depolamayı destekler özel formlar, SQL sorguları ve diğer veriler. ACCDB dosyaları, Microsoft XML tabanlı dosya yapısına geçtikten sonra [MDB](/tr/database/mdb/) dosyalarının yerini aldı. ACCDB dosyaları hala eski uyumlulukla MDB'ye dönüştürülebilir. Ancak, ACCDB şu anda yaygın olarak kullanılan Access veritabanı dosya biçimidir. Microsoft ayrıca dosya eklerini, ikili verileri ve çok değerli alan desteğini depolama olasılığı gibi ACCDB biçimindeki ek özellikleri de destekledi.

## ACCDB Dosya Biçimi

MDB gibi, ACCDB dosya biçimi için de genel bir belirtim yoktur. Microsoft, Açık Veritabanı Bağlantısı (ODBC) standardı ve Visual Basic for Applications (VBA) aracılığıyla programlı olarak bu dosyalara erişimi destekler.

### Bir fikir

Basit bir ACCDB dosyasının onaltılık dökümü, önceki MDB Biçim Ailesinin en son sürümleriyle yapı bakımından genel benzerlikler olduğunu gösterir. Her iki dosya biçimi de 4096 baytlık sabit sayfa boyutları kullanır. ACCDB ve MDB arasındaki diğer bir benzerlik, ACCDB için "Standart ACE DB" dizesini içeren sihirli sayının biçimidir. Bir sürüm veya uyumluluk kodu, her iki biçimde de aynı konumdadır. mdbtools | HACKING dosyası, "Offset 0x14, bu veritabanının Jet sürümünü içerir" diyor ve resmi olmayan MDB Kılavuzu aynı fikirde. [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) için Wikipedia girişiyle birleştirilen bu kaynaklardaki bilgiler, 0x02 değerinin ACE 12'yi (Access 2007) ve 0x03'ün ACE'yi gösterdiğini gösterir. 14 (Erişim 2010). Ancak, Access 2010'da oluşturulan minimal bir veritabanı ve Access 2016'da oluşturulan benzer bir veritabanının her ikisi de bu konumda 0x02'ye sahiptir. Access 2016'da oluşturulan, ancak yeni tanıtılan "büyük tamsayı" veri türüyle bir sütun tanımlayan minimal bir veritabanı 0x05 değerine sahipti. ACCDB dosyalarında, bu gösterge, onu oluşturmak için kullanılan ACE motorunun sürümü yerine dosyanın uyumluluğunu yansıtıyor gibi görünmektedir.

## Referanslar

* [Erişim 2016 Spesifikasyonları](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Veritabanı Motoru](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Hangi Access dosya biçimini kullanmalıyım?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
