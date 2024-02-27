{
  "date": "2020-03-02",
  "keywords": [
"SVG",
"fil",
"filformat",
"Side Beskrivelse Sprog",
"Skalar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om SVG-filformat og API'er, der kan oprette og åbne SVG-filer.",
  "title": "Hvad er en SVG fil?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sv-dag"
}
},
  "lastmod": "2020-03-02"
}

## Hvad er en SVG fil? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Kort historie ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Før dette blev lignende filformatspecifikationer i seks forskellige formater indsendt til W3C indtil 1998. En opdatering blev anvendt til specifikationerne i 2011, og den blev version 1.1. I 2016 blev SVG 2 udgivet som nyere version inklusive funktioner ud over dem i SVG 1.1.

## Filformatspecifikationer ##

SVG Document Object Model (DOM) lægger grundlaget for alle de specifikationer og grænseflader, der svarer til de særlige sektioner af specifikationerne. SVG-seere skal implementere SVG DOM-grænseflader som defineret i W3C-specifikationerne. Dens DOM afslører flere grænseflader for forskellige datatyper og elementer.

### SVG-former ###

SVG har nogle foruddefinerede formelementer, som kan bruges af udviklere:

* Rektangel<rect>

* Cirkel<circle>

* Ellipse<ellipse>

* Linje<line>

* Polyline<polyline>

* Polygon<polygon>

* Sti<path>


Baseret på disse former og specifikationer er de funktionelle områder af SVG som følger.

**Stier** - Stier bruges til at repræsentere simple såvel som sammensatte formkonturer. Kodninger bruges til at definere arten af operationen. For eksempel bruges M til Flyt til, L bruges til Linje til, Z bruges til at lukke en sti og så videre.

**Grundlæggende former** - Lige liniebaner og stier, der består af en række forbundne ligelinjede segmenter (polylinjer), samt lukkede polygoner, cirkler og ellipser kan tegnes. Rektangler og rektangler med runde hjørner er også standardelementer.

**Tekst** - Tekstrepræsentation er udtrykt som XML-tegndata, hvor mange visuelle effekter kan anvendes på teksten. Specifikationerne gør det muligt at håndtere tovejstekst, lodret tekst og tegn langs en buet sti.

**Maleri** - Former kan udfyldes og/eller omridses med en farve, en gradient eller et mønster, hvilket giver mulighed for at gøre det uigennemsigtigt eller have nogen grad af gennemsigtighed. Linjeendens funktioner, såsom pilespidser eller symboler, der vises ved hjørnerne af en polygon, er repræsenteret af markører.

**Farve** - SVG-specifikationer gør det muligt at anvende farver på alle synlige SVG-elementer, enten direkte eller via fyld, streg og andre egenskaber. Forskellige farvekoder kan bruges til at specificere som sort eller blå, hex-repræsentation, decimal eller som procenter af formen RGB.

**Gradienter og mønstre** - Former i en SVG-fil kan udfyldes eller omrids med solide farver, gradienter eller gentagne mønstre.

**Filtereffekter** - Det er faktisk en række grafikoperationer, der anvendes på givet kildevektorgrafik for at producere modificeret resultat.

**Interaktivitet** - Brugere kan interagere med SVG-filer ved at ændre fokus, museklik, rulle eller zoome på billedet. Interaktiviteten lader SVG-billeder interagere med brugere på mange forskellige måder som førnævnt.

**Linking** - Det er muligt for SVG-billeder at have hyperlinks til andre dokumenter. Dette opnås via XML Linking Language eller XLink. Dette giver mulighed for at oprette specifikke visningstilstande, der bruges til at zoome ind/ud af et specifikt område eller til at begrænse visningen til et bestemt element.

**Scripting** - I lighed med HTML er alle aspekter af et SVG-dokument tilgængelige for manipulation ved hjælp af scripts. SVG DOM-objekterne giver vejledningen til at opnå dette ved hjælp af SVG-element og -attribut. Scripts er indesluttet i script-tagelementer og kan køre som svar på markør-, tastatur- eller dokumenthændelser efter behov.

**Animation** - DOM-elementerne<animate> ,<animateMotion> og<animateColor> lader dig inkludere animation til SVG-indhold. Dette er selvfølgelig ikke muligt uden brug af scripts og indbyggede timere. Disse animationer kan være kontinuerlige og kan sættes på loop såvel som gentagelser, mens de samtidig reagerer på brugerhændelser.

**Skrifttyper** - Tekst i SVG kan referere til eksterne skrifttypefiler såsom systemskrifttyper. I mangel af sådanne skrifttyper vil tekst i SVG ikke blive gengivet til outputtet. Dette kan overvindes ved at inkorporere de nødvendige glyffer i en sådan fil som en skrifttype, der derefter gengives ved hjælp af<text> element.

## Eksempler ##
De følgende linjer viser, hvordan en cirkel er repræsenteret ved hjælp af SVG-scriptet.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

De følgende linjer med kode viser, hvordan du bruger<text> blok til gengivelse af tekst til SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referencer ##

* [W3C SVG-specifikationer](https://www.w3.org/TR/SVG2/Overview.html)

* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


