{
  "date": "2020-03-16",
  "keywords": [
"IFC fails",
"Formāts",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par IFC failu formātu un API, kas var izveidot un atvērt IFC failus.",
  "title": "IFC faila formāts",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-lvc"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir IFC fails?

Faili ar IFC paplašinājumu attiecas uz Industry Foundation Classes (IFC) failu formātu, kas nosaka starptautiskus standartus ēku objektu un to īpašību importēšanai un eksportēšanai. Šis faila formāts nodrošina dažādu lietojumprogrammu savietojamību. Šī faila formāta specifikācijas izstrādā un uztur buildingSMART International kā savu datu standartu. IFC faila formāta galvenais mērķis ir uzlabot saziņu, produktivitāti, piegādes laiku un kvalitāti visā ēkas dzīves ciklā.

Pateicoties noteiktajiem standartiem būvniecības nozarē izplatītiem objektiem, tas samazina informācijas zudumu pārraides laikā no vienas lietojumprogrammas uz otru. IFC var glabāt datus par ģeometriju, aprēķiniem, daudzumiem, telpu pārvaldību, cenu noteikšanu utt. daudzām dažādām profesijām (arhitekts, elektriskais, HVAC, konstrukcijas, reljefs utt.).

## Īsa vēsture ##

IFC iniciatīvu 1994. gadā uzņēma Autodesk, lai atbalstītu integrētu lietojumprogrammu izstrādi, un tajā bija iekļauti tādi uzņēmumi kā Honeywell, Butler Manufacturing un AT&T. 1995. gadā dalība tika atvērta ikvienam, un nosaukums tika mainīts uz International Alliance for Interoperability. Bezpeļņas organizācijas nolūks bija publicēt Industry Foundation Class (IFC) kā AEC produkta modeli. 2005. gadā nosaukums atkal tika mainīts, un tagad to uztur buildSMART.

## IFC faila formāts ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Ik pa laikam notika vairākas nelielas izmaiņas, kā arī tās ir iekļautas specifikācijās kā papildinājumi. Tālāk ir saraksts ar dažādām failu specifikāciju versijām, kas iepriekš ir publiskotas.

* IFC4 Add2 (2016)IFC4 Add1 (2015)

* IFC4 (2013. gada marts) ifcXML2x3 (2007. gada jūnijs)

* IFC2x3 (2006. gada februāris) ifcXML2, kas paredzēts IFC2x2 add1 (RC2)

* IFC2x2 1. pielikums (2004. gada jūlijs) ifcXML2, kas paredzēts IFC2x2 (RC1)

* IFC 2x2IFC 2x papildinājums 1ifcXML1 priekš IFC2x un

* IFC2x papildinājums 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


Jaunākās IFC failu formātu specifikāciju versijas vienmēr ir pieejamas buildingSMART vietnē, un izstrādātājam ir jākonsultējas ar tām par jebkāda veida lietojumprogrammām, kuras viņi plāno izstrādāt. Rakstot šo rakstu, 4. versijas specifikācijas ir jaunākās tiešsaistē pieejamās specifikācijas.

### IFC datu failu formāti ###

IFF faila formāts atbalsta datu apmaiņu starp lietojumprogrammām, izmantojot dažādus tālāk norādītos formātus.

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Šim faila formātam ir .ifc faila paplašinājums, un tas ir visbiežāk izmantotais IFC formāts.

**IFC-XML:** tā ir IFC XML faila formāta versija, ko var tieši ģenerēt nosūtošā lietojumprogramma saskaņā ar ISO 10303-28 struktūru, ko sauc arī par STEP-XML. IFC-XML faila formāts tiek uzskatīts par piemērotu sadarbspējai starp XML rīkiem. Salīdzinot ar IFC faila formātu, IFC-XML ir par 300–400% lielāks.

**IFC-ZIP:** tā ir [ZIP](/compression/zip/) saspiesta IFC vai IFC-XML versija, kurā viens no šiem failiem atrodas ZIP arhīva galvenajā direktorijā. Šis formāts saspiež .ifc failu par 60–80% un .ifc XML failu par 90–95%.

### IFC arhitektūra ###

IFC specifikācijā ir iekļauti termini, jēdzieni un datu specifikācijas vienumi, kas izriet no izmantošanas būvniecības un ēku apsaimniekošanas nozares disciplīnās, profesijās un profesijās. Termini un jēdzieni izmanto vienkāršus angļu valodas vārdus, datu vienumiem datu specifikācijā ir ievērota nosaukšanas konvencija.

tipu, entītiju, noteikumu un funkciju datu vienību nosaukumi sākas ar prefiksu Ifc un turpinās ar angļu valodas vārdiem CamelCase nosaukšanas konvencijā (bez pasvītras, vārda pirmais burts ar lielo burtu); atribūtu nosaukumi entītijā atbilst CamelCase nosaukšanas konvencijai bez prefiksa; rekvizītu kopas definīcijas, kas ir daļa no šī standarta, sākas ar prefiksu Pset_ un turpinās ar angļu vārdiem CamelCase nosaukšanas konvencijā; daudzuma kopas definīcijas, kas ir daļa no šī standarta, sākas ar prefiksu Qto_ un turpinās ar angļu vārdiem CamelCase nosaukšanas konvencijā.

IFC datu shēmas arhitektūra definē četrus konceptuālos slāņus, katra atsevišķa shēma tiek piešķirta tieši vienam konceptuālajam slānim.

**Resursu slānis** — zemākais slānis ietver visas individuālās shēmas, kas satur resursu definīcijas, šīs definīcijas neietver globāli unikālu identifikatoru, un tās nedrīkst izmantot neatkarīgi no definīcijas, kas deklarēta augstākā līmenī;

**Pamatslānis** — nākamajā slānī ir ietverta kodola shēma un paplašinājuma pamatshēmas, kas satur vispārīgākās entītiju definīcijas, visām entītijām, kas definētas pamata slānī vai augstāk, ir globāli unikāls ID un pēc izvēles informācija par īpašnieku un vēsturi;

**Savstarpējās izmantojamības slānis** — nākamais slānis ietver shēmas, kas satur entītiju definīcijas, kas raksturīgas vispārīgam produktam, procesam vai resursa specializācijai, ko izmanto vairākās disciplīnās; šīs definīcijas parasti tiek izmantotas starpdomēnu apmaiņai un būvniecības informācijas koplietošanai;

**Domēna slānis** — augstākais slānis ietver shēmas, kas satur entītiju definīcijas, kas ir noteiktai disciplīnai raksturīgu produktu, procesu vai resursu specializācijas; šīs definīcijas parasti tiek izmantotas domēna iekšējai apmaiņai un informācijas apmaiņai.

## Atsauces Nr.

* [Industry Foundation Classes — Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


