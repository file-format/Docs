{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Computer grafik metafil",
"Fil",
"Udvidelse",
"Filformat",
"Vektorgrafik",
"Metafil Descriptor"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CGM filformat",
  "description": "Lær om CGM-filformat og API'er, der kan oprette og åbne CGM-filer.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-dam"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er en CGM fil? ##

Computer Graphics Metafile (CGM) er et gratis, platformsuafhængigt internationalt standard metafilformat til lagring og udveksling af vektorgrafik (2D), rastergrafik og tekst. CGM bruger en objektorienteret tilgang og mange funktionsbestemmelser til billedproduktion. CGM bruger disse objektorienterede egenskaber til at omforme grafiske elementer for at gengive et billede. En metafil indeholder nødvendige oplysninger, der definerer andre filer. I CGM indeholder en tekstbaseret kildefil alle grafiske elementer, som senere kan kompileres til en binær fil. Grundlæggende er CGM en måde at lette 2D grafisk dataudveksling, uafhængigt af en bestemt platform eller enhed.

CGM-formatet giver forskellige elementer til at udføre funktioner og betegne objekter for at justere geometriske primitiver og grafisk information. Selvom CGM er blevet afløst af andre formater til at vise grafisk kunst på websider, da det ikke er godt understøttet af websider, er det stadig meget populært blandt industrielle, aeronautiske og andre tekniske applikationer. Selvom World Wide Web Consortium har udviklet WebCGM, en alternativ tilgang til brugen af CGM på nettet. Den primære CGM-implementering var en illustration af rækkefølgen af grundlæggende operationer i det grafiske kernesystem (GKS). Det er ikke blevet brugt meget i professionelle designs, men er stort set erstattet af andre formater såsom DXF og SVG.

## Historie ##

CGM viste sig at være en international standard i 1987 (ISO 8632-1987) og blev også vedtaget som en national standard i Storbritannien af BSI og USA af ANSI. Efter en række ændringer i 1991 blev en revideret standard for CGM udgivet i 1992 (ISO 8632:1992). I 2001 udviklede World Wide Web Consortium WebCGM med forbedret kapacitet til brug med websiderne. I 2007 blev den anden version af WebCGM udgivet, og den tredje version blev udgivet i 2010 med forbedrede muligheder.

## CGM-filformat ##

Computergrafik-metafiler er grundlæggende en database til grafisk information og giver midlerne til indfangning, lagring og transmission af grafiske data. Derfor skal der være en grafisk systemkomponent til at oprette databasen samtidig med afviklingen af en applikation i et metafilformat. I de fleste tilfælde er denne komponent Metafile-generatoren. Sideløbende er der behov for en anden komponent, der kan hente, fortolke og gengive grafiske data i en metafil. Dette behov opfyldes ved tilstedeværelsen af en metafiltolk. Følgende figur repræsenterer det grafiske metafil-arbejdsmiljø.

Forholdet mellem CGM og andre komponenter i et typisk grafiksystem er illustreret i ovenstående figur. Det fremgår også tydeligt af figuren, at metafilens funktionalitet ikke er afhængig af den endelige enhedsoutput.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Metafil deskriptor
1. En pulje af logisk uafhængige billeder

Hvert billede er en samling af billedbeskrivelser og en billedtekst inklusive en billeddefinition. metafil-deskriptor definerer beskrivende information, der gælder for alle billeder af den metafil. Denne information hjælper tolken med at parse en metafil korrekt og genkende de ressourcer, der er nødvendige for den korrekte gengivelse af et billede. Selvom billedbeskrivelsen også omslutter den beskrivende information, kan den kun genkende det billede, hvori beskrivelsen findes. I dette filformat er hver billeddefinition selvstændig og logisk suveræn. De er uafhængige af alle andre billeddefinitioner i en fil. Lige efter fortolkningen af meta-deskriptoren kan billeder tilgås og fortolkes tilfældigt. Ændring i tilstanden af tidligere billeder har ingen effekt på deres efterfølgere. Denne billeduafhængighed er et andet fremtrædende træk ved CGM.CGM består af koordinatrum, som er 2D kartesiske koordinater kaldet virtuelle enhedskoordinater og kan repræsenteres gennem tal eller præcision, der repræsenterer rækkevidden og granulariteten. CGM angiver både det direkte valg af farver og indeksbaseret valg. I førstnævnte består farvespecifikationen af en RGB-tredobbelt, mens farvespecifikationen senere angiver et indeks i en farvetabel.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
