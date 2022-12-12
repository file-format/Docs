{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "soubor", "rozšíření", "formát", "E-kniha", "Digitální kniha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru EPUB a rozhraních API, která mohou vytvářet a otevírat soubory EPUB.",
  "title" :"Co je soubor EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Co je soubor EPUB?

Soubory s příponou .epub jsou formát souboru e-knihy, který vydavatelům a spotřebitelům poskytuje standardní formát digitální publikace. Tento formát je již tak běžný, že jej podporuje mnoho elektronických čteček a softwarových aplikací. Například v systému Mac OS poskytuje předinstalovaný software **Books** podporu pro otevírání takových souborů. Kromě toho je k dispozici spousta kompatibilního softwaru pro chytré telefony, tablety a počítače. Standardy souborů EPUB jsou udržovány [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Verzi EPUB 3 podporuje také Book Industry Study Group (BISG), přední knižní obchodní sdružení pro standardizované osvědčené postupy, výzkum, informace a akce pro balení obsahu.

## Stručná historie formátu souborů EPUB

* **Říjen 2007** – EPUB 2.0 byl schválen
* **Září 2010** - Byla vydána aktualizace údržby
* **Říjen 2011** – Specifikace EPUB 3.0 vstoupily v platnost
* **Červen 2014** – Byla vydána drobná aktualizace údržby, která nahrazuje verzi 3.0
* **Leden 2017** – EPUB 3.1 vstoupil v platnost

## Formát souboru EPUB

Formát souboru EPUB je archiv, který lze přejmenovat na příponu [ZIP](/cs/komprese/zip/) a jeho obsah lze zobrazit rozbalením archivu pomocí libovolného extraktoru archivu. Je to otevřený formát založený na XML a skládá se ze souborů HTML, obrázků, šablon stylů CSS a dalších prvků. Lze jej také převést do PDF, Mobi a několika dalších formátů souborů prostřednictvím řady softwarových aplikací a rozhraní API.

{{< figure src="../epub.png" alt="Formát souboru EPUB" >}}

**E-kniha EPUB otevřena pomocí aplikace Knihy Mac OS**

Formát souboru EPUB je založen na následujících třech otevřených standardech.

### Otevřená veřejná struktura (OPS) ###

Soubor EPUB 2.0 používá k vytvoření obsahu publikace XHTML 1.1. V podstatě to znamená, že soubor EPUB se skládá z jedné nebo více webových stránek. I když byste mohli zahrnout celý obsah knihy nebo novin na jednu stránku, je lepší, aby takový soubor nepřesáhl 300 kB, a to jak z důvodu výkonu, tak z důvodů kompatibility. Stejně jako u běžných webových stránek je styl a rozvržení definováno pomocí kaskádových stylů (CSS). V souborech EPUB je třeba použít podmnožinu (omezenou řadu příkazů) CSS2. Mnoho nových funkcí CSS3, jako jsou zaoblené rámečky nebo vržené stíny, zatím není k dispozici. Pro zpětnou kompatibilitu může tvůrce ke kódování obsahu použít místo XHTML také DTBook.

### Open Packaging Format (OPF) ###

Tato část specifikací se zabývá strukturálními informacemi, jako jsou metadata (kdo je autor a vydavatel, jaký je název atd.), manifest (seznam všech souborů v souboru epub) a obsah. Tato data jsou všechna vložená pomocí XML.

### Formát otevřeného kontejneru (OCF) ###

Jak by mělo být z výše uvedených popisů jasné, dokument EPUB se skládá z řady souborů. Specifikace OCF definují, jak se všechny tyto soubory nakonec zabalí do jednoho souboru kontejneru. K tomu slouží ZIP komprese.

## Podporované formáty obrazových souborů ##

Formát souboru EPUB podporuje následující formáty souborů obrázků.

* [GIF](/cs/image/gif/)
* [JPG](/cs/image/jpeg/)
* [PNG](/cs/image/png/)
* [SVG](/cs/page-description-language/svg/)

## Reference ##

* [EPUB – z Wikipedie](https://en.wikipedia.org/wiki/EPUB)

