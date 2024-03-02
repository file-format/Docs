{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"páirteach",
"síneadh",
"comhad",
"formáid",
"gréasáin",
"Sindeacáitiú an-Simplí",
"Bogearraí Userland"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS - Sindeacáitiú Fíor-Simplí",
  "description": "Foghlaim faoi fhormáid comhaid RSS agus APIanna ar féidir comhaid RSS a chruthú agus a oscailt.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-gas"
}
},
  "lastmod": "2021-06-24"
}

## Cad is comhad RSS ann? ##

Tugtar Sindeacáitiú Fíorshimplí ar chomhad leis an síneadh .rss. Is cineál comhaid é RSS a léann an ríomhaire go héasca nó go héasca, an comhad XML. Déantar na comhaid XML seo a nuashonrú go huathoibríoch le haon athruithe ar shonraí nó nuashonruithe ar shuíomh Gréasáin nó ar leathanach gréasáin. Baintear an fhaisnéis nuashonraithe mar aon leis na meiteashonraí (ainm an údair, ainm an fhoilsitheora, dáta foilsithe, etc.), agus ábhar gréasáin eile an tsuímh Ghréasáin as comhaid RSS an úsáideora agus cuirtear i láthair iad i bhformáid atá éasca le léamh. Is í an ghné is fearr de na comhaid RSS seo ná go n-oibríonn sé i bhfíor-am, agus na nuashonruithe, nuacht, foilsíonn, is é sin an ceann is déanaí, ar taispeáint ar bharr an chomhaid. Ag baint úsáide as comhad RSS, is féidir leat comhad a chruthú go héasca ina bhfuil na nuashonruithe is déanaí ar aon ábhar a bhfuil suim agat ann, tríd an ábhar gaolmhar a tharraingt ón ngréasán agus é a léamh ag baint úsáide as comhad RSS.

## Stair Ghearr ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. Tá oibriú an dá chomhad cosúil go leor agus tá sé sábháilte glacadh leis gur bunaíodh coincheap RSS bunaithe ar oibriú RDF, léitheoir comhaid a úsáideadh chun meiteashonraí a bhailiú.

## Sonraíocht Theicniúil ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Tá leaganacha éagsúla de chomhaid RSS éagsúla, mar shampla 0.91, 0.92, 2.0, i measc daoine eile. Cloíonn comhad gach leagan le sonraíochtaí agus caighdeáin an leagain shonraigh sin. 

## Sampla RSS ##

Seo a leanas sampla simplithe den RSS.

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
## Tagairt ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
