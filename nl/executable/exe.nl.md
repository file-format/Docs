{
  "date" : "2021-06-30",
  "keywords" :[ "exe-bestand", "exe-bestandsindeling", "wat is een exe-bestand", "bestand", "exe-voorbeeld", "exe-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Een .exe-bestand is een Microsoft Executable-bestand dat wordt uitgevoerd op Windows OS. Meer weten over de EXE-bestandsindeling.",
  "title" :"Wat is een uitvoerbaar EXE-bestand?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Wat is een EXE-bestand?

Het woord EXE is een afkorting voor **uitvoerbaar**. Een .exe-bestand is een programma dat kan worden uitgevoerd op het Microsoft Windows-besturingssysteem. Applicatieontwikkelaars publiceren hun programma's voor Windows OS meestal in uitvoerbaar formaat als exe-bestanden. Het is de standaard bestandsindeling om toepassingen op Windows uit te voeren. **Setup.exe**, **Install.exe** en **cmd.exe** zijn enkele veelvoorkomende en bekende namen van EXE-bestanden.

## EXE-bestandsindeling

MS-DOS-compilers werden geïntroduceerd met de geheugenmodellen met de 64K geheugenbeperking. Het algemene concept is om verschillende segmentregisters in de x86 CPU (CS, DS, ES, SS) in te stellen om naar de verschillende of dezelfde segmenten te wijzen, waardoor verschillende niveaus van toegang tot het geheugen mogelijk zijn. Enkele specifieke geheugenmodellen waren:

- **Tiny**: alle geheugentoegangen zijn 16-bits (segmentregisters ongewijzigd). Produceert een .COM-bestand in plaats van een .EXE-bestand.
- **Klein**: alle geheugentoegangen zijn 16-bits (segmentregisters ongewijzigd).
- **Compact**: gegevensadressen omvatten zowel segment als offset, waardoor de DS- of ES-registers opnieuw worden geladen bij toegang en tot 1 miljoen gegevens mogelijk zijn. Codetoegangen veranderen het CS-register niet, waardoor 64K code mogelijk is.
- **Gemiddeld**: codeadressen omvatten het segmentadres, herladen van CS bij toegang en toestaan van maximaal 1M code. Gegevenstoegangen veranderen de DS- en ES-registers niet, waardoor 64K aan gegevens mogelijk is.
- **Groot**: zowel code- als data-adressen zijn (segment, offset) paren, waarbij de segmentadressen altijd opnieuw worden geladen. De volledige geheugenruimte van 1M byte is beschikbaar voor zowel code als gegevens.
- **Enorm**: hetzelfde als het grote model, met extra rekenkunde die door de compiler wordt gegenereerd om toegang te krijgen tot arrays groter dan 64K.

De ontwikkelaars moeten beslissen welk model moet worden geselecteerd bij het maken van een exe-bestand.

### Draagbaar EXE-bestandsformaat

Het draagbare uitvoerbare bestandsformaat (PE) bevat een aantal informatieve headers, het volgende is de lijst met headers:

- **DOS-header**: MS-DOS-header zorgt voor achterwaartse compatibiliteit of een elegante afwijzing van nieuwe bestandstypen.
- **PE Header**: bij offset 60 (0x3C) vanaf het begin van de DOS-header is een pointer naar de PE File-header
- **COFF-header**: de COFF-header bevat informatie die nuttig is voor een uitvoerbaar bestand en informatie die nuttiger is voor een objectbestand.
- **PE Optionele Header**: De PE Optionele Header komt direct na de COFF-header voor, en sommige bronnen laten zelfs zien dat de twee headers deel uitmaken van dezelfde structuur.
- **Sectietabel**: Direct na de PE Optionele Header vinden we een sectietabel. De sectietabel bestaat uit een array van IMAGE_SECTION_HEADER-structuren.
- **Toewijsbare secties**: kan geheugenruimte besparen door de code van een bibliotheek aan meer dan één proces toe te wijzen.

## Kun je een EXE-bestand op een Mac uitvoeren?

Exe-bestanden worden niet gebruikt als uitvoerbare bestanden op Mac OS. Als u echter een exe-bestand op Mac OS wilt uitvoeren, kunnen de volgende methoden worden gebruikt.

1. **Wine** - Wine is de perfecte oplossing voor mensen die hun pc-applicaties op Mac-systemen willen gebruiken. Het is een acroniem dat staat voor "Wine Is Not A Emulator", wat betekent. Wine creëert dezelfde directory-omgeving als door Microsoft wordt gebruikt, zodat u uw Windows-toepassing ermee kunt uitvoeren.
2. **Virtuele machines** - Maak een virtuele Windows-machine met Parallel Desktop of VM Virtual Box en voer uw toepassing uit op de virtuele machine.
3. **Boot Camp** - Door Windows Boot Camp op Mac OS te installeren en configureren, kunt u het Windows-besturingssysteem op een Mac-computer uitvoeren.

## Referenties

* [.exe- door Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

