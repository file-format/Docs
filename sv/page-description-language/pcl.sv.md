{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Läs mer om PCL-filformat och API:er som kan skapa och öppna PCL-filer.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PCL fil? ##

PCL står för Printer Command Language som är ett Page Description Language som introducerats av Hewlett Packard (HP). HP skapade PCL för att ge ett effektivt sätt att kontrollera skrivarfunktioner på många olika utskriftsenheter. Formatet utvecklades ursprungligen för HP:s punktmatris- och bläckstråleskrivare, men har varit en del av olika termo-, matris- och sidskrivare med tidens gång. Formatet genomgick flera olika revisioner, vilket resulterade i olika versioner där varje version förbättrades för att möta tidens krav med avseende på skrivarens kontrollfunktioner. Idag är PCL det mest spridda skrivarspråket på marknaden för lasterskrivare.

## PCL-versioner ##

PCL-versioner skiljer sig åt i funktionalitet (t.ex. stöd för typsnittstyp: bitmappsteckensnitt, skalbara teckensnitt (Intellifonts, TrueType-teckensnitt), rastergrafikkomprimeringsmetoder, HP-GL/2-grafikstöd).

**PCL 1:** runt 1980 - Print and Space-funktionalitet är basuppsättningen funktioner som tillhandahålls för enkel, bekväm arbetsstationsutmatning för en användare.

**PCL 2:** runt 1980 - EDP (Electronic Data Processing)/Transaktionsfunktionalitet är en superset av PCL 1. Funktioner lades till för allmänt bruk, systemutskrift med flera användare.

**PCL 3**: 1984 - Office Word Processing-funktioner är en superset av PCL 2. Funktioner lades till för högkvalitativ kontorsdokumentproduktion och ökad dpi upp till 300 dpi. Det tillät användning av ett begränsat antal bitmappade teckensnitt och grafik, och stödde HP-GL. PCL 3 imiterades i stor utsträckning av andra skrivartillverkare och kallades av dessa företag som "LaserJet Plus-emulering."
(Skrivare: HP DeskJet-familjen, HP LaserJet-skrivare, HP LaserJet Plus-skrivare)

**PCL3+:** Används av skrivare DeskJet och DesignJet-familjen.

**PCL3c:** Används av skrivare i DeskJet och DesignJet-familjen.

**PCL3e**: Används av DeskJet och DesignJet-familjen av skrivare. Används nu även i PhotoSmart.

**PCL3GUI**: Använder RTL och används av skrivare i DeskJet- och DesignJet-familjen.

**PCLSLEEK**: Använder RTL och används av skrivare i DeskJet- och DesignJet-familjen.

**PCL 4**: 1985 - Sidformateringsfunktioner är en superset av PCL 3. Makron som stöds, större bitmappstypsnitt och grafik. (Skrivare: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing-funktionalitet är en superset av PCL 4. Nya publiceringsmöjligheter inkluderar teckensnittsskalning och HP-GL/2 (vektor) grafik. (Skrivare: HP LaserJet III)

**PCL 5e:** 1994 - Det här är en större revidering, som inkluderar nya funktioner som Adaptive Compression System, 2byte teckenkodning, stöd för vektorteckensnitt och dubbelriktade konfigurationskommandon. Inkluderar logiska operationer (motsvarar GDI ROPs) för att förbättra Windows-stödet innan du klipper banor. (Skrivare: HP LaserJet 4)

**PCL 5j:** Nya funktioner som stöd för 2-byte tecken för skalbara teckensnitt i Japan, vertikal skrift, japanska pappersstorlekar och typsnittssträngar. (Skrivare: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Färgstöd och logiska operationer lades till i PCL5. PCL5c föregår PCL5e. Vissa modeller har även stöd för urklippsbanor. (Skrivare: HP Color LaserJet, HP PaintJet 300 XL (första skrivaren med PCL5c), HP DeskJet 1200C/1600C (dessa modellnummer har återanvänts och de nyare modellerna är inte PCL 5c)

**PCL 5ce:** Stöder Agfa Microtype skalbara typsnitt. (Skrivare: HP 2500c Pro-skrivare)

**PCL 6 / XL:** 1996 - PCL 6 eller PCL XL är ett nytt format som introducerades 1995, som inte är kompatibelt med några tidigare versioner av PCL. (Skrivare: HP LaserJet 5, 5M och 5N)

## PCL 6 översikt ##

HP introducerade PCL 6 1996, vilket var nästa utveckling av PCL-språket och relaterade teknologier. Den har följande komponenter:

**PCL 6 Enhanced:** ger optimerad version för utskrift från grafiska användargränssnitt (GUI) som MS Windows och OS/2

**PCL 6 Standard:** ger fullständig bakåtkompatibilitet med tidigare HP LaserJet-skrivare

**PCL Font Synthesis:** tillhandahåller skalbara teckensnitt, teckensnittshantering och lagring av formulär och teckensnitt.

Den utökade versionen PCL XL är närmare GDI som många applikationer använder. Det ser till att färre översättningar sker, vilket resulterar i ökade WYSIWYG-kapacitet och bättre prestanda med applikationer som stöder escapes implementerade av Enhanced-drivrutinen. Utdata från den förbättrade (PCL XL) drivrutinen kanske inte är densamma som utdata från standarddrivrutinen. Om utdata inte är som förväntat, välj standarddrivrutinen (PCL5e) istället.

PCL 6 Enhanced-kommandon är designade för att optimalt matcha grafikutskriftskraven för GUI-baserade applikationer. I de flesta fall, för varje grafikutskriftskommando som ett GUI vill utföra, finns det ett matchande PCL 6 Enhanced-kommando. Detta minskar antalet kommandon som krävs för att beskriva en grafiksida. Varje kommando i PCL 6 Enhanced är utformat för att kräva minimal dataöverföring från värddatorn till skrivaren. Detta minskar mängden data som krävs för att beskriva en sida.

Windows utskriftssystem för de flesta HP LaserJet-skrivare har två separata drivrutiner: Standard och Enhanced. Standarddrivrutinen ger bakåtkompatibilitet genom att använda PCL 6 Standard (PCL5e)-kommandon för att skriva ut enkel text eller blandade text- och grafiksidor. Den förbättrade drivrutinen använder PCL 6 Enhanced-kommandon som har optimerats för att skriva ut komplexa grafiksidor.

## PCL 6 klassversioner ##

#### Klass 1.1 ####

**Ritverktyg:** Stöd ritningslinjer, bågar/ellipser/ackord, (rundade) rektanglar, polygoner, Bezierbanor, klippta banor, rasterbilder, skanningslinjer, rasteroperationer.
**Färghantering:** Stöder 1/4/8-bitars paletter, RGB/grå färgrymd. Stöd anpassade halvtonsmönster (max 256 mönster).
**Kompression:** Stöder RLE.
**Måttenheter:** tum, millimeter, tiondels millimeter.
**Pappershantering:** Stödjer anpassade eller fördefinierade uppsättningar av papperstyper, inklusive vanliga Letter, Legal, A4, etc. Kan välja papper från manuell matning, fack, kassetter. Papper kan duplexas horisontellt eller vertikalt. Papper kan orienteras i stående, liggande eller 180 graders rotation av de två förstnämnda.
**Teckensnitt:** Stöder bitmapp- eller TrueType-teckensnitt, 8 eller 16-bitars kodpunkter. Att välja teckenuppsättning använder annan symboluppsättningskod från PCL 5. När bitmappstypsnitt används är många skalningskommandon inte tillgängliga. När TrueType-teckensnitt används stöds inte beskrivningar av variabel längd, fortsättningsblock. Konturteckensnitt kan roteras, skalas eller klippas.

#### Klass 2.0 ####

**Kompression:** Lade till en proprietär JPEG-komprimering som heter JetReady.
**Pappershantering:** Media kan omdirigeras till olika utmatningsfack (upp till 256). Lade till A6 och japanska B6 förinställda mediastorlekar. Tillagd tredje kassettförinställning, 248 externa fack mediekällor.
**Teckensnitt:** Text kan skrivas vertikalt.

#### Klass 2.1 ####

**Färghantering:** Tillagd färgmatchningsfunktion.
**Kompression:** Lade till deltarad.
**Pappershantering:** Orientering, mediastorlek är valfria när du deklarerar en ny sida. Lagt till B5, JIS 8K, JIS 16K, JIS Exec papperstyper.

#### Klass 3.0 ####

**Färghantering:** Tillåt användning av olika halvtonsinställningar för vektor- eller rastergrafik, text. Stöder adaptiv halvtoning.
**Protokoll:** Stöder PCL-passthrough, vilket gör att PCL 5-funktioner kan användas av PCL 6-strömmar. Vissa PCL 6-tillstånd bevaras dock inte när den här funktionen används.
**Teckensnitt:** Stöder PCL-teckensnitt.
**Viewer/Converter:** PCLReader (gratisprogram) kan visa, konvertera eller skriva ut vilken nivå av PCL 6 som helst (inklusive JetReady) till vilken skrivare som helst.

## Referenser ##

* [PCL - av Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

