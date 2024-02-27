{
  "date": "2020-03-16",
  "keywords": [
"IFC fil",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om IFC-filformat og API'er, der kan oprette og åbne IFC-filer.",
  "title": "IFC filformat",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-dac"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en IFC fil?

Filer med IFC-udvidelse henviser til filformatet Industry Foundation Classes (IFC), der etablerer internationale standarder for import og eksport af bygningsobjekter og deres egenskaber. Dette filformat giver interoperabilitet mellem forskellige softwareapplikationer. Specifikationer for dette filformat er udviklet og vedligeholdt af buildingSMART International som dets datastandard. Det ultimative mål med IFC-filformat er at forbedre kommunikation, produktivitet, leveringstid og kvalitet gennem hele en bygnings livscyklus.

På grund af de etablerede standarder for almindelige objekter i byggebranchen, reducerer det tabet af information under overførsel fra en applikation til en anden. IFC kan opbevare data for geometri, beregning, mængder, facility management, prissætning etc. for mange forskellige erhverv (arkitekt, el, HVAC, konstruktion, terræn etc.).

## Kort historie ##

IFC-initiativet blev taget i 1994 af Autodesk for at understøtte integreret applikationsudvikling og inkluderede virksomheder som Honeywell, Butler Manufacturing og AT&T. I 1995 blev medlemskabet åbnet for åbent for alle, og navnet blev ændret til International Alliance for Interoperability. Nonprofitens hensigt var at udgive Industry Foundation Class (IFC) som en AEC-produktmodel. I 2005 blev navnet igen ændret, og buildSMART bevarer det nu.

## IFC-filformat ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Der skete fra tid til anden adskillige mindre ændringer, ligesom det er blevet gjort til en del af specifikationerne som tillæg. Følgende er en liste over forskellige versioner af filspecifikationer, der er blevet offentliggjort i fortiden.

* IFC4 Tilføj2 (2016)IFC4 Tilføj1 (2015)

* IFC4 (marts 2013) ifcXML2x3 (juni 2007)

* IFC2x3 (februar 2006) ifcXML2 for IFC2x2 add1 (RC2)

* IFC2x2-tillæg 1 (juli 2004)ifcXML2 for IFC2x2 (RC1)

* IFC 2x2IFC 2x Tillæg 1ifcXML1 til IFC2x og

* IFC2x-tillæg 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


De seneste versioner af IFC-filformatspecifikationer er altid tilgængelige på buildingSMART-webstedet, og udviklere bør konsultere disse for enhver type applikationer, de planlægger at udvikle. Når denne artikel skrives, er version 4-specifikationerne de seneste tilgængelige online.

### IFC-datafilformater ###

IFF-filformat understøtter dataudveksling mellem applikationer, der bruger forskellige formater som angivet nedenfor:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Dette filformat har filtypenavnet .ifc og er det mest brugte IFC-format.

**IFC-XML:** Det er en XML-filformatversion af IFC, der kan genereres direkte af den afsendende applikation i henhold til ISO 10303-28-strukturen, også kaldet STEP-XML. IFC-XML-filformatet anses for at være egnet til interoperabilitet mellem XML-værktøjer. Sammenlignet med IFC-filformatet er IFC-XML 300-400 % større i størrelse.

**IFC-ZIP:** Det er en [ZIP](/compression/zip/) komprimeret version af IFC eller IFC-XML, hvor den ene af disse filer er hovedbiblioteket i zip-arkivet. Dette format komprimerer en .ifc ned med 60-80 % og en .ifc XML-fil med 90-95 %.

### IFC-arkitektur ###

IFC-specifikationen omfatter termer, koncepter og dataspecifikationselementer, der stammer fra brug inden for discipliner, fag og erhverv i bygge- og facility management-industrien. Termer og begreber bruger de almindelige engelske ord, dataelementerne i dataspecifikationen følger en navnekonvention.

dataelementnavnene for typer, entiteter, regler og funktioner starter med præfikset Ifc og fortsætter med de engelske ord i CamelCase-navnekonventionen (ingen understregning, første bogstav i ord med store bogstaver); attributnavnene i en enhed følger CamelCase-navnekonventionen uden præfiks; egenskabssætdefinitionerne, der er en del af denne standard, starter med præfikset Pset_ og fortsætter med de engelske ord i CamelCase-navnekonventionen; mængdesættets definitioner, der er en del af denne standard, starter med præfikset Qto_ og fortsætter med de engelske ord i CamelCase-navnekonventionen.

Dataskemaarkitekturen i IFC definerer fire konceptuelle lag, hvert enkelt skema er tildelt nøjagtigt ét konceptuelt lag.

**Ressourcelag** — det nederste lag inkluderer alle individuelle skemaer, der indeholder ressourcedefinitioner, disse definitioner inkluderer ikke en globalt unik identifikator og skal ikke bruges uafhængigt af en definition, der er erklæret på et højere lag;

**Kernelag** — det næste lag inkluderer kerneskemaet og kerneudvidelsesskemaerne, der indeholder de mest generelle enhedsdefinitioner, alle entiteter defineret på kernelaget eller derover bærer et globalt unikt id og eventuelt ejer- og historieinformation;

**Interoperabilitetslag** — det næste lag inkluderer skemaer, der indeholder enhedsdefinitioner, der er specifikke for en generel produkt-, proces- eller ressourcespecialisering, der bruges på tværs af flere discipliner, disse definitioner bruges typisk til udveksling mellem domæner og deling af konstruktionsinformation;

**Domænelag** — det højeste lag inkluderer skemaer, der indeholder enhedsdefinitioner, der er specialiseringer af produkter, processer eller ressourcer, der er specifikke for en bestemt disciplin, disse definitioner bruges typisk til udveksling inden for domænet og deling af information.

## Referencer ##

* [Industry Foundation Classes - Af Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


