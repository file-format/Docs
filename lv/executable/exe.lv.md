{
  "date": "2021-06-30",
  "keywords": [
"exe fails",
"exe faila formāts",
"kas ir exe fails",
"failu",
"exe piemērs",
"exe faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": ".exe fails ir Microsoft izpildāmais fails, kas tiek palaists operētājsistēmā Windows OS. Uzziniet vairāk par EXE faila formātu.",
  "title": "Kas ir izpildāms EXE fails?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-lve"
}
},
  "lastmod": "2021-06-30"
}

## Kas ir EXE fails?

Vārds EXE ir saīsinājums no **izpildāmā**. .exe fails ir programma, ko var izpildīt operētājsistēmā Microsoft Windows. Lietojumprogrammu izstrādātāji lielākoties publicē savas programmas Windows OS izpildāmā formātā kā exe failus. Tas ir standarta faila formāts lietojumprogrammu palaišanai operētājsistēmā Windows. **Setup.exe**, **Install.exe** un **cmd.exe** ir daži izplatīti un labi pazīstami EXE failu nosaukumi.

## EXE faila formāts

MS-DOS kompilatori tika ieviesti ar atmiņas modeļiem ar 64K atmiņas ierobežojumu. Vispārīgā koncepcija ir iestatīt dažādus segmentu reģistrus x86 CPU (CS, DS, ES, SS), lai norādītu uz dažādiem vai tiem pašiem segmentiem, tādējādi nodrošinot dažādas piekļuves pakāpes atmiņai. Daži konkrēti atmiņas modeļi bija:

- **Tiny**: visas atmiņas piekļuves ir 16 bitu (segmentu reģistri nav mainīti). Izveido .COM failu, nevis .EXE failu.
- **Mazs**: visas atmiņas piekļuves ir 16 bitu (segmentu reģistri nav mainīti).
- **Kompakts**: datu adreses ietver gan segmentu, gan nobīdi, pārlādējot DS vai ES reģistrus piekļuvei un ļaujot iegūt līdz 1 M datu. Piekļuve kodam nemaina CS reģistru, pieļaujot 64 K kodu.
- **Vidējs**: koda adresēs ir ietverta segmenta adrese, piekļuves CS atkārtota ielāde un līdz 1 M koda atļauja. Piekļuve datiem nemaina DS un ES reģistrus, ļaujot iegūt 64 K datu.
- **Lielas**: gan koda, gan datu adreses ir (segmenta, nobīdes) pāri, vienmēr atkārtoti ielādējot segmentu adreses. Visa 1 M baita atmiņas vieta ir pieejama gan kodam, gan datiem.
- **Milzīgs**: tāds pats kā lielajam modelim, kompilators ģenerē papildu aritmētiku, lai nodrošinātu piekļuvi masīviem, kas lielāki par 64 K.

Izstrādātājiem ir jāizlemj, kurš modelis ir jāizvēlas, veidojot exe failu.

### Pārnēsājams EXE faila formāts

Pārnēsājamais izpildāmā faila formāts (PE) satur vairākas informatīvas galvenes, tālāk ir norādīts galveņu saraksts:

- **DOS galvene**: MS-DOS galvene nodrošina vai nu atpakaļsaderību, vai graciozu jaunu failu tipu samazināšanos.
- **PE galvene**: nobīdē 60 (0x3C) no DOS galvenes sākuma ir rādītājs uz PE faila galveni.
- **COFF Header**: COFF galvenē ir informācija, kas ir noderīga izpildāmajam failam, un informācija, kas ir noderīgāka objekta failam.
- **PE izvēles galvene**: PE izvēles galvene parādās tieši aiz COFF galvenes, un daži avoti pat parāda divas galvenes kā vienas struktūras daļu.
- **Sadaļu tabula**: uzreiz pēc PE izvēles galvenes mēs atrodam sadaļu tabulu. Sadaļu tabula sastāv no IMAGE_SECTION_HEADER struktūru masīva.
- **Mapable Sections**: var ietaupīt vietu atmiņā, kartējot bibliotēkas kodu vairāk nekā vienā procesā.

## Vai Mac datorā varat palaist EXE failu?

Exe faili netiek izmantoti kā izpildāmie faili operētājsistēmā Mac OS. Tomēr, ja vēlaties palaist exe failu operētājsistēmā Mac OS, var izmantot šādas metodes.

 1. **Vīns** — Wine ir ideāls risinājums cilvēkiem, kuri vēlas izmantot savas datora lietojumprogrammas Mac sistēmās. Tas ir akronīms, kas nozīmē Vīns nav emulators. Wine izveido tādu pašu direktoriju vidi, ko izmanto Microsoft, lai jūs varētu palaist savu Windows lietojumprogrammu, izmantojot to.
 2. **Virtuālās mašīnas** — izveidojiet Windows virtuālo mašīnu, izmantojot Parallel Desktop vai VM Virtual Box, un palaidiet lietojumprogrammu virtuālajā mašīnā.
 3. **Boot Camp** — Windows sāknēšanas nometnes instalēšana un konfigurēšana operētājsistēmā Mac OS ļauj darbināt Windows OS operētājsistēmā Mac.

## Atsauces

* [.exe- Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly/Windows izpildāmie faili](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


