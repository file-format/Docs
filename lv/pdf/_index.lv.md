{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portable Document Format (PDF) ir standarta dokumentu attēlojums, kas nav atkarīgs no programmatūras, aparatūras un OS. PDF standarti ietver PDF/A, PDF/E, PDF/UA, PDF/VT un PDF/X.",
  "title" : "PDF faila formāts — kas ir PDF fails?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
"svars : 01"
}
},
  "lastmod" : "2019-09-10"
}

Portatīvais dokumenta formāts (PDF) ir dokumenta veids, ko Adobe izveidoja deviņdesmitajos gados. Šī faila formāta mērķis bija ieviest standartu dokumentu un citu atsauces materiālu attēlošanai formātā, kas ir neatkarīgs no lietojumprogrammatūras, aparatūras un operētājsistēmas. PDF faila formātā ir pilna iespēja saturēt informāciju, piemēram, tekstu, attēlus, hipersaites, veidlapas laukus, bagātinātu multividi, digitālos parakstus, pielikumus, metadatus, ģeotelpiskās funkcijas un 3D objektus, kas var kļūt par avota dokumenta daļu.

Vairumā gadījumu esošie dokumenti tiek pārveidoti PDF formātā, nevis izveidot jaunu PDF failu no jauna. Taču tas nenozīmē, ka nav programmatūras PDF failu izveidei vai manipulēšanai ar tiem.

**(Vai jums ir jādalās ar kaut ko par PDF faila formātu? Savus rezultātus varat publicēt sadaļā [PDF File Format News](https://news.fileformat.com/t/PDF).)**

## PDF faila formāts — īsa vēsture

Īsa laika skala par [PDF file format](https://products.fileformat.com/pdf/) laika skalas izteiksmē ir šāda:

**1993** — Adobe Systems padarīja PDF specifikācijas pieejamas bez maksas

**2008** — PDF kā atvērts standarts tika izlaists 2008. gada 1. jūlijā, un Starptautiskā standartizācijas organizācija to publicēja kā **ISO 32000-1:2008**.

**2008. gads** — Adobe publicēja publisko patentu licenci ISO 32000-1 formāta bezatlīdzības tiesībām attiecībā uz visiem Adobe piederošajiem patentiem, kas ir nepieciešami, lai izveidotu, izmantotu, pārdotu un izplatītu PDF saderīgus implementācijas.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. PDF 1.7, kas kļuva par ISO 32000-1, ietver dažas nestandartizētas patentētas tehnoloģijas, kā arī Adobe XML Forms Architecture (XFA) un JavaScript paplašinājumu programmai Acrobat. 2017. gada 28. jūlijā tika publicēts PDF 2.0, kas pazīstams kā ISO 32000-2:2017, kurā nav iekļautas nekādas nestandartizētas tehnoloģijas.

## PDF faila formāta specifikācijas

PDF fails ir baitu kopa, ko var grupēt marķieros saskaņā ar sintakses noteikumiem, kas noteikti PDF specifikācijās. Vienreiz vai vairāki marķieri tiek apvienoti, veidojot augstāka līmeņa sintaktiskās entītijas, galvenokārt objektus, kas ir pamatdatu vērtības, no kurām tiek izveidots PDF dokuments.

### PDF failu failu struktūra

PDF faila saturs failā ir sakārtots šādā secībā.

|Galvene
|Ķermenis
|Starpatsauču tabula
|Piekabe

#### PDF faila galvene ####

Neatkarīgi no PDF versijas PDF fails sākas ar galveni, kurā ir unikāls PDF identifikators un formāta versija, piemēram, %PDF-1.x, kur x ir no 1 līdz 7.

#### Faila pamatteksts ####

PDF faila pamattekstu veido netiešu objektu secība, kas attēlo dokumenta saturu. Objekti, kā aprakstīts iepriekš, attēlo dokumenta sastāvdaļas, piemēram, fontus, lapas un attēlu paraugus. Sākot ar PDF 1.5, pamattekstā var būt arī objektu straumes, no kurām katra satur netiešu objektu secību.

#### Savstarpēju atsauču tabula ####

Savstarpējās atsauces tabulā ir informācija, kas ļauj nejauši piekļūt failā esošajiem netiešajiem objektiem, tāpēc, lai atrastu kādu konkrētu objektu, nav jālasa viss fails. Tabulā ir vienas rindas ieraksts katram netiešajam objektam, norādot šī objekta baitu nobīdi faila pamattekstā. (Sākot ar PDF 1.5, daļa vai visa savstarpējās atsauces informācija var būt ietverta savstarpējās atsauces plūsmās.

#### Faila reklāmkadri ####

PDF faila reklāmkadri ļauj atbilstošam lasītājam ātri atrast savstarpējās atsauces tabulu un noteiktus īpašus objektus. Atbilstošajiem lasītājiem ir jālasa PDF fails no tā beigām. Faila pēdējā rindā ir tikai faila beigu marķieris %%EOF. Divās iepriekšējās rindās katrā rindā un secībā ir jābūt atslēgvārdam startxref un baitu nobīdei dekodētajā straumē no faila sākuma līdz atslēgvārda xref sākumam pēdējā savstarpējās atsauces sadaļā.

### PDF objekti ###

PDF failā ir ietverti vairāki dažāda veida objekti, kas ir šāda veida

* Būla vērtības — nosacītas patiesas vai nepatiesas

* Skaitļi - veselas un reālās vērtības

* Virknes — iekavās ir rakstzīmes

* Vārdi — sāciet ar uz priekšu / rakstzīmi, piemēram, /ASomewhatLongerName rezultāts ir ASomewhatLangerName

* Masīvi — PDF atbalsta viendimensiju masīvus. Lielāku izmēru masīvus var izveidot, izmantojot masīvus kā ligzdotus elementus

* Vārdnīcas - objektu kā atslēgu-vērtību pāru kolekcija. Tajā var būt nulle ierakstu.

* Straumes - attēlo baitu secību, kas var būt arī neierobežota garuma

* Null Object — apzīmē nulles vērtību


Var būt arī citi objekti, piemēram, komentāri, kas tiek ievadīti ar % zīmi un var saturēt 8 bitu rakstzīmes.

### Netiešie objekti ###

Jebkurš objekts PDF failā var tikt apzīmēts kā netiešs objekts. Netiešajiem objektiem tiek piešķirts unikāls objekta identifikators, ar kuru citi objekti var atsaukties uz tiem. Savstarpējās atsauces uz tiem tiek uzturētas indeksa tabulā un atzīmētas ar xref atslēgvārdu, kas seko galvenajam pamattekstam un sniedz katra netiešā objekta baitu nobīdi no faila sākuma.

### Lineāri un nelineāri PDF izkārtojumi ###

Atkarībā no mērķa lietojumprogrammām un citiem faktoriem PDF izkārtojumi tiek klasificēti kā Llnear un nelineāri.

Nelineāri — nelineārie PDF faili aizņem mazāk vietas diskā, salīdzinot ar lineārajiem PDF failiem. Dokumenta PDF lapas ir izkaisītas visā PDF failā, un tāpēc nelineārie faili ir lēnāki, salīdzinot ar lineārajiem failiem.

Lineārs PDF — tiešsaistes PDF skatītāju mērķauditorijas atlasei Lineārie PDF faili ir izveidoti tā, lai tie tiktu ierakstīti diskā lineāri. Šim nolūkam nav nepieciešami pārlūkprogrammas spraudņi, lai viss dokuments tiktu ielādēts pirms parādīšanas.

### Objektu pārskats ###

Kā minēts, PDF pamatteksts ir iepriekš minēto objektu kolekcija. PDF lielākoties ir balstīts uz PostScript bez programmēšanas valodu vadības funkcijām, piemēram, if un cilpas komandām. Postscript koda izdotās komandas grafiskā satura ģenerēšanai tiek apkopotas un marķētas papildus visiem dokumentā minētajiem failiem, grafikiem vai fontiem. Viss šis saturs tiek uzkrāts vienā failā, kā rezultātā tiek izveidota PostScript izvade.

#### Teksts ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Grafika ####

Grafikas operatori, kas tiek izmantoti PDF satura straumēs, apraksta to lappušu izskatu, kuras paredzēts reproducēt rastra izvades ierīcē. Telpas ir paredzētas gan printeru, gan displeja lietojumprogrammām. Grafikas operatori veido sešas galvenās grupas:

* Grafikas stāvokļa operatori manipulē ar datu struktūru, ko sauc par grafikas stāvokli, globālo sistēmu, kurā izpilda citi grafikas operatori. Grafikas stāvoklis ietver pašreizējo transformācijas matricu (CTM), kas PDF satura straumē izmantotās lietotāja telpas koordinātas kartē izvadierīces koordinātēs. Tas ietver arī pašreizējo krāsu, pašreizējo apgriešanas ceļu un daudzus citus parametrus, kas ir gleznošanas operatoru netiešie operandi.

* Ceļu veidošanas operatori norāda ceļus, kas nosaka dažādu veidu formas, līniju trajektorijas un reģionus. Tie ietver operatorus jauna ceļa sākšanai, līniju segmentu un līkņu pievienošanai un tā aizvēršanai.

* Ceļa krāsošanas operatori aizpilda ceļu ar krāsu, krāso pa to insultu vai izmanto to kā apgriešanas robežu.

* Citi gleznošanas operatori krāso noteiktus pašaprakstošus grafikas objektus. Tie ietver paraugus attēlus, ģeometriski definētus ēnojumus un visas satura straumes, kas savukārt satur grafikas operatoru secības.

* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* Atzīmētā satura operatori augstāka līmeņa loģisko informāciju saista ar objektiem satura straumē. Šī informācija neietekmē satura renderēto izskatu; tas ir noderīgi lietojumprogrammām, kas dokumentu apmaiņai izmanto PDF.


## Atsauces Nr.

* [PDF faila formāts: pamata struktūra](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)

* [PDF — Wikipedia](https://en.wikipedia.org/wiki/PDF)

* [PDF atsauce — Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)


