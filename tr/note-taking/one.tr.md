{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote Dosya Biçimi",
  "description":"BİR dosya biçimi ve BİR dosya oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## .ONE dosyası nedir? ##

.ONE uzantısıyla temsil edilen dosya, Microsoft OneNote uygulaması tarafından oluşturulur. OneNote, not almak için taslak defterinizi kullanıyormuşsunuz gibi uygulamayı kullanarak bilgi toplamanıza olanak tanır. OneNote dosyaları, belge sayfalarında sabit olmayan konumlara yerleştirilebilen farklı öğeler içerebilir. Bu öğeler metin, sayısallaştırılmış el yazısı ve resimler, çizimler ve multimedya (ses/video) klipleri dahil diğer uygulamalardan kopyalanan nesneleri içerebilir. Microsoft artık Office365'in bir parçası olarak, Notların internet üzerinden diğer OneNote kullanıcılarıyla paylaşılabileceği çevrimiçi OneNote sürümünü sunuyor.

## .ONE Dosya Biçimi Özellikleri ##

OneNote dosya formatı, dijital notları hiyerarşik bölüm ve sayfa kümeleri olarak temsil etmenin etkili bir yolunu sağlar. Her sayfa, dosya biçimi Belge Nesne Modeli (DOM) tarafından temsil edilmek üzere belirli bir yapıda kullanıcı tanımlı içerik içerir. Bu format için veri modeli aşağıda gösterildiği gibidir.

### Yapıya Genel Bakış ###

OneNote dosya biçimi için veri modelinde gösterildiği gibi, bir OneNote belgesi farklı öğelerden oluşur.

#### Bölüm ####

Bölüm, OneNote dosyasındaki en üstteki kapsayıcıdır ve içinde ayrıca aşağıdaki gibi farklı öğeler içerir:

* Sayfalar
* Meta veriler
* Özellikleri

Meta veriler ve özellikler, bölüm adını, bölümde bulunan sayfaların kimliğini ve bu sayfaların görüntülenme sırasını içerir. "Bölüm" terimi, bir bölümdeki tüm sayfaları ve bu verilerin .one dosya adı uzantısına sahip bir OneNote® düzeltme deposu dosyasındaki temsilini ifade eder.

#### Sayfa ####

OneNote belgesindeki kullanıcı tanımlı içerik, bir sayfanın içinde bulunur. Sayfa bilgileri metin, listeler, tablolar, sayfa başlıkları, resimler ve not etiketlerini içerir. Bir sayfa, içerilen nesnelerin çoğunun eklendiği anahat nesnelerinden oluşur. Anlamlı gösterim için her sayfaya bir ad verilebilir ve nesneler doğrudan sayfalara da eklenebilir. Bir sayfa ayrıca hiyerarşik bir sistemde alt sayfalar içerebilir.

#### Özellikler ve Özellik Kümeleri ####

OneNote içeriği, özelliklerden, özellik kümelerinden ve dosya veri nesnelerinden oluşur. Özellik kümesi, bir tür içeriği temsil eden bir özellikler koleksiyonudur. Bir dosya veri nesnesi, resimler, katıştırılmış dosyalar veya ses/video içeriği içeren bir ikili veri bloğudur.

#### OneNote Not Defteri ####

Not defteri, aynı dizinde depolanan bölüm dosyalarının bir koleksiyonudur. Not defteri içindeki bölümlerin sırası ve not defterinin rengi gibi ayarları belirtmek için bir özellikler koleksiyonu kullanılır.

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

|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bayt):` İşaretsiz bir tamsayı. Bu dosyanın dosya biçimine bağlı olarak aşağıdaki tablodaki değerlerden biri OLMALIDIR.

|Dosya Biçimi|Değer
--- | --- |
|.bir|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bayt):` "fcrZero" değerine sahip OLMALIDIR **FileChunkReference32** yapısı.

`fcrLegacyTransactionLog (8 bayt):` "fcrNil" OLMALIDIR **FileChunkReference32** yapısı.

`cTransactionsInLog (4 bayt):` İşlem günlüğündeki işlem sayısını belirten işaretsiz bir tamsayı. Sıfır OLMAMALIDIR.

`cbLegacyExpectedFileLength (4 bayt):` Sıfır olması GEREKEN ve yok sayılması GEREKEN işaretsiz bir tamsayı.

`rgbPlaceholder (8 bayt):` Sıfır olması GEREKEN ve yok sayılması GEREKEN işaretsiz bir tamsayı.

`fcrLegacyFileNodeListRoot (8 bayt):` "fcrNil" OLMALIDIR **FileChunkReference32** yapısı.

`cbLegacyFreeSpaceInFreeChunkList (4 bayt):` Sıfır olması GEREKEN ve yok sayılması GEREKEN işaretsiz bir tamsayı.

`fNeedsDefrag (1 bayt):` dikkate alınmamalıdır ZORUNLU.

`fRepairedFile (1 byte):` göz ardı edilmelidir.

`fNeedsGarbageCollect (1 bayt):` dikkate alınmamalıdır ZORUNLU.

`fHasNoEmbeddedFileObjects (1 byte):` Sıfır olması GEREKEN ve yok sayılması GEREKEN işaretsiz bir tamsayı.

`guidAncestor (16 bayt):` İçindekiler dosyasının **Header.guidFile** alanını belirten ve aşağıdaki tabloda verilen bir GUID:


|İçindekiler Dosya Biçimi|İçindekiler Dosyasının Konumu
--- | --- |
|Bölüm Dosyası - .One|İçindekiler dosyası bu dosyayla aynı dizinde bulunur.
|İçindekiler Dosyası - .onetoc2|İçindekiler dosyası bu dosyanın üst dizininde bulunur.

GUID {00000000-0000-0000-0000-000000000000} ise, bu alan bir içindekiler tablosu dosyasına başvurmaz.

`crcName (4 bayt):` Bu revizyon depolama dosyasının adının CRC değerini belirten işaretsiz bir tamsayı. Ad, dosya adının uzantısı ve sonunda ek bir boş karakterle Unicode temsilidir. Bu CRC, bu revizyon deposu dosya biçiminden bağımsız olarak her zaman .one dosyası için CRC algoritması kullanılarak hesaplanır.

`fcrHashedChunkList (12 bayt):` Bir karma yığın listesindeki ilk **FileNodeListFragment**'e bir başvuruyu belirten bir **FileChunkReference64x32** yapısı. **FileChunkReference64x32** yapısının değeri "fcrZero" veya "fcrNil" ise karma yığın listesi mevcut değildir.

`fcrTransactionLog (12 bayt):` Bir işlem günlüğündeki ilk **TransactionLogFragment** yapısına bir başvuruyu belirten bir **FileChunkReference64x32** yapısı. **fcrTransactionLog** alanının değeri "fcrZero" OLMAMALIDIR ve "fcrNil" OLMAMALIDIR.

`fcrFileNodeListRoot (12 bayt):` Bir kök dosya düğümü listesine başvuru belirten bir **FileChunkReference64x32** yapısı. **fcrFileNodeListRoot** alanının değeri "fcrZero" OLMAMALIDIR ve "fcrNil" OLMAMALIDIR.

`fcrFreeChunkList (12 bayt):` İlk **FreeChunkListFragment** yapısına bir başvuru belirten bir **FileChunkReference64x32** yapısı. **FileChunkReference64x32** yapısının değeri "fcrZero" veya "fcrNil" ise, serbest öbek listesi mevcut değildir.

`cbExpectedFileLength (8 bayt):` Bu revizyon depolama dosyasının boyutunu bayt cinsinden belirten işaretsiz bir tamsayı.

`cbFreeSpaceInFreeChunkList (8 bayt):` Boş yığın listesi tarafından belirtilen boş alanın boyutunu bayt cinsinden belirtmesi GEREKEN işaretsiz bir tamsayı.

`guidFileVersion (16 bayt):` BİR GUID. **cTransactionsInLog** alanının veya **guidDenyReadFileVersion** alanının değeri değiştirilirken **guidFileVersion** yeni bir GUID olarak değiştirilmelidir ZORUNLU.

`nFileVersionGeneration (8 bayt):` Dosyanın kaç kez değiştiğini belirten işaretsiz bir tamsayı. **guidFileVersion** alanı değiştiğinde ARTIRILMALIDIR.

`guidDenyReadFileVersion (16 bayt):` BİR GUID. Dosyanın **Başlık** yapısı ve kullanılmayan depolama blokları hariç, dosyanın mevcut içeriği değiştirilirken, **guidDenyReadFileVersion** yeni bir GUID olarak DEĞİŞTİRİLMESİ GEREKİR.

`grfDebugLogFlags (4 bayt):` sıfır OLMALIDIR. göz ardı edilmelidir.

`fcrDebugLog (12 bayt):` "fcrZero" değerine sahip OLMALIDIR **FileChunkReference64x32** yapısı. göz ardı edilmelidir.

`fcrAllocVerificationFreeChunkList (12 bayt):` "fcrZero" OLMALIDIR **FileChunkReference64x32** yapısı. göz ardı edilmelidir.

`bnCreated (4 bayt):` Bu revizyon deposu dosyasını oluşturan uygulamanın yapı numarasını belirten işaretsiz bir tamsayı. Göz ardı edilmelidir.

`bnLastWroteToThisFile (4 bayt):` Bu revizyon deposu dosyasına en son yazan uygulamanın yapı numarasını belirten işaretsiz bir tamsayı. Göz ardı edilmelidir.

`bnOldestWritten (4 bayt):` Bu revizyon deposu dosyasına yazan en eski uygulamanın yapı numarasını belirten işaretsiz bir tamsayı. Göz ardı edilmelidir.

`bnNewestWritten (4 bayt):` Bu revizyon deposu dosyasına yazan en yeni uygulamanın yapı numarasını belirten işaretsiz bir tamsayı. Göz ardı edilmelidir.

`rgbReserved (728 bayt):` sıfır OLMALIDIR. göz ardı edilmelidir.

## Referanslar ##

* [[MS-ONEstore] - OneNote Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

