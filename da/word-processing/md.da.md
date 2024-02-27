{
  "date": "2019-10-11",
  "keywords": [
"md fil",
"md filformat",
"hvad er en md-fil",
"fil",
"md eksempel",
"md filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD - MarkDown Language File",
  "description": "Lær om MD-filformat og API'er, der kan oprette og åbne MD-filer.",
  "linktitle": "MD",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-m-dad"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en MD fil?

Tekstfiler oprettet med Markdown-sprogdialekter gemmes med filtypenavnet **.md** eller **.MARKDOWN**. MD-filer gemmes i almindeligt tekstformat, der bruger Markdown-sprog, som også inkluderer inline-tekstsymboler, der definerer, hvordan en tekst kan formateres, såsom indrykning, tabelformatering, skrifttyper og overskrifter. MD-filer kan konverteres til HTML med et program kaldet Markdown. Markdown-sprog er udgivet af John Gruber.

MD-filer kan også kategoriseres som udviklerfiler, som for det meste bruges af Markdown, til at konvertere tekstfiler til HTML-versioner, så brugerne kan oprette filer, der er nemme at læse og skrive. Følgende er de programmer, der kan åbne en .md-fil:

* Microsoft Notesblok

* Notesblok 2

* Apple TextEdit

* Microsoft WordPad


En advarsel er, at du ikke omdøber udvidelsen af .md-filer. Hvis det er tilfældet, vil dette ikke ændre filtypen, fordi der findes specielle konverteringssoftware til at ændre en fil fra en type til en anden. Som diskuteret ovenfor er .MD-filer udvidelser af filer, der er oprettet Markdown-sprogsoftware. **Markdown** er en [lightweight markup language](https://en.wikipedia.org/wiki/Lightweight_markup_language) beregnet til ét formål, der skal bruges til at formatere tekst på nettet med almindelig tekstformateringssyntaks. Lad det være klart, at Markdown ikke er en erstatning for HTML, fordi dens syntaks er meget lille og indeholder en meget lille delmængde af HTML-tags. Årsagen bag Markdown er at gøre det nemt at læse, skrive og redigere prosa. Med andre ord kan vi sige, at HTML er et udgivelsesformat, mens Markdown er et skriveformat.

Markdown er nu et af verdens mest populære markup-sprog. Mens du bruger Microsoft Word, formateres ord og sætninger ved at klikke på knapper, og ændringer er umiddelbart synlige. Men Markdown er ikke sådan. Når Markdown-formateret fil oprettes, tilføjes Markdown-syntaks til teksten for at angive, hvilke ord og sætninger der kan se anderledes ud. For at vise en overskrift tilføjes f.eks. et taltegn før den (f.eks. # Overskrift 1). For at lave en fed sætning tilføjes to stjerner før og efter den (f.eks. **denne tekst er fed**). Markdown-syntaks kan ses efter et stykke tid i teksten.

## Kort historie

John Gruber og Aaron Swartz i 2004 skabte Markdown-sproget med ideen om at gøre det muligt for folk at skrive ved at bruge letlæseligt og skrive almindeligt tekstformat og med mulighed for at konvertere det til XHTML eller HTML. Målet bag dets design er læsbarhed - sproget er læsbart, som det er, uden at se ud som om det er blevet tagget eller tilføjet med formateringsinstruktioner, som det gøres i markup-sprog som RTF eller HTML, hvor tags og formateringsinstruktioner er indlysende. Den grundlæggende inspiration er at bruge eksisterende konventioner til markering af almindelig tekst i e-mail.

Siden da er Markdown blevet re-implementeret af andre, ligesom i en Perl [module](https://en.wikipedia.org/wiki/Modular_programming) tilgængelig på [CPAN](https://en.wikipedia.org/wiki/CPAN) og på forskellige andre programmeringssprog. Det distribueres under en [BSD-style license](https://en.wikipedia.org/wiki/BSD_license) og er inkluderet med eller tilgængelig som et plugin til flere [content-management systems](https://en.wikipedia.org/wiki/Content_management_system).

## Tekniske specifikationer for MD-filer

Når noget er skrevet i Markdown, gemmes teksten først i en almindelig tekstfil med filtypenavnet .md eller .markdown, derefter bruges markdown-applikation som Dillinger til behandling af Markdown-fil for at konvertere Markdown-formateret tekst til HTML for at vise den på nettet browsere. Markdown-applikationer bruger en //Markdown-processor// (også almindeligvis omtalt som en parser eller en implementering) til at tage den Markdown-formaterede tekst og udlæse den til HTML-format. Flowdiagrammet for processen er som nedenfor:

Kort sagt er det en fire-trins proces som følger:

1. Først oprettelse af Markdown-filer med en teksteditor eller Markdown-applikation med en udvidelse af .md eller .markdown.
1. Markdown-filen åbnes derefter i en Markdown-applikation.
1. Markdown-applikationen bruges til at konvertere Markdown-filen til et HTML-dokument.
1. HTML-filen ses derefter i en webbrowser, eller Markdown-applikationen bruges til at konvertere den til et andet filformat, såsom PDF.

Markdown er hurtigt og nemt at tage noter, skrive indhold til hjemmeside, producere printklare dokumenter, til at udgive bøger, generere præsentationer og lave dokumenter.

Nogle af versionerne i markdown havde en væsentlig indvirkning på andre versioner så meget, at man ofte vil se dem citeret som en del af andre versioner. Eksempelvis nævner biblioteker støtte til CommonMark (GFM). Lad os tage et kort kig på dem.

### GFM
Markdown er så populær blandt udviklere, fordi open source-delingsplatformen Github accepterede og udvidede sproget med en version kaldet Github Flavored Markup (GFM), som inkluderer indhegnede kodeblokke, URL aultolinking, gennemstregning, tabeller og oprettelse af gøremål.

### CommonMark
Markdown-udviklere forsøgte for nylig at standardisere markdown, de gik sammen for at skabe en version, test og dokumentation til sproget, som er mere robust og kaldes CommonMark. Dette format er lidt nyt og understøtter ikke mange funktioner, men snart vil mange MultiMarkdown-funktioner blive tilføjet.

### Multi-Markdown
Multi-Markdown tilføjede forskellige funktioner til sproget, som understøttes af andre versioner. Oprindeligt blev det skrevet i Perl, men senere flyttet til C. Det understøtter indhegnede kodeblokke, syntaksfremhævning, tabeller, metadata, fragmenter/krydsreferencelinks, fodnoter, gennemstregning, definitionslister, matematik.

## Hvorfor MarkDown?

MD-filer er populære valg af brug af følgende årsager.

1. **Simpel syntaks:** Markdown bruger en enkel og intuitiv syntaks, som er nem at lære og skrive. Syntaksen er designet til at kunne læses som almindelig tekst, hvilket gør den tilgængelig for brugere, der ikke er fortrolige med HTML eller andre mere komplekse markup-sprog.

1. **Platformuafhængig:** Markdown-filer kan oprettes og redigeres på enhver platform, inklusive Windows, Mac og Linux, da de kun er almindelige tekstfiler. Dette gør dem til et populært valg til samarbejde, især i distribuerede teams, hvor forskellige teammedlemmer kan bruge forskellige operativsystemer.

1. **Portabilitet:** Markdown-filer er bærbare, hvilket betyder, at de nemt kan konverteres til andre formater såsom HTML, PDF og Word. Dette gør dem til et ideelt format til at skabe dokumentation, blogindlæg og andre typer indhold, der muligvis skal deles i forskellige formater.

1. **Versionskontrol:** Markdown-filer kan nemt spores og administreres ved hjælp af versionskontrolsystemer såsom Git. Dette gør det nemt at samarbejde om dokumenter med andre teammedlemmer, spore ændringer over tid og vende tilbage til tidligere versioner, hvis det er nødvendigt.

1. **Tilgængelighed:** Markdown-filer er tilgængelige for brugere med handicap, da de nemt kan konverteres til andre formater såsom punktskrift, lyd og skærmlæsbar tekst.

## Referencer

 * [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

