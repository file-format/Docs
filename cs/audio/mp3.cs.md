{
  "date" : "2019-12-13",
  "keywords" :[ "MP3", "soubor", "přípona", "formát", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů MP3 a rozhraních API, která mohou otevírat a vytvářet soubory MP3.",
  "title" :"MP3 - formát zvukového souboru",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## Co je soubor MP3?

Soubory s příponou .mp3 jsou digitálně kódované formáty souborů pro zvukové soubory, které jsou formálně založeny na MPEG-1 Audio Layer III nebo MPEG-2 Audio Layer III. Byl vyvinut společností Moving Picture Experts Group (MPEG), která používá kompresi zvuku Layer 3. Komprese dosahovaná formátem souborů MP3 je 1/10 velikosti souborů .WAV nebo .AIF. Tento formát poskytuje výhody streamování takových zvukových souborů přes internet pro poslech online, což dříve nebylo možné kvůli velké velikosti souborů zvukových souborů. Kvalitu zvuku zvukového souboru MP3 lze ovládat nastavením parametrů, jako je bitová rychlost, vzorkovací frekvence, společný nebo normální stereo.

## Stručná historie formátu souborů MP3

Formát MP3 byl vynalezen a vyvinut německou společností Fraunhofer-Gesellshart. Algoritmus má licencované patenty na technologii komprese, kterou používá. Zde je praktická časová osa MP3:

• **1987** – Fraunhoferův institut v Německu začal zkoumat vysoce kvalitní kódování zvuku s nízkou bitovou rychlostí. Jmenoval se projekt EUREKA EU147, Digital Audio Broadcasting.

• **leden 1988** – byla založena skupina expertů na pohyblivé obrázky neboli MPEG.

• **Duben 1989** – Fraunhofer získal v Německu patent na MP3.

• **1992** - Dieter Seitzer, který pomáhal Fraunhoferovi s jeho výzkumem, integroval své kódování zvuku do MPEG-1.

• **1993** – Byl publikován standard MPEG-1.

• **1994** – Standard MPEG-2 byl vyvinut a poté publikován o rok později.

• **Listopad 26, 1996** - Byl vydán americký patent na MP3.

• **Září 1998** – Fraunhofer začala prosazovat patentová práva. Kdo použil kódování zvuku MP3, zaplatil Fraunhoferovi licenční poplatek.

• **Únor 1999** – SubPop, nahrávací společnost, distribuovala hudbu ve formátu MP3, jako první taková společnost.

• **1999** – Objevují se první přenosné MP3 přehrávače.

## Formát souboru MP3

Soubor MP3 se skládá z rámců MP3, kde každý snímek obsahuje záhlaví a datový blok. Rámce nejsou nezávislé a obvykle je nelze extrahovat na libovolných hranicích rámců. Datové bloky souboru obsahují informace o zvuku z hlediska frekvencí a amplitud. Synchronizační slovo v záhlaví identifikuje začátek platného rámce. Poté následují 3 bity, kde první bit ukazuje, že se jedná o standard MPEG a zbývající 2 bity ukazují, že je použita vrstva 3; tedy MPEG-1 Audio Layer 3 nebo MP3. Poté se hodnoty budou lišit v závislosti na souboru MP3.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 definuje rozsah hodnot pro každou sekci záhlaví spolu se specifikací záhlaví. Většina souborů MP3 dnes obsahuje [ID3](https://en.wikipedia.org/wiki/ID3) [metadata](https://en.wikipedia.org/wiki/Metadata), které předchází nebo následuje za snímky MP3, jak je uvedeno v diagramu. Datový tok může obsahovat volitelný kontrolní součet.

## Reference ##

* [MP3 – z Wikipedie](https://en.wikipedia.org/wiki/MP3)

