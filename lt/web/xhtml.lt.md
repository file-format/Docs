{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"išplečiamas html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML – išplečiamas hiperteksto žymėjimo kalbos failo formatas",
  "description": "Sužinokite, kas yra XHTML failo formatas ir API, kurios gali kurti ir atidaryti XHTML failus.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra XHTML failas?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Šie failai puikiai tinka atidaryti arba peržiūrėti žiniatinklio naršyklėje. XHTML buvo sukurtas taip, kad būtų labiau struktūrizuotas, mažiau scenarijų, bendras; naudojant visas esamas XML priemones ir daugiau nepriklausomų nuo įrenginių. XHTML suteikia paprastai vertingą elementų ir atributų rinkinį su plėtinio parinktimis kartu su stiliaus lapais. Atributai naudojami iš metaduomenų atributų rinkinio. XHTML suteikia lankstumo ir pasiekiamumo, pajungdamas visus **[HTML](/web/html/)** pateikties elementus stiliaus lapams. Stiliaus lapai yra universalesni nei šie pristatymo elementai. HTML 4.01, HTML5 ir XHTML specifikacijas dinamiškai kuria World Wide Web Consortium (W3C).

## Trumpa XHTML failo formato istorija

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. Tačiau 2005 m. buvo sudaryta darbo grupė (WHATWG), kurios tikslas buvo tobulinti įprastą HTML, nepriklausantį nuo XHTML. Galiausiai WHATWG pradėjo dirbti su HTML5 lygiagrečiai su XHTML 2.

## XHTML failo formatas

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. XHTML failai yra pagrįsti XML ir skirti dirbti su vartotojo agentais, pagrįstais XML. XHTML failai atitinka XML. Standartiniai XML įrankiai naudojami peržiūrėti, redaguoti ir patvirtinti XHTML failus. HTML dokumento objekto modelis arba XML dokumento objekto modelis [DOM] priklausomos programos gali veikti per XHTML dokumentus. Šiandien pasirinkę XHTML, turinio kūrėjai gali mėgautis visais susijusiais XML privalumais nesijaudindami dėl savo turinio suderinamumo pirmyn ar atgal.

Susijusių elementų rinkinys sukuria modulį XHTML. Formos arba lentelės modulyje gali būti įvairių formų ar lentelės elementų, kurie gali būti rodomi tinklalapyje. Modularizacija buvo skirta išskirti HTML elementus į daugybę susietų elementų rinkinius. Kad turinio kūrėjai galėtų pasinaudoti modulių pasirinkimu įvairių tipų įrenginiams. Be to, moduliai leidžia vartotojų agentams pasirinkti elementus neprarandant suderinamumo su XHTML standartu. XHTML analizės reikalavimai yra tokie patys kaip XML, o HTML praktikuoja savo.

### Dokumento atitiktis

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Dokumentų atitiktis yra dviejų tipų.

Griežtai atitinkantis dokumentas yra pagrįstas XML, kuriam reikalingos tik privalomos paslaugos, apibrėžtos šioje specifikacijoje. XHTML failai turi atitikti šiuos kriterijus:

* Failas turi atitikti apribojimus, apibrėžtus DTD ir B priede.

* Pagrindinis failo elementas turi būti html.

* Pagrindiniame failo elemente turi būti XHTML vardų erdvės deklaracija ir jis turi būti apibrėžtas kaip:


```
http://www.w3.org/1999/xhtml.
```

* Pagrindinis elementas gali būti parašytas taip:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Anksčiau nei pagrindinis elementas turi būti deklaruotas DOCTYPE, kurio viešasis identifikatorius turi nurodyti vieną iš trijų dokumento tipo apibrėžimų (DTD). Sistemos identifikatorius gali būti pakeistas, kad atitiktų esamas sistemos taisykles.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML dokumentuose nebūtina nurodyti XML deklaracijų visuose dokumentuose; tačiau turinio kūrėjai yra viliojami naudoti XML deklaracijas visuose savo XHTML dokumentuose. Šios deklaracijos yra privalomos, kai dokumento simbolių kodavimas skiriasi nuo UTF-8 /16 arba kai kodavimas nenurodytas vadovaujančiame protokole. Šis XHTML dokumento pavyzdys apibrėžia XML deklaracijas

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Atitinkantis vartotojo agentas turi atitikti šias taisykles:

* XHTML dokumento analizę ir įvertinimą atlieka vartotojo agentas, užtikrinantis jo suderinamumą su XML 1.0 rekomendacija.

* Patvirtinant vartotojo agentą, jis turi patikrinti dokumentų galiojimą jų nurodytiems DTD pagal XML. Kai vartotojo agentas XHTML failą apdoroja kaip bendrąjį XML, ID tipo ypatybės bus pripažintos kaip fragmento identifikatoriai.


Jei vartotojo agentas atsitrenkia į neatpažintą elementą, šie privalomi kriterijai, kuriuos ji turi įvykdyti

* apdoroti to nežinomo elemento turinį

* ignoruoti atributą ir jo reikšmę

* Naudokite numatytąją atributo reikšmę.


Kai vartotojo agentas aptinka objekto nuorodos deklaraciją, kuri nebuvo apdorota anksčiau, ji turėtų būti apdorojama kaip simboliai (pradedant & ženklu ir baigiant kabliataškiu). Apdorojant turinį, simboliai arba simbolių objektų nuorodos, kurias nuspėja vartotojo agentas, bet kurių negalima pateikti, gali naudoti bet kokį alternatyvų atvaizdavimą, kuris suteikia panašią reikšmę. Tokiu atveju dokumentas turi būti rodomas taip, kad vartotojas matytų, jog atvaizdavimo procesas nebuvo įprastas. Norėdami apdoroti tarpą, vartotojo agentas turi ieškoti apibrėžimo iš CSS simbolių [CSS2].

## XHTML atgalinis suderinamumas

The back ward compatibility of XHTML 1.  dokumentai gerai išmano HTML 4 vartotojų agentus, jei laikomasi tinkamų taisyklių. XHTML 1.1 yra visiškai suderinamas, išskyrus rubino komentarus, net jei HTML 4 naršyklės jų paprastai nepaiso. XHTML 2.0 yra palyginti mažiau suderinamas, tačiau problema buvo išspręsta tam tikru mastu naudojant scenarijus.

## Nuorodos

* [XHTML istorija: nuo 1990-ųjų iki šiandien](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


