{
  "date": "2019-12-13",
  "keywords": [
"ppt fails",
"ppt faila formātā",
"kas ir ppt fails",
"failu",
"ppt piemērs",
"ppt faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PPT faila formātu un API, kas var izveidot un atvērt PPT failus.",
  "title": "PPT — PowerPoint faila formāts",
  "linktitle": "PPT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pp-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PPT fails?

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. PPT fails var saturēt dažādu veidu informāciju, piemēram, tekstu, punktus ar aizzīmēm, attēlus, multividi un citus iegultos OLE objektus. Microsoft izstrādāja jaunāku PowerPoint faila formātu, kas pazīstams kā [PPTX](/presentation/pptx/), sākot no 2007. gada, kas ir balstīts uz Office OpenXML un atšķiras no šī binārā faila formāta. Arī vairākas citas lietojumprogrammas, piemēram, OpenOffice Impress un Apple Keynote, var izveidot PPT failus.

## Īsa vēsture ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. Stabilais binārais formāts tika koplietots kā noklusējuma formāts programmā PowerPoint 97-2003 darbam ar Windows. Bināro failu formātu lasīšanai un rakstīšanai atbalsta jaunākās PowerPoint versijas, kā arī PowerPoint 2016.

## Faila formāta specifikācijas ##

Kopš tā ieviešanas PPT faila formāts ir vairākkārt pārskatīts, lai pievienotu jaunas funkcijas un uzlabojumus. Jaunākās pieejamās versijas specifikācijas ir versijas 6.0 specifikācijas, kas tika publicētas 2018. gada augustā, un tās nedrīkst sajaukt ar reālo produkta numuru PPT faila formātā, jo Microsoft vairs nenodrošina šī formāta modifikācijas.

### Faila formāta pārskats ###

Daži no galvenajiem PPT faila formāta komponentiem ir šādi:

#### Slaidi ####

Lietotāja dati, piemēram, formas, teksts, animācijas un multivide, tiek pievienoti prezentācijai slaidā. Prezentācijā var būt viens vai vairāki slaidi, kas tiek parādīti kā slaidrāde prezentācijas palaišanas laikā. Prezentācijā ir galvenie slaidi un virsrakstu pamatslaidi, kas darbojas kā prezentācijas slaidu kopējo vizuālo īpašību veidne. Ir arī piezīmju galvenais slaids un izdales materiāla galvenais slaids, kas kalpo līdzīgam mērķim un nodrošina kopējus vizuālos rekvizītus visiem piezīmju slaidiem un visiem izdrukātajiem izdales materiāliem.

#### Formas ####

Formas ir objekti, kas ļauj lietotājiem pievienot slaidam dažādu saturu vietturu formu, attēlu un grafiku veidā. Formas galvenajā slaidā nosaka kopīgus datus formu grupām.

#### Vietturu formas ####

Tie ir īpaši vietturi, kas kalpo kā konteineri dažādiem objektiem. Var izmantot dažādas vietturu formas, lai sniegtu norādes, kā ievietot noteikta veida formas, piemēram, tabulas vai diagrammas. Slaidā viettura forma tiek pielāgota vizuālajiem rekvizītiem no galvenā galvenā slaida, virsraksta galvenā slaida vai piezīmju galvenā slaida.

#### Ārējie objekti ####

Slaidā var iegult ārējos objektus, piemēram, iegulto un saistīto audio, saistīto video, iegultos un saistītos OLE objektus un hipersaites. Šos objektus var izmantot, lai aktivizētu saistītos objektus, lai slaidrādes laikā piekļūtu ārējiem resursiem.

### Faila formāta struktūras ###

PowerPoint bināro failu formāti sastāv no šādām plūsmām, lai attēlotu kopējo dokumenta struktūru un datus.

* Pašreizējā lietotāja straume

* PowerPoint dokumentu straume

* Attēlu straume

* Kopsavilkuma informācija un dokumenta kopsavilkuma informācija (pēc izvēles)


Pilnas DOC faila formāta specifikācijas ir atrodamas, kā to nodrošina [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx), un tās ir jāskata, atsaucoties uz sadaļām, kas minētas tālāk sniegtajā detaļā.

#### Pašreizējā lietotāja straume ####

Tas reģistrē pēdējo lietotāju, kurš atvēra dokumentu, un tā nosaukumam ir jābūt Pašreizējais lietotājs.

#### PowerPoint dokumentu straume ####

Uzglabā visu informāciju par PowerPoint prezentāciju un izskaidro tās izkārtojumu un saturu. Tā ir obligāta straume, kuras nosaukumam OBLIGĀTI ir PowerPoint dokuments. Šīs straumes saturu nosaka augstākā līmeņa ierakstu secība. Daļēji kārtošanas ierobežojumi ierakstu secībai ir norādīti PersistDirectoryAtom un UserEditAtom ierakstos.

Kā konteinera ieraksti ieraksti DocumentContainer, MainMasterContainer (2.5.3. sadaļa), HandoutContainer (2.5.8. sadaļa), SlideContainer (2.5.1. sadaļa) un NotesContainer (2.5.6. sadaļa) ir konteinera ierakstu koka sakne. un atomu ieraksti. Jebkurā konteinera ierakstā var būt citi ieraksti, kas nav tieši norādīti kā pakārtotie ieraksti. Nezināmi ieraksti tiek identificēti, ja RecordHeader struktūras lauks recType (2.3.1. sadaļa) satur vērtību, kas nav norādīta RecordType uzskaitījumā (2.13.24. sadaļa). Šie nezināmie ieraksti, ja tie ir sastopami, ir JĀIgnorē un VAR<1> jāsaglabā. Nezināmus ierakstus var ignorēt, meklējot recLen baitus no RecordHeader struktūras beigām.

Katru reizi, kad tiek rakstīta šī straume, esošajai straumei var pievienot jaunus augstākā līmeņa ierakstus, lietotāja labojumus vai visu straumes saturu var aizstāt ar atjauninātu augstākā līmeņa ierakstu secību. Ja visa straume netiek aizstāta, visus iepriekš esošos augstākā līmeņa ierakstus, kas ietvēra jebkuru iepriekšējo lietotāja labojumu, var padarīt novecojušus, izmantojot vēlāk pievienotos augstākā līmeņa ierakstus, kas ietver pašreizējo lietotāja labojumu.

#### Attēlu straume ####

Šī ir izvēles straume, kas satur datus par PowerPoint prezentācijā iekļautajiem attēliem. Tās nosaukumam OBLIGĀTI jābūt Bildes. Šīs straumes saturs ir norādīts OfficeArtBStoreDelay ierakstā, kā norādīts [MS-ODRAW] sadaļā 2.2.21.

#### Kopsavilkuma informācijas straume ####

Tā saglabā statistiku par dokumentu atbilstoši Microsoft Office standartam. Kopsavilkuma informācijas straumes nosaukumam ir jābūt \005SummaryInformation, kur \005 ir rakstzīme ar vērtību 0x0005, nevis virknes burts \005. Šifrētiem dokumentiem šī straume BŪTU jāizlaiž. Šīs straumes saturs ir norādīts [MS-OSHARED] sadaļā 2.3.3.2.1.

#### Dokumentu kopsavilkuma informācijas straume ####

Neobligāta straume, kuras nosaukumam OBLIGĀTI ir jābūt \005DocumentSummaryInformation, kur \005 ir rakstzīme ar vērtību 0x0005, nevis virknes burts \005. Šo straumi VAR <2> izlaist šifrētiem dokumentiem. Šīs straumes saturs ir norādīts [MS-OSHARED] sadaļā 2.3.3.2.2.

#### Šifrēta kopsavilkuma informācijas straume ####

Neobligāta straume, kuras nosaukumam OBLIGĀTI ir jābūt EncryptedSummary”. Šī straume pastāv tikai šifrētā dokumentā. Šīs straumes saturs ir norādīts [MS-OFFCRYPTO] sadaļā 2.3.5.4.

#### Digitālā paraksta krātuve ####

Papildu krātuve, kuras nosaukumam OBLIGĀTI ir _xmlsignatures. To VAR izlaist un VAR ignorēt. Šīs krātuves saturs ir norādīts [MS-OFFCRYPTO] sadaļā 2.5.2.

#### Pielāgota XML datu krātuve ####

Papildu krātuve, kuras nosaukumam OBLIGĀTI ir jābūt MsoDataStore. Krātuves saturs ir norādīts [MS-OSHARED] sadaļā 2.3.6.

#### Parakstu straume ####

Neobligāta straume, kuras nosaukumam OBLIGĀTI ir _signatures. To BŪTU jāizlaiž un VAR ignorēt. Šīs straumes saturs ir norādīts [MS-OFFCRYPTO] sadaļā 2.5.1.

## Atsauces Nr.

* [PPT faila formāta specifikācijas](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: Office izplatītie datu tipi un objektu struktūras](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] — Office dokumentu kriptogrāfijas struktūra](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint failu formāti](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


