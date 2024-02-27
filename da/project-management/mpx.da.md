{
  "date": "2019-10-11",
  "keywords": [
"mpx fil",
"mpx filformat",
"hvad er en mpx-fil",
"fil",
"mpx eksempel",
"mpx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX - Microsoft Project Exchange-filformat",
  "description": "Lær om MPX-filformat og API'er, der kan oprette og åbne MPX-filer.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-dax"
}
},
  "lastmod": "2021-05-07"
}

## Hvad er en MPX fil? ##

En fil med filtypenavnet .mpx er et Microsoft Exchange-filformat. Et MPX-filformat blev udviklet af Microsoft Project (MSP) for at lette projektinformationsudveksling mellem MSP og andre applikationer, der understøtter MPX-filformatet, inklusive Primavera Project Planner, Sciforma og Timerline Precision Estimating. Ved at bruge MPX-filerne kan du overføre alle former for information fra et projekt til et andet system, såsom detaljerede ressourcetildelingsoplysninger, kalenderoplysninger eller info fra dialogboksen Projektinfo.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. Understøttelse af oprettelse af MPX-filer har dog stoppet udgivelsen af Microsoft Project 2000, og versionerne indtil Microsoft Project 2010 understøtter kun MPX-læsning. MPX-filformatet understøttes ikke i versioner senere end MSP 2010.

## MPX-filformat ##

En oversigt over MPX-filspecifikationerne er givet i dette afsnit. Fuldstændige specifikationer kan findes i denne [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artikel og kan henvises til for detaljer.

### Optegnelser ###

En registrering af MPX-filen består af information for projektet. Der er forskellige typer poster, hvor hver post har sin egen rækkefølge. Hver posttype identificeres ved sit postnummer. For en MPX-fil er det nødvendigt at indeholde posttypen File Creation. Andre typer optegnelser er ikke obligatoriske. Følgende tabel viser alle posttyper, deres postnumre og antallet af poster, hver type kan indeholde i MPX-filen. Recordinkludering i MPX-filen skal følge tabelrækkefølgen, med kommentarer indsat hvor som helst.

|Rekordnavn|Recordnummer|Maksimalt antal poster
---|---|---|
|Oprettelse af filer (påkrævet)|ingen|1
|Valutaindstillinger|10|1
|Standardindstillinger|11|1
|Dato- og tidsindstillinger|12|1
|Basiskalenderdefinition|20|250
|Base kalendertimer|25| 7 pr. basiskalenderdefinitionspost
|Basis kalenderundtagelse|26| 250 pr. basiskalenderdefinitionspost
|Projektoverskrift|30|1
|Tekstressourcetabeldefinition|140|1- (Eller du kan bruge den numeriske ressourcetabeldefinitionpost)
|Definition af numerisk ressourcetabel|41|1
|Ressource|50|9.999
|Ressourcenoter|51| 1 pr. ressourcepost
|Ressourcekalenderdefinition|55| 1 pr. ressourcepost
|Ressourcekalendertimer|56| 7 pr. ressourcekalender
|Ressourcekalenderundtagelse| 57|250 pr. ressourcekalender
|Tekstopgavetabeldefinition|60|1 (Eller du kan bruge den numeriske opgavetabeldefinitionpost)
|Definition af numerisk opgavetabel|61|1
|Opgave|70|9
|Opgavenoter|71| 1 pr. opgavepost
|Gentagende opgave|72| 1 pr. opgavepost
|Ressourcetildeling|75| 100 pr. opgavepost
|Opgave Arbejdsgruppe felter|76| 1 pr. opgavepost
|Projektnavne|80|500
|DDE- og OLE-klientlinks|81|500
|Kommentarer|0|ubegrænset

### Filstruktur ###

En MPX-fil består af poster nævnt ovenfor, der er arrangeret på forudindstillet måde inde i filen. Detaljer om disse registreringstyper diskuteres som følger:

**File Creation Record (FCR):** Dette er en obligatorisk registrering, hvis formål er at identificere:

* Filformat (MPX)

* Listeskilletegn brugt i filen

* Program og versionsnummer brugt til at oprette filen

* Versionsnummer for MPX-filformatet, der bruges i filen

* Kodeside, der bruges til at oprette filen


Dette skal være den første post i filen. Ved eksport fra Microsoft Project er listeseparatortegnet angivet i punktet Regionale indstillinger i Windows Kontrolpanel. En FCR Record indeholder følgende felter:

* MPX umiddelbart efterfulgt af listeseparatortegnet

* Programnavn/identifikator

* Filens versionsnummer

* Kodeside (850, 437, MAC, ANSI)


For eksempel kan posten indeholde information **MPX, Microsoft Project, 3.0**, som angiver, at et komma bruges som listeseparatortegn i denne MPX-fil. Den version af MPX-formatet, der bruges i filen, eksporteres fra Microsoft Project version 3.0.

**Valutaindstillinger** Denne post, der har postnummer 10, specificerer indstillinger for valutaindstillingerne i dialogboksen Indstillinger. Hvis denne post ikke er inkluderet, bruges de aktuelle indstillinger i dialogboksen Indstillinger. Separatorerne tusinder og decimaler er angivet i punktet Regionale indstillinger i Windows Kontrolpanel.
Felterne inkluderet i denne post er:

* Valutasymbol

* Symbolposition (0 # efter, 1 # før, 2 # efter med et mellemrum, 3 # før med et mellemrum)

* Valutacifre (0,1,2)

* Tusinder Separator

* Decimalseparator


**Eksempel:** 10,$,1,2,,,.
Dette eksempel specificerer, at valutaværdier inkluderer et dollartegn ($) foran dem, at to cifre er inkluderet efter decimaltegnet, at et komma bruges til at adskille tusinder, og at et punktum bruges som decimalkomma. Fordi listeseparatortegnet er inkluderet i feltet Thousands Separator, er feltet omgivet af anførselstegn.

**Standardindstillinger:** Denne post, der har postnummer 11, angiver indstillinger for standardindstillingerne i dialogboksen Indstillinger. Hvis en varighed ikke er angivet, skal standardvarighedsenheden indstilles for korrekte varighedsenhedsberegninger. Hvis denne post ikke er inkluderet, bruges de aktuelle indstillinger i dialogboksen Indstillinger.
Felterne inkluderet i denne post er:

* Standard varighedsenheder (0 # minutter, 1 # timer, 2 # dage, 3 # uger)

* Standard varighedstype (0 # ikke fast, 1 # fast)

* Standardarbejdsenheder (0 # minutter, 1 # timer, 2 # dage, 3 # uger)

* Standard timer/dag

* Standard timer/uge

* Standard standardpris

* Standard overtidssats

* Opdatering af opgavestatus Opdatering af ressourcestatus (0 # nej, 1 # ja)

* Opdel igangværende opgaver (0 # nej, 1 # ja)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Felterne inkluderet i denne post er:

* Datobestilling (0 # måned/dag/år, 1 # dag/måned/år, 2 # år/måned/dag)

* Tidsformat (0 # 12 timer, 1 # 24 timer)

* Standardtid (antal minutter efter midnat)

* Datoseparator

* Tidsseparator

* 0:00 til 11:59 SMS

* 12:00 til 23:59 Sms

* Datoformat (0 -14)*

* Søjletekst Datoformat (0 -194)*


**Definition af basiskalender:** Disse poster, der har postnummer 20, definerer basiskalendere og deres arbejds- og ikke-arbejdsdage i ugen. Standardindstillingerne bruges, hvis der ikke er nogen indtastning i en dag. Standardindstillingerne er mandag til fredag for arbejdsdage og lørdag og søndag for ikke-arbejdsdage. I denne post er feltet Navn påkrævet. For hver af dagene angiver en indtastning på 0, at dagen er en ikke-arbejdsdag, og en indtastning på 1 angiver, at dagen er en arbejdsdag.
Felterne inkluderet i denne post er:

* Navn

* Søndag

* Mandag

* Tirsdag

* Onsdag

* Torsdag

* Fredag

* Lørdag


**Basiskalendertimer:** Disse poster, der har postnummer 25, angiver arbejdstiden for ugedagene, hvis de afviger fra standardindstillingerne. Standardarbejdstiden er 8:00 til 12:00 og 13:00 til 17:00. Hver basiskalendertimer-post refererer til den foregående basiskalenderdefinitionspost. Op til syv af disse poster kan følge hver basiskalenderdefinitionspost.

* Ugedag (1 - 7, hvor 1 # søndag og 7 # lørdag)

* Fra tidspunkt 1

* Til tid 1

* Fra tidspunkt 2

* Til tid 2

* Fra tidspunkt 3

* Til tid 3


**Basiskalenderundtagelse:** Disse poster, der har postnummer 26, definerer undtagelserne fra de dage og timer, der er angivet i de to foregående posttyper. Op til 250 af disse poster kan følge hver basiskalenderdefinitionspost. Disse optegnelser skal være opført i kronologisk rækkefølge. Hvis en undtagelse er en dag, kan du lade feltet Til dato stå tomt. Hvis der ikke er angivet nogen tider, bruges standardtiderne 8:00 til 12:00 og 13:00 til 17:00.
Felterne inkluderet i denne post er:

* Fra dato

* Til dato

* Ikke-arbejdende/arbejdende (0 # ikke-arbejdende, 1 # arbejdende)

* Fra tidspunkt 1

* Til tid 1

* Fra tidspunkt 2

* Til tid 2

* Fra tidspunkt 3

* Til tid 3


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Felterne og fanerne inkluderet i denne post er:

* Projektfane

* Selskab

* Manager

* Kalender (Standard bruges, hvis ingen post)

* Startdato (enten dette felt eller det næste felt beregnes for en importeret fil, afhængigt af indstillingen Planlæg fra)

* Slutdato

* Tidsplan fra (0 # start, 1 # finish)

* Nuværende dato*

* Kommentarer

* Omkostninger

* Basisomkostninger

* Faktiske omkostninger

* Arbejde

* Baseline arbejde

* Faktisk arbejde

* Arbejde

* Varighed*

* Baseline Varighed*

* Faktisk varighed

* Procent fuldført

* Baseline Start

* Baseline Finish

* Faktisk start

* Faktisk finish

* Startvarians

* Afslutningsvariance

* Emne

* Forfatter

* Nøgleord


**Definition af tekstressourcetabel**: Denne post viser de ressourcefelter, i rækkefølge, der importeres eller eksporteres. For importerede filer skal navnene matche feltnavnene, der bruges i Microsoft Project. For eksporterede filer kommer denne post fra tabellen med ressourceeksport. Enten denne post eller den numeriske ressourcetabeldefinitionspost skal bruges. Ved eksport fra Microsoft Project er begge disse poster inkluderet.

**Definition af numerisk ressourcetabel:** Ved at bruge tal i stedet for navne viser denne post de ressourcefelter, i rækkefølge, der importeres eller eksporteres. Dette er en alternativ metode til at identificere de ressourcefelter, der er inkluderet i hver ressourcepost, og den er nyttig, når du definerer en MPX-fil, der er oprettet af et fremmedsprogsprodukt.

**Ressource:** Disse poster indeholder oplysningerne for hver ressource, der importeres eller eksporteres. Hver ressourcepost beskriver én ressource. Når du importerer oplysninger, defineres felterne, der er inkluderet, af posten Tekstressourcetabeldefinition eller Numerisk ressourcetabeldefinitionspost. Når du eksporterer oplysninger, er de felter, der er inkluderet, dem, der er angivet i ressourceeksporttabellen.

**Ressourcenoter:** Disse poster indeholder noter om den umiddelbart foregående Ressourcepost. For en ny linje i noten bruges ASCII-tegn 127. Hvis noten indeholder listeseparatortegnet, skal du sætte noten i anførselstegn.

**Definition af ressourcekalender:** Disse poster definerer arbejdsdagene for den ressource, der er angivet i den umiddelbart foregående ressourcepost. For importerede filer, hvis der ikke er nogen indtastning i feltet Basiskalendernavn, bruges Standard. Ingen indtastning for den specifikke dag angiver, at dagen er indstillet til standard (2). Hvis der ikke er nogen ressourcekalenderdefinitionsposter, bruges Standard som basiskalender for ressourcen, med standard for dagene. For hver af dagene angiver en indtastning på 0, at dagen er en ikke-arbejdsdag, 1 angiver, at dagen er en arbejdsdag, og 2 angiver, at standarden er brugt.

**Ressourcekalendertimer:** Disse poster definerer arbejdstiden for ressourcen, der adskiller sig fra den basiskalender, der bruges af ressourcen. Disse registreringer gælder for posten med definition af ressourcekalender umiddelbart før denne post. Op til syv af disse poster kan følge hver Resource Calendar Definition-post.

**Ressourcekalenderundtagelse:** Disse poster definerer undtagelserne fra de dage og timer, der er angivet i de to foregående posttyper. Op til 250 af disse poster kan følge hver Resource Calendar Definition-post. Disse optegnelser skal være opført i kronologisk rækkefølge. Hvis undtagelsen kun er én dag, kan du lade feltet Til dato stå tomt. Hvis der ikke er angivet nogen tider, bruges standardtiderne 8:00 til 12:00 og 13:00 til 17:00.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Definition af numerisk opgavetabel:** Ved at bruge tal i stedet for navne viser denne post opgavefelterne, i rækkefølge, der importeres eller eksporteres. Dette er en alternativ metode til at identificere opgavefelterne, der er inkluderet i hver opgavepost, og den er nyttig, når du definerer en MPX-fil, der er oprettet af et fremmedsprogsprodukt.

**Opgave:** Disse poster indeholder oplysningerne for hver opgave, der importeres eller eksporteres. Hver opgavepost beskriver én opgave. Når du importerer oplysninger, er de felter, der er inkluderet, defineret af posten Tekstopgavetabeldefinition eller Numerisk opgavetabeldefinitionspost. Når du eksporterer oplysninger, er de felter, der er inkluderet, dem, der er angivet i opgaveeksporttabellen.

**Opgavenoter:** Disse poster indeholder noter om den umiddelbart foregående Opgavepost. Brug ASCII-tegn 127 til at angive en ny linje i noten. Hvis noten indeholder listeseparatortegnet, skal du sætte noten i anførselstegn.

**Ressourcetildeling**: Disse poster viser oplysninger om de ressourcer, der er tildelt opgaven, som blev defineret i den foregående opgavepost. Hvis du flette filer, og du ønsker at beholde oplysninger om ressourcetildeling, skal du inkludere oplysningerne i MPX-filen. Hvis du flettes, slettes alle eksisterende opgaver på flettede opgaver. Hvis du flette filer baseret på unikke id'er, tildeles ressourcer ved hjælp af de unikke ressource-id'er i stedet for id'er.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Hvis du bruger arbejdsgruppefunktionerne, skal du inkludere denne registrering for at sikre, at ingen af oplysningerne går tabt.

**Projektnavne:** Disse poster viser alle DDE-linknavne, der er gemt i projektet.

**DDE- og OLE-klientlinks:** Disse poster viser DDE-links til projektet.

**Kommentarer:** Disse poster kan bruges til at tilføje kommentarer til filen og kan vises på en hvilken som helst position i filen. Hver kommentarpost skal begynde med et 0.

## Problemer med at åbne en MPX-fil ##

Her er listen over nogle almindelige problemer, der kan opstå og forårsage fejlfunktion af MPX-formatet:

 *   Fravær af understøttende software
 *   Korrupt fil
 *   Inficeret fil på grund af virus
 *   Ingen adgangsret i systemet til at åbne filerne
 *   Forældet drev i dit system
 *   Filudvidelsen omdøbes

## Referencer ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


