{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "kısmi", "uzantı", "dosya", "biçim", "web", "Gerçekten Basit Dağıtım","Kullanıcı Ülkesi Yazılımı"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Gerçekten Basit Dağıtım",
  "description":"RSS dosya formatı ve RSS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## RSS dosyası nedir? ##

.rss uzantılı bir dosya, Gerçekten Basit Dağıtım olarak bilinir. RSS, bilgisayar tarafından kolayca veya kolayca okunabilen bir dosya türü olan XML dosyasıdır. Bu XML dosyaları, bir web sitesinin veya web sayfasının verilerindeki veya güncellemelerindeki herhangi bir değişiklikle otomatik olarak güncellenir. Sitenin metadata (yazarın adı, yayıncının adı, yayınlanma tarihi vb.) Bu RSS dosyalarının en iyi özelliği ise gerçek zamanlı olarak çalışması ve güncellemelerin, haberlerin, yayınların yani en son yapılanların dosyanın üst kısmında görüntülenmesidir. Bir RSS dosyası kullanarak, ilgili içeriği web'den çekip bir RSS dosyası kullanarak okuyarak, ilgilendiğiniz herhangi bir konunun en son güncellemelerini içeren bir dosyayı kolayca oluşturabilirsiniz.

## Kısa Tarih ##

Etinde, RSS dosyası ilk olarak Netscape tarafından oluşturuldu, RSS dosyasının ilk sürümünü icat ettiler, ancak daha sonra fikri bıraktılar ve daha yeni sürümlerle devam etmediler. O zamanlar RSS dosya biçimi üzerinde çalışan ve onu daha yeni bir sürümle yenilemeye devam eden **Userland Yazılımı** idi, RSS v2 bu şekilde piyasaya çıktı. Bununla birlikte, RSS'nin icadı, 1997'de Ramanathan V tarafından yazılan Kaynak Açıklama Çerçevesine bağlanabilir. İki dosyanın işleyişi oldukça benzerdir ve RSS kavramının, RDF'nin çalışmasına dayalı olarak oluşturulduğunu varsaymak güvenlidir. meta verileri toplamak için kullanılan bir dosya okuyucu.

## Teknik Şartname ##

RSS dosyası bir tür XML dosyasıdır ve tüm RSS dosyalarının XML 1.0 standartlarına uyması gerekir. Diğerlerinin yanı sıra 0.91, 0.92, 2.0 gibi farklı RSS dosyalarının farklı sürümleri vardır. Her sürümün dosyası, o sürümün spesifikasyonlarına ve standartlarına uygundur.

## RSS Örneği ##

Aşağıda basitleştirilmiş bir RSS örneği verilmiştir.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Referans ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
