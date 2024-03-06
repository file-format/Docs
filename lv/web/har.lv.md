{
  "date": "2021-07-08",
  "keywords": [
"HAR",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"JSON",
"Arhīva fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAR — HTTP arhīva faila formāts",
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir HAR fails un API, kas var izveidot un atvērt HAR failu.",
  "linktitle": "HAR",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ha-lvr"
}
},
  "lastmod": "2021-07-08"
}

## Kas ir HAR fails?

Fails ar .har (HTTP arhīva) failu ir HTTP arhīva fails, kas saglabā sesijas datu pārsūtīšanu, izmantojot daudzas pārlūkprogrammas (piemēram, Chrome, Safari, IE, Firefox utt.) [JSON](/web/json/) faila formātā. Dati, kas tiek pārsūtīti internetā starp serveri un klientu (šajā gadījumā lietotāja pārlūkprogrammu), satur HTTP pieprasījumu un atbilžu galvenes, kas tiek saglabātas HAR failā. Tajā ir arī detalizēta informācija par pārlūkprogrammā ielādēto tīmekļa lapu veiktspējas datiem. HAR failus var atvērt jebkurā teksta redaktorā, piemēram, Notepad operētājsistēmā Microsoft Windows un TextEdit operētājsistēmā Apple MacOS.

## HAR faila formāts — vairāk informācijas

HAR faili sesijas informācija tiek glabāta vienkārša teksta failā, izmantojot populāro JSON formātu. HAR faila formāta specifikācijas izstrādāja World Web Consortium (W3C) Web Performance Group, taču tās nevarēja publicēt. Tomēr tas veiksmīgi definēja arhīva formātu HTTP darījumiem.

Papildus pieprasījuma un atbildes informācijas pārsūtīšanas uzraudzībai izstrādātāji izmanto HAR failus, lai reģistrētu tīmekļa pārlūkprogrammas veiktspēju, ņemot vērā lapas ielādes ātrumu, satura ielādes ilgumu, ielādētu saturu, vaicājumus, kas izpildīti, lai saņemtu atbildi no pārlūkprogrammas, un daudz ko citu. .

## Kāpēc izmantot HAR failus?

HAR faili var būt noderīgi, lai uzlabotu vietnes veiktspēju, novērtējot ilgu ielādes laiku, lapas renderēšanas laiku un reakcijas laiku. HAR failus var analizēt, lai atrastu šādas problēmas un atrisinātu visas problēmas ar vietni, lai uzlabotu veiktspēju.

## Kā ģenerēt HAR failu?

Tātad, kā ģenerēt HAR failu? Tas ir atkarīgs no tā, kāda veida pārlūkprogrammu izmantojat HAR faila ģenerēšanai. Šajā rokasgrāmatā mēs uzskaitām Google Chrome pārlūkprogrammas darbības. Metodes HAR failu ģenerēšanai, izmantojot Safari, Firefox u.c., var viegli meklēt internetā un sekot tām.

### Darbības, lai ģenerētu HAR failu, izmantojot Google Chrome

Tālāk norādītās darbības var veikt tīmekļa lapā, kurā ir radušās problēmas.

 1. Pārlūkā Google Chrome atveriet tīmekļa lapu, kurā radās problēma.
 1. Atveriet izstrādātāja rīku (pārbaudiet elementu).
 1. Lai sāktu faila ierakstīšanu, dodieties uz paneļa kreiso pusi. Šajā sadaļā ir maza apaļa sarkana poga.
 1. Noklikšķiniet uz Notīrīt ikonu”, lai izdzēstu visus pārlūkprogrammā saglabātos žurnāla ierakstus.
 1. Lai saglabātu vajadzīgo saturu, kā parādīts iepriekš, ar peles labo pogu noklikšķiniet un noklikšķiniet uz Saglabāt kā HAR failu.

## Atsauces

* [HAR faila formāts — Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))


