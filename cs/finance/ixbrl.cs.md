{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl", "soubor ixbrl", "formát souboru ixbrl", "typ souboru ixbrl", "soubor", "typ", "co je soubor ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Formát souboru obchodního a finančního výkaznictví",
  "description":"Další informace o formátu souboru IXBRL a rozhraních API, která mohou vytvářet a otevírat soubory IXBRL.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Co je soubor iXBRL?

Formát souboru iXBRL (ilnine XBRL) umožňuje vložení dat [XBRL](/cs/web/xbrl/) do souboru HTML, aby byly čitelné pro stroje i pro lidi. Je to ve skutečnosti soubor [xHTML](/cs/web/xhtml/), který používá značky XBRL a byl vyvinut společností XBRL International, aby splnil požadavky britského HMRC. Pomocí iXBRL lze vytvářet finanční výkazy se zachováním vzhledu původního dokumentu. Soubory iXBRL lze otevřít v libovolném textovém editoru, jako je Poznámkový blok v operačním systému Windows a TextEdit v systému MacOS.

## Formát souboru iXBRL

Uvnitř iXBRL je obsah XBRL zabalen do formátu souboru xHTML, který používá značky XML. Jako XBRL,<xbrl> je kořenový prvek souborů iXBRL. Formát XHTML představuje svůj obsah jako soubor různých typů dokumentů a modulů. Všechny soubory v XHTML jsou založeny na formátu souboru XML a odpovídají standardům dokumentů XML. XHTML je formát nezbytný pro provozní využití závislého [HTML](/cs/web/html/) Document Object Model (DOM) nebo [XML](/cs/web/xml/) Document Object Model. Pro vnější svět se iXBRL řídí specifikacemi formátu souboru [xHTML](/cs/web/xhtml/).

### iXBRL vs XBRL

XBRL lze porovnat s iXBRL na základě následujících faktorů:

* Složitost
* Možnosti formátování
* Typy souborů/přípony
* Možnost vykreslování
* Proces podání

Následující tabulka ilustruje tyto rozdíly.

|Parametr|XBRL|iXBRL|
---|---|---|
|Složitost|Složitější než iXBRL|Méně složité díky existujícímu organizačnímu schématu XHTML|
|Možnosti formátování|Omezená flexibilita|Vysoká flexibilita formátování obsahu|
|Typy souborů/Přípona|Formálně uloženo s příponou .xml|Obvykle uloženo jako přípona .html nebo .xhtml|
|Možnosti vykreslování|K jejich zobrazení jsou zapotřebí prohlížeče XBRL|Obsah čitelný člověkem, který lze zobrazit v prohlížečích|
|Proces archivace| Dokumenty instancí XBRL (strojově čitelné) a HTML (čitelné člověkem) je třeba ukládat samostatně.|V jediném dokumentu jsou k dispozici formáty čitelné pro člověka i strojově čitelné formáty|

## Reference

* [XBRL – podle Wikipedie](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

