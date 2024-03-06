{
  "date": "2021-03-08",
  "keywords": [
"PML",
"e-lasītājs",
"pagarinājumu",
"formātā",
"e-grāmata",
"Palm iezīmēšanas valoda"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PML faila formātu, Palm Markup Language un API, kas var izveidot un atvērt PML failus.",
  "title": "PML — Palm Markup Language File",
  "linktitle": "PML",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pm-lvl"
}
},
  "lastmod": "2021-03-08"
}

## Kas ir PML fails?

Palm Inc ieviesa PML faila formātu, kas apzīmē Palm Markup Language File. Tās mērķis ir izveidot dokumentus eReader, kas ir planšetdatoram līdzīga e-grāmatu lasīšanas ierīce. PML fails nodrošina [PDB](/programming/pdb/) faila izkārtojumu (kas satur dažādus datu failus), ko parādīt Palm ierīcē.

## PML failu tehniskā informācija

PML failu struktūra sastāv no tagiem e-grāmatas iestatīšanas izveidei, tostarp rindkopām, virsrakstiem, atkāpēm un atsaucēm. Tas arī ļauj izmantot formatēšanas tagus, piemēram, treknrakstu, mazos burtus un augšējo indeksu. Izstrādātāji var arī pievienot attēlus e-grāmatām.

### Palm iezīmēšanas valoda
Šajā tabulā ir norādītas PML komandas:

|Komanda|Apraksts|
---|---|
| \p | Jauna lapa |
| \x | Jauna nodaļa; rada arī jaunu lappuses pārtraukumu. Iekļaujiet nodaļas nosaukumu (un jebkuru stilu kodus) ar \x un \x |
| \Xn | Jauna nodaļa ar atkāpi n līmeņos (n no 0 līdz 4 ieskaitot) nodaļas dialoglodziņā; neizraisa lapas pārtraukumu. Iekļaujiet nodaļas nosaukumu (un jebkuru stilu kodus) ar \Xn un \Xn |
| \Cn=Nodaļas nosaukums | Nodaļu sarakstā ievietojiet Nodaļas nosaukums ar n līmeni (piemēram, \Xn). Lapā teksts netiek rādīts, un tas neizraisa lapas pārtraukumu. Dažreiz tas var būt noderīgi, piemēram, ievietojot nodaļas atzīmi nodaļas ievada sākumā. |
| \c | Centrējiet šo teksta bloku; aizveriet ar \c rindas sākumā |
| \r | Labās taisnošanas teksta bloks; aizvērt ar \r rindas sākumā |
| \i | Slīpveida bloks; aizveriet ar \i |
| \u | Pasvītrot bloku; aizveriet ar \u |
| \o | Overstrike bloks; aizveriet ar \o |
| \v | Neredzams teksts; aizveriet ar \v (var izmantot komentāriem) |
| \t | Atkāpes bloks. Sāciet rindas sākumā, noslēdziet ar \t rindas beigās |
| \T=50% | Atkāpē norādīto ekrāna platuma procentuālo daļu, šajā gadījumā 50%. Ja pašreizējā zīmēšanas pozīcija jau pārsniedz norādīto ekrāna atrašanās vietu, šis tags tiek ignorēts. |
| \w=50% | Iegult horizontālu kārtulu ar noteiktu ekrāna platuma procentuālo daļu, šajā gadījumā — 50%. Šis tags rada rindiņas pārtraukumu pirms un pēc tā. Noteikums ir centrēts. Procentu zīme ir obligāta. |
| \n | Pārslēdzieties uz parasto fontu, ko norādījis lietotājs |
| \s | Pārslēgties uz stdFont; aizveriet ar \s, lai atgrieztos pie parastā fonta |
| \b | Pārslēgties uz boldFont; aizveriet ar \b, lai atgrieztos pie parastā fonta (novecojis; tā vietā izmantojiet \B) |
| \l | Pārslēgties uz lielu fontu; aizveriet ar \l, lai atgrieztos pie parastā fonta |
| \B | Atzīmēt tekstu kā treknrakstu. Atšķirībā no taga \b, \B nemaina fontu, tāpēc var būt liels treknraksts. Jūs nevarat sajaukt \b un \B vienā PML failā. |
| \Sp | Atzīmēt tekstu kā augšrakstu. Nedrīkst jaukt ar citiem stiliem, piemēram, treknrakstu, slīprakstu utt. Iekļaujiet virsraksta tekstu ar \Sp. |
| \Sb | Atzīmēt tekstu kā apakšindeksu. Nedrīkst sajaukt ar citiem stiliem, piemēram, treknrakstu, slīprakstu utt. Iekļaujiet parakstītu tekstu ar \Sb. |
| \k | Padarīt pievienoto tekstu ar maziem burtiem; aizveriet ar \k. Visas rakstzīmes, kas ietvertas \k tagos (ieskaitot tās, kurās ir uzsvars), tiek veidotas ar lielajiem burtiem un tiek atveidotas mazākā izmēra nekā parastās lielo burtu rakstzīmes. |
| \\ | Apzīmē vienu slīpsvītru |
| \aXXX | Ievietojiet rakstzīmi, kas nav ASCII un kuras Windows-1252 kods ir decimālskaitlis XXX. Sīkāku informāciju skatiet PML rakstzīmju tabulā. |
| \UXXXX | Ievietojiet rakstzīmi, kas nav ASCII un kuras Unikoda kods ir heksadecimāls XXXX. Plašāku informāciju skatiet paplašinātajā PML rakstzīmju tabulā. |
| \m=imagename.png | Ievietojiet nosaukto attēlu. Skatiet tālāk sadaļu par attēliem. |
| \q=#linkanchorDaļa teksta\q | Atsauce uz saites enkuru, kas atrodas citā dokumenta vietā. Virkne aiz enkura specifikācijas un pirms beigu \q tiek pasvītrota vai kā citādi parādīta kā saite, skatot dokumentu. |
| \Q=linkanchor | Dokumentā norādiet saites enkuru. |
| \- | Ievietojiet mīkstu defisi. Mīksta defise tiek parādīta tikai tad, ja ir nepieciešams lauzt vārdu pāri līnijai. |
| \Fn=footnote11\Fn | Saistiet 1 ar zemsvītras piezīmi, kuras nosaukums ir zemsvītras piezīme1, kas atzīmēta PML dokumenta beigās. Skatiet tālāk sadaļu par zemsvītras piezīmēm un sānjoslām. |
| \Sd=sidebar1Sānjosla\Sd | Saistiet Sānjoslas tekstu ar sānjoslu, kuras nosaukums ir sānjosla1, kas atzīmēta PML dokumenta beigās. Skatiet tālāk sadaļu par zemsvītras piezīmēm un sānjoslām. |
| \I | Atzīmēt kā atsauces indeksa vienumu. Iekļaujiet indeksa vienumu (un jebkuru stilu kodus) ar \I un \I.|
 

## Atsauces

* [Palm Markup Language — MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-lasītājs — MobileRead](https://en.wikipedia.org/wiki/E-reader)


