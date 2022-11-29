{
  "date" : "2019-10-11",
  "keywords" :[ "mpx-fil", "mpx-filformat", "vad är en mpx-fil", "fil", "mpx-exempel", "mpx-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange-filformat",
  "description":"Läs mer om MPX-filformat och API:er som kan skapa och öppna MPX-filer.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Vad är en MPX fil? ##

En fil med filändelsen .mpx är ett Microsoft Exchange-filformat. Ett MPX-filformat utvecklades av Microsoft Project (MSP) för att underlätta utbyte av projektinformation mellan MSP och andra applikationer som stöder MPX-filformatet, inklusive Primavera Project Planner, Sciforma och Timerline Precision Estimating. Med hjälp av MPX-filerna kan du överföra all slags information från ett projekt till ett annat system, till exempel detaljerad resurstilldelningsinformation, kalenderinformation eller information från dialogrutan Projektinfo.

Microsoft Project 4.0 introducerade stöd för att skapa och läsa MPX-filformat som fortsatte att användas genom Microsoft Project 98. Stöd för att skapa MPX-filer har dock upphört med utgåvan av Microsoft Project 2000, och versionerna fram till Microsoft Project 2010 stöder endast MPX-läsning. MPX-filformat stöds inte i versioner senare än MSP 2010.

## MPX-filformat ##

En översikt över MPX-filspecifikationerna ges i detta avsnitt. Fullständiga specifikationer finns i denna [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artikel och kan hänvisas till för detaljer.

### Records ###

Ett register över MPX-filen består av information för projektet. Det finns olika typer av poster där varje post har sin egen ordning. Varje posttyp identifieras med sitt postnummer. För en MPX-fil är det nödvändigt att innehålla posttypen File Creation. Andra typer av poster är inte obligatoriska. Följande tabell visar alla posttyper, deras postnummer och antalet poster varje typ kan innehålla i MPX-filen. Postinkludering i MPX-filen måste följa tabellordningen, med kommentarer infogade var som helst.

|Rekordsnamn|Rekordsnummer|Maximalt antal poster
---|---|---|
|Skapa fil (krävs)|ingen|1
|Valutainställningar|10|1
|Standardinställningar|11|1
|Inställningar för datum och tid|12|1
|Baskalenderdefinition|20|250
|Bas kalendertimmar|25| 7 per baskalenderdefinitionspost
|Baskalenderundantag|26| 250 per baskalenderdefinitionspost
|Projekthuvud|30|1
|Definition av textresurstabell|140|1- (Eller så kan du använda posten för definition av numerisk resurstabell)
|Definition av numerisk resurstabell|41|1
|Resurs|50|9 999
|Resursanteckningar|51| 1 per resurspost
|Resurskalenderdefinition|55| 1 per resurspost
|Resurskalendertimmar|56| 7 per resurskalender
|Undantag för resurskalender| 57|250 per resurskalender
|Textuppgiftstabelldefinition|60|1 (Eller så kan du använda posten för definition av numerisk uppgiftstabell)
|Definition av numerisk uppgiftstabell|61|1
|Uppgift|70|9
|Uppgiftsanteckningar|71| 1 per uppgiftspost
|Återkommande uppgift|72| 1 per uppgiftspost
|Resursuppdrag|75| 100 per uppgiftspost
|Fält för uppdragsarbetsgrupp|76| 1 per uppdragspost
|Projektnamn|80|500
|DDE- och OLE-klientlänkar|81|500
|Kommentarer|0|obegränsat

### Filstruktur ###

En MPX-fil består av poster som nämns ovan som är ordnade på förinställt sätt inuti filen. Detaljer om dessa posttyper diskuteras enligt följande:

**File Creation Record (FCR):** Detta är en obligatorisk post vars syfte är att identifiera:

* Filformat (MPX)
* Listavgränsare som används i filen
* Program och versionsnummer som används för att skapa filen
* Versionsnummer för MPX-filformatet som används i filen
* Kodsida som används för att skapa filen

Detta måste vara den första posten i filen. När du exporterar från Microsoft Project, anges listseparatortecknet i objektet Regionala inställningar på kontrollpanelen i Windows. En FCR-post innehåller följande fält:

* MPX omedelbart följt av listseparatortecknet
* Programnamn/identifierare
* Filens versionsnummer
* Kodsida (850, 437, MAC, ANSI)

Till exempel kan posten innehålla informationen **MPX, Microsoft Project, 3.0**, som anger att ett kommatecken används som listseparatortecken i denna MPX-fil. Den version av MPX-formatet som används i filen exporteras från Microsoft Project version 3.0.

**Valutainställningar** Denna post, som har postnummer 10, anger inställningar för valutaalternativen i dialogrutan Alternativ. Om denna post inte ingår används de nuvarande inställningarna i dialogrutan Alternativ. Avgränsare för tusentals och decimaler anges i objektet Regionala inställningar på kontrollpanelen i Windows.
Fälten som ingår i denna post är:

* Valutasymbol
* Symbolposition (0 # efter, 1 # före, 2 # efter med ett mellanslag, 3 # före med ett mellanslag)
* Valuta siffror (0,1,2)
* Tusentals separator
* Decimalavskiljare

**Exempel:** 10,$,1,2,",",.
Det här exemplet anger att valutavärden inkluderar ett dollartecken ($) före dem, att två siffror ingår efter decimalkomma, att ett kommatecken används för att skilja tusentals åt och att en punkt används som decimalkomma. Eftersom listseparatortecknet ingår i fältet Tusentalsavskiljare, omges fältet av citattecken.

**Standardinställningar:** Denna post, som har postnummer 11, anger inställningar för standardalternativen i dialogrutan Alternativ. Om en varaktighet inte anges måste standardvaraktighetsenheten ställas in för korrekta varaktighetsberäkningar. Om denna post inte ingår används de nuvarande inställningarna i dialogrutan Alternativ.
Fälten som ingår i denna post är:

* Standard varaktighetsenheter (0 # minuter, 1 # timmar, 2 # dagar, 3 # veckor)
* Standardvaraktighetstyp (0 # inte fast, 1 # fast)
* Standardarbetsenheter (0 # minuter, 1 # timmar, 2 # dagar, 3 # veckor)
* Standard timmar/dag
* Standard timmar/vecka
* Standard standardpris
* Standard övertidsfrekvens
* Uppdatering av uppgiftsstatus Uppdaterar resursstatus (0 # nej, 1 # ja)
* Dela upp pågående uppgifter (0 # nej, 1 # ja)

**Datum- och tidsinställningar:** Denna post, som har postnummer 12, anger inställningar för datum- och tidsalternativen i dialogrutan Alternativ och alternativet Strecktext Datumformat i dialogrutan Layout. Om denna post inte ingår används de nuvarande inställningarna i dialogrutan Alternativ.
\\Fälten som ingår i denna post är:

* Datumordning (0 # månad/dag/år, 1 # dag/månad/år, 2 # år/månad/dag)
* Tidsformat (0 # 12 timmar, 1 # 24 timmar)
* Standardtid (antal minuter efter midnatt)
* Datumavskiljare
* Tidseparator
* 0:00 till 11:59 Sms
* 12:00 till 23:59 Sms:a
* Datumformat (0 -14)*
* Stapeltext Datumformat (0 -194)*

**Baskalenderdefinition:** Dessa poster, som har postnummer 20, definierar baskalendrar och deras arbetsdagar och icke-arbetsdagar i veckan. Standardinställningarna används om det inte finns någon post under en dag. Standardinställningarna är måndag till fredag för arbetsdagar och lördag och söndag för icke-arbetsdagar. I denna post är fältet Namn obligatoriskt. För var och en av dagarna anger en post 0 att dagen är en arbetsfri dag, och en post på 1 anger att dagen är en arbetsdag.
Fälten som ingår i denna post är:

* Namn
* Söndag
* Måndag
* Tisdag
* Onsdag
* Torsdag
* Fredag
* Lördag

**Baskalendertimmar:** Dessa poster, som har postnummer 25, anger arbetstiderna för veckodagarna om de skiljer sig från standardinställningarna. Standardarbetstiderna är 8:00 AM till 12:00 PM och 1:00 PM till 5:00 PM. Varje baskalendertimmarspost hänvisar till föregående baskalenderdefinitionspost. Upp till sju av dessa poster kan följa varje baskalenderdefinitionspost.

* Veckodag (1 - 7, där 1 # söndag och 7 # lördag)
* Från tid 1
* Till tid 1
* Från tid 2
* Till tid 2
* Från tid 3
* Till tid 3

**Baskalenderundantag:** Dessa poster, som har postnummer 26, definierar undantagen från de dagar och timmar som anges i de två föregående posttyperna. Upp till 250 av dessa poster kan följa varje baskalenderdefinitionspost. Dessa poster måste listas i kronologisk ordning. Om ett undantag är en dag kan du lämna Till Datum-fältet tomt. Om inga tider anges används standardtiderna 8:00 till 12:00 och 13:00 till 17:00.
Fälten som ingår i denna post är:

* Från datum
* Hittills
* Icke-arbetande/arbetande (0 # icke-arbetande, 1 # arbetande)
* Från tid 1
* Till tid 1
* Från tid 2
* Till tid 2
* Från tid 3
* Till tid 3

**Projektrubrik:** Denna post, som har postvärde 30, anger globala projektfält, såsom projektets startdatum och projektets slutdatum. Fälten i denna post motsvarar informationen i dialogrutorna Projektinfo och Statistik.
Fälten och flikarna som ingår i denna post är:

* Projektfliken
* Företag
* Chef
* Kalender (standard används om ingen post)
* Startdatum (antingen detta fält eller nästa fält beräknas för en importerad fil, beroende på inställningen Schemalägg från)
* Slutdatum
* Schema från (0 # start, 1 # finish)
* Dagens datum*
* Kommentarer
* Kostnad
* Baslinjekostnad
* Verklig kostnad
* Arbete
* Baslinjearbete
* Faktiskt arbete
* Arbete
* Varaktighet*
* Baslinjelängd*
* Faktisk varaktighet
* Procent färdigt
* Baslinjestart
* Baslinjefinish
* Faktisk start
* Faktisk finish
* Startvarians
* Finish Variance
* Ämne
* Författare
* Nyckelord

**Definition av textresurstabell**: Denna post listar resursfälten, i ordning, som importeras eller exporteras. För importerade filer måste namnen matcha fältnamnen som används i Microsoft Project. För exporterade filer kommer denna post från tabellen för resursexport. Antingen denna post eller definitionsposten för numerisk resurstabell måste användas. Vid export från Microsoft Project ingår båda dessa poster.

**Definition av numerisk resurstabell:** Med hjälp av siffror istället för namn, listar denna post resursfälten, i ordning, som importeras eller exporteras. Detta är en alternativ metod för att identifiera resursfälten som ingår i varje resurspost och är användbar när du definierar en MPX-fil skapad av en främmande språkprodukt.

**Resurs:** Dessa poster innehåller informationen för varje resurs som importeras eller exporteras. Varje resurspost beskriver en resurs. När du importerar information, definieras fälten som ingår av posten Text Resource Table Definition eller Numeric Resource Table Definition-posten. När du exporterar information är fälten som ingår de som anges i tabellen för resursexport.

**Resursanteckningar:** Dessa poster innehåller anteckningar om den omedelbart föregående resursposten. För en ny rad i anteckningen används ASCII-tecken 127. Om anteckningen innehåller listseparatortecknet, omslut anteckningen inom citattecken.

**Definition av resurskalender:** Dessa poster definierar arbetsdagarna för resursen som anges i den omedelbart föregående resursposten. För importerade filer, om det inte finns någon post för fältet Base Calendar Name, används Standard. Ingen inmatning för den specifika dagen indikerar att dagen är inställd på standard (2). Om det inte finns några definitionsposter för resurskalender används Standard som baskalender för resursen, med standard för dagarna. För var och en av dagarna anger 0 att dagen är en icke-arbetsdag, 1 anger att dagen är en arbetsdag och 2 anger att standarden används.

**Resurskalendertimmar:** Dessa poster definierar arbetstimmar för resursen som skiljer sig från baskalendern som används av resursen. Dessa poster gäller för posten Resource Calendar Definition omedelbart före denna post. Upp till sju av dessa poster kan följa varje resurskalenderdefinitionspost.

**Undantag för resurskalender:** Dessa poster definierar undantagen från de dagar och timmar som anges i de två föregående posttyperna. Upp till 250 av dessa poster kan följa varje Resource Calendar Definition-post. Dessa poster måste listas i kronologisk ordning. Om undantaget bara är en dag kan du lämna fältet Till datum tomt. Om inga tider anges används standardtiderna 8:00 till 12:00 och 13:00 till 17:00.

**Definition av textuppgiftstabell:** Denna post listar uppgiftsfälten, i ordning, som importeras eller exporteras. För importerade filer måste namnen matcha fältnamnen som används i Microsoft Project. Om filen exporteras kommer denna post från uppgiftsexporttabellen. Vid export från Microsoft Project ingår båda dessa poster. Fält som beräknas av Microsoft Project, till exempel schemalagd start och schemalagd avslutning, ignoreras om de importeras. Om du har fastställda start- eller slutdatum för uppgiften, använd fälten Begränsningstyp och Begränsningsdatum.

**Definition av numerisk uppgiftstabell:** Med hjälp av siffror istället för namn, listar denna post de uppgiftsfält, i ordning, som importeras eller exporteras. Detta är en alternativ metod för att identifiera uppgiftsfälten som ingår i varje uppgiftspost och är användbar när du definierar en MPX-fil skapad av en främmande språkprodukt.

**Uppgift:** Dessa poster innehåller informationen för varje uppgift som importeras eller exporteras. Varje uppgiftspost beskriver en uppgift. När du importerar information, definieras fälten som ingår av posten Text Task Table Definition eller Numeric Task Table Definition posten. När du exporterar information är fälten som ingår de som listas i uppgiftsexporttabellen.

**Uppgiftsanteckningar:** Dessa poster innehåller anteckningar om den omedelbart föregående uppgiftsposten. Använd ASCII-tecken 127 för att indikera en ny rad i anteckningen. Om anteckningen innehåller listseparatortecknet, omslut anteckningen inom citattecken.

**Resurstilldelning**: Dessa poster visar information om resurserna som tilldelats uppgiften som definierades i föregående uppgiftspost. Om du slår samman filer och du vill behålla information om resurstilldelning måste du inkludera informationen i MPX-filen. Om du slår samman kommer alla befintliga uppdrag på sammanslagna uppgifter att raderas. Om du slår samman filer baserat på unika ID:n tilldelas resurser med hjälp av resursunika ID:n snarare än ID:n.

**Resource Assignment Workgroup Fields:** Dessa poster listar informationen som lagras med varje tilldelning för arbetsgruppsfunktionerna i Microsoft Project 4.0 och 4.1. Om du använder arbetsgruppsfunktionerna måste du inkludera denna post för att säkerställa att ingen av informationen går förlorad.

**Projektnamn:** Dessa poster listar alla DDE-länknamn som är lagrade i projektet.

**DDE- och OLE-klientlänkar:** Dessa poster listar DDE-länkarna till projektet.

**Kommentarer:** Dessa poster kan användas för att lägga till kommentarer till filen och kan visas på valfri plats i filen. Varje kommentarspost måste börja med en "0".

## Problem med att öppna en MPX-fil ##

Här är listan över några vanliga problem som kan uppstå och orsaka att MPX-formatet inte fungerar:

* Avsaknad av stödprogramvara
* Korrupt fil
* Infekterad fil på grund av virus
* Ingen åtkomsträtt i systemet för att öppna filerna
* Föråldrad enhet i ditt system
* Filtillägget döps om

## Referenser ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

