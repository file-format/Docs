{
"tarih": "2023-04-20",
  "keywords": [
"ldb dosyası",
"ldb dosyası nedir",
"ldb hangi bilgileri içerir",
"ldb dosyasının amacı nedir",
"ldb uzantısı",
"dosya",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LDB Dosya Formatı - Microsoft Access Kilit Dosyası",
  "description":"LDB formatı ve hangi bilgileri içerdiği hakkında bilgi edinin.",
"linktitle" : "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"sonmod": "2023-04-20"
}

## .LDB dosyası nedir?

LDB dosyası, birden fazla kullanıcının aynı veritabanını aynı anda düzenlemesini önlemek için Microsoft Access tarafından kullanılan bir kilit dosyasıdır. Kullanıcı bir Access veritabanını açtığında Access, veritabanıyla aynı dizinde karşılık gelen bir LDB dosyası oluşturur. Bu dosya, veritabanını halihazırda kimin kullandığı ve hangi kayıtları düzenlediğine ilişkin bilgileri içerir.

LDB dosyası, veritabanı açıldığında Microsoft Access tarafından otomatik olarak oluşturulur ve veritabanı kapatıldığında silinir. LDB dosyasının hiçbir zaman manuel olarak silinmemesi gerektiğini unutmamak önemlidir çünkü bu, veritabanında sorunlara neden olabilir.

Microsoft Access veritabanıyla ilgili sorunlarla karşılaşırsanız olası çözümlerden biri, o veritabanıyla ilişkili LDB dosyasını silmeyi denemektir. Bu, veritabanına erişmenizi engelleyebilecek tüm kilitleri serbest bırakacaktır. Ancak, LDB dosyasının silinmesi, yanlış yapılması durumunda veri kaybına veya bozulmasına neden olabileceğinden, bunu denemeden önce veritabanının yedeğini aldığınızdan emin olun.

## LDB Dosya Formatı - Daha Fazla Bilgi

Microsoft Access'teki bir LDB dosyası, veritabanına şu anda erişen kullanıcılar hakkında kullanıcı adı, bilgisayar adı ve oturum açma zamanı gibi bilgiler içerir. LDB dosyası ayrıca, hangi kayıtların hangi kullanıcı tarafından düzenlendiği gibi veritabanına yerleştirilen kilitlerle ilgili bilgileri de içerir.

Bir LDB dosyasında bulunabilecek bilgi türlerinin daha ayrıntılı listesi aşağıda verilmiştir:

- **Kullanıcı adı** - şu anda veritabanına erişen kullanıcının adı
- **Bilgisayar adı** - kullanıcının veritabanına eriştiği bilgisayarın adı
- **Oturum açma zamanı** - kullanıcının veritabanını ilk açtığı zaman
- **Kayıt kilitleri** - hangi kayıtların hangi kullanıcı tarafından düzenlendiğine ilişkin bilgiler
- **Nesne kilitleri** - hangi veritabanı nesnelerinin (tablolar, formlar veya raporlar gibi) şu anda hangi kullanıcı tarafından düzenlendiğine ilişkin bilgiler
- **Bağlantı bilgileri** - kullanıcının veritabanına nasıl bağlandığına ilişkin bilgiler (örneğin, yerel bağlantı mı yoksa ağ bağlantısı mı kullandığı)

LDB dosyasındaki bilgiler Microsoft Access tarafından birden fazla kullanıcının aynı anda aynı veritabanında çakışan değişiklikler yapmasını önlemek için kullanılır. Kullanıcı başka bir kullanıcı tarafından kilitlenmiş bir kaydı veya nesneyi düzenlemeye çalıştığında Microsoft Access, nesnenin zaten kullanımda olduğunu belirten bir mesaj görüntüler. LDB dosyası, kullanıcılar veritabanını açıp kapattıkça ve kilitli nesnelerde değişiklik yaptıkça güncellenir.

## Referanslar
* [LDB Dosyası Nedir?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

