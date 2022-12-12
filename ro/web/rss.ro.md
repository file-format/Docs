{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "parțial", "extensie", "fișier", "format", "web", "Sindicare foarte simplă", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS – Sindicare cu adevărat simplă",
  "description":"Aflați despre formatul de fișier RSS și despre API-urile care pot crea și deschide fișiere RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Ce este un fișier RSS? ##

Un fișier cu extensia .rss este cunoscut sub numele de Really Simple Syndication. RSS este un tip de fișier ușor sau ușor de citit de computer, fișierul XML. Aceste fișiere XML sunt actualizate automat cu orice modificări ale datelor sau actualizări ale unui site web sau unei pagini web. Informațiile actualizate împreună cu metadatele (numele autorului, numele editorului, data publicării etc.) și alte conținuturi web ale site-ului web sunt extrase de fișierele RSS ale utilizatorului și prezentate într-un format ușor de citit. Cea mai bună caracteristică a acestor fișiere RSS este că funcționează în timp real, iar actualizările, știrile, publicările, adică cele mai recente, sunt afișate în partea de sus a fișierului. Folosind un fișier RSS, puteți crea cu ușurință un fișier care conține cele mai recente actualizări ale oricărui subiect care vă interesează, trăgând conținutul aferent de pe web și citindu-l folosind un fișier RSS.

## Scurt istoric ##

În trupul său, fișierul RSS a fost creat pentru prima dată de Netscape, au inventat prima versiune a fișierului RSS, dar apoi au renunțat la idee și nu au continuat cu versiuni mai noi. Atunci **Userland Software** a lucrat la formatul de fișier RSS și a continuat să-l inoveze cu o versiune mai nouă, așa a intrat pe piață RSS v2. Cu toate acestea, invenția RSS poate fi legată înapoi la Resource Description Framework, de către Ramanathan V în 1997. Funcționarea celor două fișiere este destul de similară și este sigur să presupunem că conceptul de RSS a fost format pe baza funcționării RDF, un cititor de fișiere care a fost folosit pentru a colecta metadate.

## Specificatii tehnice ##

Fișierul RSS este un tip de fișier XML și toate fișierele RSS trebuie să respecte standardele XML 1.0. Există diferite versiuni ale diferitelor fișiere RSS, cum ar fi 0.91, 0.92, 2.0, printre altele. Fișierul fiecărei versiuni este conform cu specificațiile și standardele acelei versiuni specifice.

## Exemplu RSS ##

Următorul este un exemplu simplificat de RSS.

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
## Referință ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
