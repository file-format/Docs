{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote Dosya Biçimi",
  "description":"ONETOC2 dosya formatı ve ONETOC2 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2 nedir? ##

[Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) uygulamasıyla çalışanlar not defteri klasöründe .onetoc2 dosyalarının olduğunu fark etmiş olabilir. Microsoft OneNote, bir not defterindeki farklı not alma bölümlerinin sıralanması hakkında bir dizin tutmak için İçindekiler Tablosu olarak ikili .onetoc2 dosyası oluşturur. Not defteri, aynı dizinde depolanan bölüm dosyalarının bir koleksiyonudur. .onetoc2 dosyası, not defteri içindeki bölümlerin sırası ve not defterinin rengi gibi ayarları belirtmek için bir özellikler koleksiyonu kullanır.

OneNote 2016'da bir not defteri oluşturduğunuzda, otomatik olarak yeni 2010-2016 dosya biçiminde kaydedilir. Matematik denklemleri ve bağlantılı notlar gibi OneNote 2016'daki tüm özelliklerin düzgün çalışmasını istiyorsanız bu biçime ihtiyacınız olacak.

## ONETOC2 Dosya Biçimi ##

.onetoc2 dosya formatı, OneNote Revizyon Deposu Dosya Formatı olarak temsil edilir ve özellik kümelerine sahip nesneleri içeren ve eşzamansız ortamda dosya bütünlüğünü sağlamak için bir işlem günlüğü içeren, çapraz referanslı nesne alanlarında düzenlenen bir revizyon deposunu belirten bir yapılar koleksiyonudur. yazar. .onetoc2 dosya formatının tüm belirtimleri [çevrimiçi](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) mevcuttur ve uygulamaların geliştirilmesi için başvurulabilir .

### Dosya Yapısı ###

Bir revizyon deposu dosyası **Başlık** yapısıyla başlamalıdır ZORUNLU. Dosyanın geri kalanı, her bloğun boyutunun ve yapısının kendisine başvuran alan tarafından belirlendiği bayt bloklarına bölünmüştür. Bir bloğa **Başlık** yapısı tarafından başvuruluyorsa veya başka bir erişilebilir bloktaki bir alan tarafından başvuruluyorsa erişilebilirdir. **Başlık** yapısı ve erişilebilir bloklar dışındaki veriler dikkate alınmamalıdır ZORUNLU.

Tüm yapılar 1 baytlık sınırlar üzerinde hizalanır. Aksi belirtilmedikçe tüm tamsayılar imzalanır. Aksi belirtilmedikçe tüm alanlar [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) şeklindedir.

#### Başlık ####

.ONE dosyasının Başlığı, aşağıdaki gibi dosya bilgilerinin temsili için farklı benzersiz kimlikler ve alanlar içeren parçalardan oluşur:

`guidFileType (16 bayt):` Revizyon depolama dosyasının türünü belirten bir GUID. Aşağıdaki tablodaki değerlerden biri OLMALIDIR.

|Dosya Biçimi|Değer
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bayt):` Bu revizyon depolama dosyasının kimliğini belirten bir GUID. Küresel olarak benzersiz OLMALIDIR.

`guidLegacyFileVersion (16 bayt):` "{00000000-0000-0000-0000-000000000000}" OLMALIDIR ve dikkate alınmamalıdır ZORUNLU.

`guidFileFormat (16 bayt):` Dosyanın bir revizyon depolama dosyası olduğunu belirten bir GUID. "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}" OLMALIDIR.

`ffvLastCodeThatWroteToThisFile (4 bayt):` İşaretsiz bir tamsayı. Dosya türüne bağlı olarak aşağıdaki tablodaki değerlerden biri OLMALIDIR.

|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bayt):` İşaretsiz bir tamsayı. Bu dosyanın dosya biçimine bağlı olarak aşağıdaki tablodaki değerlerden biri OLMALIDIR.


|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bayt):` İşaretsiz bir tamsayı. Bu dosyanın dosya biçimine bağlı olarak aşağıdaki tablodaki değerlerden biri OLMALIDIR.
:


|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bayt):` İşaretsiz bir tamsayı. Bu dosyanın dosya biçimine bağlı olarak aşağıdaki tablodaki değerlerden biri OLMALIDIR.


|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

## Referanslar ##

* [[MS-ONEstore] - OneNote Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

