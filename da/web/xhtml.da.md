{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"udvidelsesbar html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML - Extensible Hypertext Markup Language File Format",
  "description": "Lær om, hvad der er XHTML-filformat og API'er, der kan oprette og åbne XHTML-filer.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en XHTML fil?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Disse filer er velegnede til at blive åbnet eller vist i en webbrowser. XHTML blev designet til at være mere struktureret, mindre scripting, generisk; ved at bruge alle de eksisterende faciliteter i XML og mere enhedsuafhængig. XHTML giver et generelt værdifuldt sæt af elementer og attributter, med udvidelsesmuligheder i kombination med typografiark. Attributterne bruges fra samlingen af metadataattributter. XHTML giver fleksibilitet og tilgængelighed ved at underordne alle **[HTML](/web/html/)** præsentationselementer til typografiark. Style sheets er mere alsidige end disse præsentationselementer. Specifikationer for HTML 4.01, HTML5 og XHTML udvikles dynamisk af World Wide Web Consortium (W3C).

## Kort historie om XHTML-filformat

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. Men i 2005 blev der dannet en arbejdsgruppe (WHATWG), som havde til formål at forbedre almindelig HTML uafhængig af XHTML. WHATWG begyndte til sidst at arbejde på HTML5 parallelt med XHTML 2.

## XHTML filformat

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. Filerne i XHTML er XML-baserede og har til formål at arbejde med brugeragenterne baseret på XML. XHTML-filer er XML-konforme. Standard XML-værktøjer bruges til at se, redigere og validere XHTML-filer. HTML Document Object Model eller XML Document Object Model [DOM] afhængige applikationer kan fungere gennem XHTML dokumenter. Ved at vælge XHTML i dag kan indholdsudviklere nyde alle de tilknyttede fordele ved XML uden at bekymre sig om deres indholds frem- eller bagudkompatibilitet.

Et sæt relaterede elementer bygger et modul i XHTML. Et formular- eller tabelmodul kan indeholde forskellige formular- eller tabelelementer, der kan vises på en webside. Modulariseringen havde til formål at isolere HTML-elementer i sæt af talrige sammenkædede elementer. Så indholdsudviklere kan drage fordel af modulvalg til forskellige typer enheder. Desuden giver moduler brugeragenter mulighed for at vælge elementer uden at miste overensstemmelse med XHTML-standarden. Parsing krav til XHTML er det samme som XML, mens HTML praktiserer sit eget.

### Dokumentoverensstemmelse

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Dokumentoverensstemmelse er af to typer.

Et strengt overensstemmende dokument er XML-baseret, der kun kræver obligatoriske tjenester defineret i denne specifikation. Følgende kriterier skal være opfyldt for XHTML-filer:

* En fil skal overholde de begrænsninger, der er defineret i DTD'er og i appendiks B.

* Grundelementet i filen skal være html.

* Filens basiselement skal indeholde en erklæring for XHTML-navneområdet og skal defineres som:


```
http://www.w3.org/1999/xhtml.
```

* Basiselementet kan skrives som:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Tidligere end basiselementet skal der deklareres en DOCTYPE, hvis offentlige identifikator skal referere til en af de tre dokumenttypedefinitioner (DTD'er). Systemidentifikationen kan ændres for at overholde de nuværende systemkonventioner.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

I XML-dokumenter er det unødvendigt at angive XML-deklarationer i alle dokumenter; dog lokkes indholdsudviklere til at bruge XML-deklarationer i alle deres XHTML-dokumenter. Disse erklæringer er obligatoriske, enten når dokumentets tegnkodning er forskellig fra UTF-8 /16, eller der ikke er angivet nogen kodning af en styrende protokol. Følgende eksempel på et XHTML-dokument definerer XML-deklarationerne

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

En konform brugeragent skal opfylde følgende regler:

* Parsing og evaluering af XHTML-dokument udføres af en brugeragent, der sikrer dets overensstemmelse med XML 1.0-anbefalingen.

* I tilfælde af validerende brugeragent skal den kontrollere dokumenternes gyldighed for deres refererede DTD'er i henhold til XML. Når XHTML-fil behandles af brugeragenten som generisk XML, vil funktionerne i type-id'et blive anerkendt som fragmentidentifikatorer.


Hvis en brugeragent støder ind i et ikke-genkendt element, er følgende de obligatoriske kriterier, den skal opfylde

* behandle indholdet af det ukendte element

* ignorer attributten og dens værdi

* Brug værdien af den angivne attribut som standard.


Når en brugeragent støder på en enhedsreferenceerklæring, der ikke er blevet behandlet tidligere, skal den behandles som tegnene (startende med &-tegnet og slutter med semikolon). Under indholdsbehandling kan karakterer eller karakterenhedsreferencer, der er forudsigelige af brugeragenten, men som ikke kan gengives, bruge enhver alternativ gengivelse, der giver den samme betydning. I så fald skal dokumentet vises på en måde, der gør brugeren indlysende om, at gengivelsesprocessen ikke har været normal. For at behandle blanktegn skal brugeragenten se definition fra CSS-tegn [CSS2].

## XHTML bagudkompatibilitet

The back ward compatibility of XHTML 1.  dokumenter er velbevandret med HTML 4-brugeragenter, hvis de rette regler følges. XHTML 1.1 er fuldt ud kompatibel med undtagelse af rubin-annoteringer, selvom de generelt ignoreres af HTML 4-browsere. XHTML 2.0 er forholdsvis mindre kompatibel, ikke desto mindre er problemet til en vis grad blevet løst gennem brug af scripting.

## Referencer

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


