{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX-bestandsindeling",
  "description":"Meer informatie over TEX-bestandsindelingen en API's die TEX-bestanden kunnen maken en openen.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een TEX-bestand? ##

**TeX** is een taal die zowel programmeer- als opmaakfuncties omvat, die worden gebruikt om documenten te zetten. Donald Knuth van Stanford University is de maker van dit vindingrijke zetsysteem. Over de hele wereld is TeX de ultieme keuze van auteurs en uitgevers om technische documenten van hoge kwaliteit te produceren. TeX levert uitstekend werk bij het formatteren van complexe wiskundige uitdrukkingen. In combinatie met een hoogwaardige fotozetmachine concurreert TeX met de resultaten die worden gegenereerd door de beste traditionele zetsystemen. Daarom beschouwd als de meest stijlvolle digitale typografische systemen.

TeX-invoerbestanden zijn gebaseerd op ASCII-code, waardoor het delen van manuscripten tussen schrijvers, uitgeversmanagers en critici mogelijk wordt gemaakt. Een grote verscheidenheid aan computeromgevingen, bijna elk modern platform en veel oudere platforms ondersteunen TeX. Bovendien is TeX gratis software, beschikbaar voor een breed scala aan consumenten. Veel UNIX-installaties gebruiken zowel UNIX troff als TeX als formatteringssysteem voor verschillende doeleinden. Andere zettaken worden enorm uitgevoerd in de vorm van LaTeX, ConTeXt en andere macropakketten.

## Korte geschiedenis ##

TeX is ontworpen en geschreven door Donald Knuth in 1978. Guy Steele van het Massachusetts Institute of Technology heeft de invoer/uitvoer van TeX herzien om het onder het incompatibele besturingssysteem zoals Timesharing System (ITS) te laten draaien. De eerste versie van TeX is ontwikkeld onder Stanford's WAITS-besturingssysteem in de programmeertaal (SAIL) en getest om te draaien op een PDP-10. Knuth introduceerde het idee van geletterd programmeren voor geavanceerde versies. Geletterd programmeren is een manier om compileerbare broncode en typeset (in TeX) te genereren voor gecrosslinkte documentatie met behulp van het originele bestand. De taal die wordt gebruikt om deze geavanceerde versies van TeX te ontwikkelen, wordt WEB genoemd, een mix van DEC PDP-10 Pascal-programma's om draagbaarheid te garanderen.

Een herziene nieuwe versie van TeX gepubliceerd in 1982 en heette TeX82. De belangrijkste verandering is de vervanging van het oorspronkelijke afbreekalgoritme door het nieuw geschreven algoritme van Frank Liang. Om overdraagbaarheid over verschillende platforms te garanderen, gebruikt TeX82 in plaats van drijvende komma rekenkunde met vaste komma samen met een echte, turing-complete programmeertaal. In 1989 werd een nieuwe versie van TeX en Metafont uitgebracht. Dus de versie 3.0 van TeX faciliteert 8-bit invoer, waardoor 256 verschillende karakters in de tekst mogelijk zijn. Na versie 3 worden updates aangegeven door een extra cijfer toe te voegen aan het einde van het decimaalteken, bijvoorbeeld de huidige versie van TeX wordt aangegeven als 3.14159265. Deze versie is voor het laatst bijgewerkt op 01-12-2014.

## TeX-invoer ##

Een invoerbestand naar TEX kan worden gemaakt met een teksteditor die gewone tekst gebruikt. In tegenstelling tot een typische tekstverwerker, staat dit invoerbestand geen onzichtbare controletekens toe. Het ene bestand kan worden ingesloten in een ander bestand, dat macrodefinities en hulpdefinities bevat die de mogelijkheden van TeX vergroten. Als een TeX-installatie wordt geleverd met macrobestanden, toont de lokale informatie over TeX het gebruik van macrobestanden. De standaardvorm van TeX integreert een combinatie van macro's en andere definities die bekend staan als gewone TEX.

Op basis van nauwkeurige kennis van de grootte van alle tekens en symbolen berekent het de optimale indeling van letters per regel en regels per pagina. Op het moment van documentverwerking wordt een .dvi-bestand aangemaakt, waarbij “dvi” staat voor “apparaatonafhankelijk”. Stuurprogramma's voor apparaten zijn vereist voor het afdrukken of bekijken van het document met een dvi-extensie. Tegenwoordig wordt dvi-generatie omzeild door een veelgebruikte pdf-TeX. Er is geen voorkennis van lettertypen beschikbaar binnen de TeX-installatie, dus externe lettertypebestanden, die deel uitmaken van de lokale TeX-omgeving, worden gebruikt om informatie voor het document te verkrijgen.

## Zetsysteem ##

Ongeveer 300 primitieven (commando's) kunnen worden begrepen door het basis TeX-systeem. Primitieven zijn commando's op een laag niveau, daarom gebruikte een gewone gebruiker ze zelden rechtstreeks en de meeste functionaliteit wordt uitgevoerd door bestanden te formatteren. Deze bestandsindelingen zijn vooraf geladen geheugenafbeeldingen van TeX die worden gevolgd door het laden van grote macrocollecties. Het oorspronkelijke standaardformaat van de taal, dwz gewone TeX, voegt ongeveer 600 commando's toe.

Een backslash gegroepeerd met accolades geeft het starten van TeX-commando's aan. Aangezien TeX een op macro's en tokens gebaseerde taal is, kunnen bijna alle syntactische kenmerken van TeX tijdens runtime worden gewijzigd, inclusief door de gebruiker gedefinieerde, behalve niet-uitbreidbare tokens die vervolgens worden uitgevoerd. Uitbreiding zelf is praktisch probleemloos. Sommige commando's moeten komen na een argument dat helpt om de functie van een commando uit te leggen. Het \vskip-commando geeft TEX bijvoorbeeld de opdracht om de pagina omlaag/omhoog te slaan, gevolgd door een argument dat bepaalt hoeveel ruimte moet worden overgeslagen.

## Versies ##

LaTeX is het meest gebruikte formaat dat oorspronkelijk is ontwikkeld door Leslie Lamport. LaTeX integreert verschillende documentstijlen voor bestanden, brieven, boeken en dia's en biedt verwijzingen en automatische nummering voor verschillende secties en wiskundige uitdrukkingen. AMS-TeX is een ander populair formaat, ontwikkeld door de American Mathematical Society.

AMS-TeX biedt veel meer gebruiksvriendelijke commando's, die door tijdschriften opnieuw kunnen worden gedefinieerd om te passen bij hun lokale stijl. LaTeX kan profiteren van de voordelen van AMS-TeX door gebruik te maken van de AMS-"pakketten", die dan AMS-LaTeX worden genoemd. ConTeXt is een ander formaat geschreven door Hans Hagen dat voornamelijk wordt gebruikt voor desktop publishing.

De TeX-software biedt verschillende functies die op het moment van ontstaan niet beschikbaar waren of van lagere kwaliteit waren in andere zetsystemen. Sommige van de innovatieve kenmerken van deze taal zijn gebaseerd op interessante algoritmen die zijn afgeleid van de stellingen van Knuths studenten. Terwijl andere zetprogramma's nu handige functies van TeX in hun programma's opnemen.

## Referenties ##

* [TeX-zetsysteem](https://en.wikipedia.org/wiki/TeX)

