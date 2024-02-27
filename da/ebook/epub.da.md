{
  "date": "2019-12-12",
  "keywords": [
"EPUB",
"fil",
"udvidelse",
"format",
"E-bog",
"Digital bog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om EPUB-filformat og API'er, der kan oprette og åbne EPUB-filer.",
  "title": "Hvad er en EPUB fil?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epu-dab"
}
},
  "lastmod": "2019-12-12"
}

## Hvad er en EPUB fil?

Filer med filtypenavnet .epub er et e-bogs filformat, der giver et standard digitalt udgivelsesformat til udgivere og forbrugere. Formatet har efterhånden været så almindeligt, at det understøttes af mange e-læsere og softwareapplikationer. På Mac OS understøtter den forudinstallerede **Books**-software f.eks. åbning af sådanne filer. Derudover er der en masse kompatibel software tilgængelig til smartphones, tablets og computere. EPUB-filstandarder vedligeholdes af [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Versionen EPUB 3 er også godkendt af Book Industry Study Group (BISG), en førende boghandelsforening for standardiseret bedste praksis, forskning, information og begivenheder, for emballering af indhold.

## Kort historie om EPUB-filformat

* **oktober 2007** - EPUB 2.0 blev godkendt

* **September 2010** - Vedligeholdelsesopdatering blev udgivet

* **oktober 2011** - EPUB 3.0-specifikationerne trådte i kraft

* **Juni 2014** - Mindre vedligeholdelsesopdatering blev udgivet for at erstatte 3.0-versionen

* **januar 2017** - EPUB 3.1 trådte i kraft


## EPUB filformat

EPUB-filformatet er et arkiv, der kan omdøbes til [ZIP](/compression/zip/)-udvidelsen, og dets indhold kan ses ved at udpakke arkivet med en hvilken som helst arkivudtrækker. Det er et åbent XML-baseret format og består af HTML-filer, billeder, CSS-typografiark og andre elementer. Den kan også konverteres til PDF, Mobi og flere andre filformater gennem en række softwareapplikationer og API'er.

{{< figure src="../epub.png" alt="EPUB filformat" >}}

**EPUB E-bog åbnet med Mac OS Books Application**

EPUB-filformatet er baseret på følgende tre åbne standarder.

### Open Public Structure (OPS) ###

En EPUB 2.0-fil bruger XHTML 1.1 til at konstruere indholdet af en publikation. I bund og grund betyder dette, at en EPUB-fil består af en eller flere websider. Selvom du kunne inkludere hele indholdet af en bog eller avis på en enkelt side, er det bedre, at en sådan fil ikke overstiger 300K, både af ydeevne- og kompatibilitetsårsager. Ligesom med almindelige websider, er stylingen og layoutet defineret ved hjælp af cascading style sheets (CSS). I EPUB-filer skal et undersæt (begrænset række af kommandoer) af CSS2 bruges. Mange af de nye funktioner i CSS3, såsom afrundede kasser eller skygger, er ikke tilgængelige endnu. For bagudkompatibilitet kan en skaber også bruge DTBook i stedet for XHTML til at kode indholdet.

### Open Packaging Format (OPF) ###

Denne del af specifikationerne omhandler strukturel information såsom metadata (hvem er forfatteren og udgiveren, hvad er titlen, ..), manifestet (en liste over alle filerne i en epub-fil) og indholdsfortegnelsen. Disse data er alle indlejret ved hjælp af XML.

### Open Container Format (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Understøttede billedfilformater ##

EPUB-filformatet understøtter følgende billedfilformater.

* [GIF](/image/gif/)

* [JPG](/image/jpeg/)

* [PNG](/image/png/)

* [SVG](/page-description-language/svg/)

## Referencer ##

* [EPUB - af Wikipedia](https://en.wikipedia.org/wiki/EPUB)


