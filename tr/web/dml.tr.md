{
  "date" : "2021-05-25",
  "keywords" :[ "DML","DML dosyası", "DML dosya biçimi", "DML dosya türü", "dosya", "tür", "DML dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - DynaScript HTML Dosyası",
  "description":"DML dosya formatı ve DML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## DML dosyası nedir?

.dml uzantılı bir dosya, DyanScript ile oluşturulan bir web komut dosyası sayfası kod dosyasıdır. DynaScript, ECMAScript ile uyumlu ve diğer betik diliyle aynı özelliklerin çoğunu sağlayan dinamik bir [HTML](/tr/web/html/) betik dilidir. ColdFusion koduna ve Microsoft Active Server Pages (ASP) koduna benzer. DML dosyaları, diğer HTML sayfalarına benzer standart web tarayıcılarında açılabilir ve görüntülenebilir.

## DML Dosya Biçimi

DML dosyaları düz metin dosyası biçiminde oluşturulur ve kodu görüntülemek için bir metin düzenleyiciyle açılabilir. DML betik dili kullanılarak kod yazma, sunucu tarafında barındırılan DML sayfalarında dinamik olarak HTML oluşturmak için kullanılabilir. DynaScript'ler aşağıdaki dil öğelerinden oluşturulmuştur:


* SCRIPT etiketi - Bunlar, belgelere HTML yorumları olarak gömülür. Bir HTML yorumu \ ile işaretlenir <!-- tag.
* Sabit Değerler - Bunlar, DynaScript dosyalarındaki sabit değerlerdir. Bunlara örnek olarak s 123 , 0x3F , 0123 gibi tamsayılar, 456.789 , 3.2e-8 gibi kayan noktalı sayılar, true veya false gibi Boolean ve "İspanya'daki yağmur" gibi dizeler dahildir.
* Değişkenler - DynaScript değişkenlerinin tanımlanmasına veya sabit bir veri tipine atanmasına gerek yoktur. Bir ifadede kullanmadan önce bir değişkenin bir değeri olmalıdır; aksi takdirde bir çalışma zamanı uyarısı oluşturulur.
* İfadeler - Bunlar, değişkenlerin, değişmez değerlerin, operatörlerin ve diğer ifadelerin kombinasyonlarıdır. Bir atama ifadesinin sağ tarafı bir ifadedir.
* Operatörler - Bunlar, işlenen adı verilen bir veya daha fazla ifade üzerinde çalışır. Bunlar üçlü, ikili veya tekli olabilir: üçlü operatörler üç ifadeye göre hareket eder, ikili operatörler iki ifadeye göre hareket eder ve birli operatörler bir ifadeye göre hareket eder.
* İfadeler - Bunlar komut dosyası akışını, nesneleri manipüle etmeyi ve genel programlamayı kontrol eder. Genel olarak, bu ifadeler standart C ve Java sözdizimini takip eder. Örnekler if-else, do-while döngüleri, geçiş, ara, devam vb. diğer betik dilleri gibi.
* İşlevler - İşlevler, diğer herhangi bir betik dili gibi, bir dizi yönergeyi bir kez bir belgede işlev olarak kapsüllemenize ve ardından bunu belge boyunca (işlevi çağırarak) birkaç kez kullanmanıza olanak tanır. DynaScript ayrıca işlevleri de destekler.
* Nesneler - DynaScript nesne yönelimlidir ve `nesneleri' ve Kapsülleme, Polimorfizm ve Kalıtım gibi temel nesne yönelimli kavramları destekler.

