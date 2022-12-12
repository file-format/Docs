{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA fájlformátum",
  "description":"További információ a PDF/UA fájlformátumról és az API-król, amelyek PDF/UA fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Mi az a PDF/UA fájl? #

A PDF/UA [ISO 14289-1-es szabvány] (https://en.wikipedia.org/wiki/ISO_14289) néven jelent meg 2012 augusztusában, és messze az első teljes körű meghatározás az univerzálisan hozzáférhető PDF-dokumentumokra vonatkozó követelményekről. Az „univerzálisan hozzáférhető” kifejezés arra utal, hogy a [PDF](/hu/pdf/) dokumentumban szereplő információknak egyformán és függetlenül kell hozzáférhetőnek lenniük általában mindenki, és különösen a fogyatékkal élők számára. A PDF/UA szabvány bevezetése jelentős lépésnek tekinthető a PDF-tartalom létrehozásához és olvasásához szükséges eszközök és alkalmazások létrehozásában.

## Fájlformátumra vonatkozó követelmények ##

A PDF/UA-nak van néhány meghatározott követelménye az alapjában, amelyek a szabvány lényegét képezik. Ezek lényegében a PDF-ek címkézésén alapulnak, ami azt jelenti, hogy minden PDF/UA-dokumentumot megfelelően címkézni kell. Azt is megköveteli, hogy a címkék szemantikailag megfelelőek és logikai sorrendben legyenek. Ez biztosítja, hogy a PDF/UA specifikációkkal létrehozott végdokumentum megbízhatóbb és hozzáférhetőbb legyen. Ez megkérdőjelezi a PDF-szerkesztőket, hogy mindent tudniuk kell-e az összes ilyen követelményről? Szerencsére ez nem így van, mivel a PDF/UA megfelelőségi eszközök vállalják a felelősséget a PDF hozzáadásáért és hozzáférhetőségének megőrzéséért.

A PDF/UA fájlformátum követelményei a következők.

* A tartalom kétféleképpen van besorolva: értelmes tartalom és műalkotások, például díszítő oldalelemek. Minden értelmes tartalmat fel kell címkézni, és integrálni kell a dokumentumon belüli összes címke szerkezeti fájába. A műtárgyakat viszont csak ilyenként kell megjelölni.
* Az értelmes tartalmat címkékkel kell megjelölni, és a dokumentum többi címkéjével együtt teljes szerkezetfát kell létrehozni.
* Az értelmes tartalmat a megfelelő szemantikai címkékkel kell jelölni.
* A dokumentumcímkék által létrehozott szerkezetfának tükröznie kell a dokumentum logikai olvasási sorrendjét.
* Csak a PDF 1.7-ben meghatározott szabványos címkék használhatók; Ha bármilyen más címkét használnak, a szerep-hozzárendelési bejegyzésnek rögzítenie kell, hogy mindegyik melyik szabványos címkét képviseli.
* Az információ nem közvetíthető kizárólag vizuális eszközökkel (pl. kontraszt, szín vagy pozíció az oldalon).
* Tilos villogó, villogó vagy villogó tartalom sem JavaScript által vezérelt effektusként, sem a PDF-be ágyazott videók részeként.
* Meg kell adni a dokumentum címét, és a dokumentumot úgy kell beállítani, hogy a cím (nem pedig a fájlnév) jelenjen meg az ablak címében.
* Minden tartalom nyelvezetét fel kell jegyezni, és a nyelvi változásokat kifejezetten meg kell jelölni.

## PDF/UA megfelelőség ##

A PDF/UA szabvány meghatározza a tartalom, az olvasók és a kisegítő technológia specifikációit. Ez a három szempont a dokumentum tartalma alapján kapcsolódik egymáshoz. Ezek mindegyikére vonatkozó megfelelőségi követelmények az alábbiakban szerepelnek.

## Megfelelő fájlok ##

A PDF/UA szabványnak megfelelő fájloknak tartalmazniuk kell a [PDF 1.7 specifikációi] (http://www.adobe.com/go/pdfreference) szerint érvényes funkciókat. A PDF/UA által kifejezetten tiltott funkciókat azonban ki kell zárni.

## Megfelelő olvasók ##

A megfelelő olvasónak be kell tartania a PDF 1.7 specifikációiban leírt szabályokat. Konkrétan támogatnia kell:

* a kisegítő lehetőségekhez megadott összes címke, attribútum és kulcsérték. Ezenkívül képesnek kell lennie a digitális aláírások, megjegyzések és opcionális tartalom feldolgozására és megjelenítésére.
* feldolgozza és képviseli a digitális aláírásokat, megjegyzéseket és az opcionális tartalmat
* különféle eszközökkel navigálhat a dokumentumban

## Megfelelő kisegítő technológia ##

Egy megfelelő kisegítő technológia szükséges a PDF/UA funkciók támogatásához. Ide tartoznak például a tartalom és az olvasó jellemzői, és lehetővé kell tenniük az oldalcímkék, a dokumentumstruktúra vagy a vázlat szerinti navigációt. Azt is lehetővé kell tennie, hogy a felhasználó felülbírálja az alapértelmezett navigációs nagyítást.

## Referenciák ##

* [PDF/UA – a Wikipédia által](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA dióhéjban](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

