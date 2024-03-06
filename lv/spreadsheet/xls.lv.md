{
  "date": "2019-12-16",
  "keywords": [
"XLS",
"failu",
"pagarinājumu",
"faila formātā",
"Excel",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir XLS fails un API, kas tos var izveidot un atvērt.",
  "title": "Kas ir XLS faila formāts? Mācieties no failu formātu ekspertiem!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-lvs"
}
},
  "lastmod": "2019-12-16"
}

## Kas ir XLS fails?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Īsa vēsture

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* 8. versija (izlaista ar Office 97): VBA tika ieviesta kā standarta valoda, un šajā versijā pirmo reizi tika iekļautas noņemtās dabiskās valodas etiķetes. Tas arī pirmo reizi ieviesa papīra saspraudes biroja palīgu.

* 9. versija (izlaists kopā ar Office 2000): 9. versijā bija tikai nelielas izmaiņas, kurās papīra saspraudes biroja palīgs varēja vienlaikus turēt vairākus objektus, kas iepriekš nebija iespējami.

* 10. versija (izlaista ar Office XP): šajā versijā nebija nekādu ievērojamu uzlabojumu.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS faila formāta specifikācijas ##

Dati tiek sakārtoti XLS failā kā bināras straumes saliktā faila veidā, kā aprakstīts Microsoft dokumentā [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx).

#### Straume un apakšstraume ####

Darbgrāmatu attēlo darbgrāmatas straume. Katru darblapu darbgrāmatā attēlo apakšplūsmas. Turklāt tai ir diagrammas lapas apakšstraume, makro lapas apakšstraume vai dialoglodziņa apakšplūsma, kas seko globālajai apakšplūsmai. Katra binārā straume vai apakšstraume, kas satur darbgrāmatas datus, OBLIGĀTI jāraksta kā bināro ierakstu sērija.

#### Ieraksts ####

Informācija par līdzekļiem darbgrāmatā tiek saglabāta kā ieraksts, kas ir mainīga garuma baitu secība. Binārais ieraksts sastāv no šādiem trim komponentiem:

**Ieraksta veids:** Ieraksta tips ir divu baitu neparakstīts vesels skaitlis, kas norāda, kāda veida informācija ir norādīta ierakstā un kā tiek sakārtota un strukturēta šim ierakstam raksturīgo ieraksta datu struktūra. Ieraksta tipa vērtībām OBLIGĀTI ir jābūt vērtībai no ierakstu uzskaites (2.3. sadaļa) vai ierakstam OBLIGĀTI jāizmanto nākotnes ierakstu arhitektūra (2.1.6. sadaļa).

**Ieraksta lielums**: ieraksta lielums ir divu baitu neparakstīts vesels skaitlis, kas norāda baitu skaitu, kas norāda ieraksta datu kopējo lielumu. Ieraksta lielumam OBLIGĀTI ir jābūt lielākam par 0 vai vienādam ar to, un OBLIGĀTI ir mazākam par 8224 vai vienādam ar to.

**Ieraksta dati:** ieraksta datu komponents satur laukus, kas atbilst noteiktam ieraksta tipam un ietver pārējo ieraksta daļu. Lauku secība un struktūra noteiktam ieraksta tipam ir norādīta attiecīgajā ieraksta tipa sadaļā. Ieraksta datu komponentes lielumam OBLIGĀTI ir jābūt vienādam ar ieraksta lielumu. Ieraksta datu komponenta lauki var saturēt vienkāršas vērtības, vērtību masīvus, vairāku lauku struktūras, lauku masīvus un struktūru masīvus.

#### Šūnu tabula ####

Šūnas ir darbgrāmatas pamatbloki, kas glabā darbgrāmatas saturu, piemēram, tekstu, formulas un skaitliskos datus. Šūnas saglabā saglabāto datu ierakstu, izmantojot datu struktūru, ko sauc par šūnu tabulu. Pati šūnu tabula tiek saglabāta ierakstu secībā, kas atbilst specifikāciju dokumentā definētajiem CELLTABLE noteikumiem. Tas sastāv no rindu bloku sērijas, kur rindas ir sakārtotas rindu blokos. Katrā rindu blokā ir rindas no pirmās rindas, kurā ir dati, līdz pēdējai rindai, kurā ir dati.

Dati vai rindas formatējums tiek saglabāts ierakstā Row katram rindu blokam. Katra šūna, kurā ir dati vai atsevišķas šūnas formatējums, tiek attēlota ar ierakstu. Ar šūnu saistīto formatējumu var iegūt no atsevišķas šūnas formatējuma, rindu formatējuma, kolonnu formatējuma vai noklusējuma šūnas formāta. Formatēšanas prioritātes secība ir atsevišķas šūnas formatējums ar augstāko prioritāti, kam seko rindu formatējums un pēc tam kolonnu formatējums un pēc tam noklusējuma šūnas formāts. Šūnas, kas nesatur datus un nesatur atsevišķu formatējumu, netiek saglabātas.

#### Formulas ####

Formula ir vērtību, šūnu atsauces, nosaukumu, funkciju vai operatoru secība šūnā, kas kopā rada jaunu vērtību. Formulas tiek glabātas marķierizētā attēlojumā, kas pazīstams kā parsētās izteiksmes. Parsēta izteiksme izpildes laikā tiek pārveidota par teksta formulu displejai un lietotāja rediģēšanai. Šūnu formulas nosaka ieraksts Formula. Masīva formulas norāda masīva ieraksts. Koplietojamās formulas ir norādītas ShrFmla ierakstā.

#### Diagrammas ####

Diagrammas lapa norāda diagrammu, grafiku, kas parāda datus vai attiecības starp datu kopām vizuālā formā, un diagrammas datu kešatmiņu, trūkst diagrammas datos izmantoto datu lokālās kopijas vai ja ir saites uz ārēju. datu avoti ir bojāti. Diagrammā ir norādītas vienas vai divu asu grupas, asu kopa, pret kurām tiek attēloti diagrammas dati, un diagrammā norādītā sēriju, tendenču līniju un kļūdu joslas kopa. Katra asu grupa norāda vienu līdz četras diagrammu grupas, kas norāda datu attēlošanai izmantotās vizualizācijas veidu. Katra sērija, tendenču līnija un kļūdu josla norāda diagrammas grupu, ar kuru tā ir saistīta.

#### Metadati ####

Metadati ir papildu dati, kas saistīti ar konkrētu šūnu vai tās saturu. Metadati tiek ierakstīti BIFF8 tikai turpmākās paplašināšanas nolūkos.

#### Rakurstabulas ####

Rakurstabula ir mehānisms avota datu apkopošanai, lai iegūtu pārskatu par šo datu izplatību. Rakurstabulā piemērojamās avota datu kolonnas kļūst par laukiem, kurus var izmantot datu apkopošanai. Ja rakurstabulas avota dati ir OLAP avota dati, OLAP hierarhijas un dažas citas OLAP entītijas kļūst par rakurstabulas laukiem.
Rakurstabulai ir divas galvenās daļas — rakurstabulas skats un rakurstabulas skats. Var būt vairāki rakurstabulas skati, kuru pamatā ir viena, nevis OLAP rakurstabula.

#### Stili ####

Šajā pārskatā ir aprakstīts, kā tiek norādīta lapas (1) šūnu formatēšanas un aizsardzības informācija. Šūnu formatējums sastāv no vairākām rekvizītu kopām:

* Fonta īpašības (treknraksts, slīpraksts, fonta krāsa, fonta lielums utt.)

* Aizpildījuma īpašības (priekšplāna krāsa, fona krāsa, raksts, gradients utt.)

* Izlīdzināšanas īpašības (līdzinājums pa kreisi, centrā, pa labi utt.)

* Apmales īpašības (pa kreisi, pa labi, augšā, apakšā, biezs vai plāns, krāsa utt.)

* Ciparu formatēšanas rekvizīti (datums, laiks, decimālzīmju skaits utt.)

* Aizsardzības īpašības (bloķētas, paslēptas utt.)


Šīs īpašības kopumā apraksta, kā tiek parādīta un izdrukāta konkrēta šūna.

## Atsauces Nr.

* [[MS-XLS] — Excel binārā faila formāta struktūra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] — saliktā faila binārais faila formāts](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


