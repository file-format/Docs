{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"failu",
"pagarinājumu",
"faila formātā",
"Excel binārā izklājlapas fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir XLSB fails un API, kas tos var izveidot un atvērt.",
  "title": "Kas ir XLSB fails?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-lvb"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir XLSB fails?

XLSB faila formāts norāda Excel bināro failu formātu, kas ir ierakstu un struktūru kolekcija, kas norāda Excel darbgrāmatas saturu. Saturs var ietvert nestrukturētas vai daļēji strukturētas skaitļu tabulas, tekstu vai gan skaitļus, gan tekstu, formulas, ārējos datu savienojumus, diagrammas un attēlus. Atšķirībā no [XLSX](/spreadsheet/xlsx/) (kas ir balstīts uz Open XML faila formātu), XLSB apzīmē bināro Excel darbgrāmatas failu. XLSB failus var lasīt un rakstīt ātrāk, tāpēc tie ir noderīgi darbam ar lieliem failiem. XLSB tiek reti izmantots darbgrāmatu glabāšanai, jo XLSX (un iepriekš [XLS](/spreadsheet/xls/)) ir visizplatītākie lietotāju atlasītie failu formāti darbgrāmatu saglabāšanai. To var atvērt, izmantojot Microsoft Office 2007 un jaunākas versijas.

## XLSB faila formāta specifikācijas ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Kopš tā laika specifikācijas ir vairākas reizes pārskatītas, un jaunākā specifikāciju versija (v 10.0) tika publicēta 2018. gada aprīlī. Microsoft specifikācijas ir publiski pieejamas kā [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx), un ikvienam ir jāiepazīstas ar tiem, lai lasītu vai failu rakstīšana XLSB faila formātā.

## XLSB faila struktūra ##

XLSB fails ir pakotne, kas sastāv no daļu kolekcijas. Šīs daļas satur informāciju par darbgrāmatas saturu, tostarp darbgrāmatas datus un pakotnes struktūru. Dažas daļas satur informāciju, kas saglabāta, izmantojot bināros ierakstus, dažas kā XML, savukārt citās ir informācija, kas tiek glabāta kā baitu bināra plūsma. Katrā binārajā ierakstā ir nulle vai vairāk strukturētu lauku, kas satur darbgrāmatas datus.

#### Iepakojums ####

XLSB pakotne ir [ZIP](/compression/zip/) arhīvs, kurā jāietver tieši viena darbgrāmatas daļa. Šai daļai ir jābūt šīs paketes attiecību daļas attiecību mērķim. Darbgrāmatas daļa ir XLSB dokumenta sākuma daļa.

#### #### daļa

Daļa ir baitu straume, kurai ir saistīts satura tips, kas norāda daļā saglabātā satura veidu un veidu. Dažas daļas glabā informāciju binārā formātā, bet citas glabā informāciju kā XML. Specifikāciju dokumenta sadaļā [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) ir norādītas derīgās daļas, satura veidi un obligātās/neobligātās attiecības starp visām pakotnes daļām.

#### Attiecības ####

Avotu un mērķa resursu savieno attiecības. Attiecības var būt:

**Pakotnes saistība:** kur mērķis ir daļa un avots ir pakotne kopumā

**Attiecības starp daļām:** kur mērķis ir pakotnes daļa un avots ir daļa

**Izteikta saistība:** kur uz resursu ir atsauce no avota daļas satura, atsaucoties uz attiecību elementa ID atribūta vērtību

**netiešās attiecības** ir attiecības, kas nav tiešas

**Iekšējās attiecības:** kur mērķis ir pakotnes daļa

**Ārējās attiecības:** ja mērķis ir ārējs resurss, kas nav iekļauts pakotnē

#### Ieraksts ####

Ieraksts ir pamata veidošanas bloks, ko izmanto, lai saglabātu informāciju par līdzekļiem darbgrāmatā. Katrs binārais ieraksts ir mainīga garuma baitu secība. Binārais ieraksts sastāv no trim sastāvdaļām:

* ieraksta veids

* rekordliels izmērs un

* ieraksta dati, kas ir raksturīgi šim ieraksta veidam.


**Ieraksta veids:** Ieraksta tips parāda ieraksta norādīto ieraksta veidu. Tas arī norāda šim ierakstam raksturīgo ieraksta datu struktūru. Derīgie ierakstu veidi ir norādīti specifikāciju dokumenta sadaļā [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx). Ieraksta tipam ir jābūt vienam vai diviem baitiem, un tam ir jābūt lielākam vai vienādam ar 128 un mazākam par 16384.

**Ieraksta lielums:** ieraksta lielums norāda baitu skaitu, kas norāda kopējo ieraksta datu lielumu. Šai vērtībai OBLIGĀTI ir viens līdz četri baiti. Šai vērtībai OBLIGĀTI ir jābūt vienam baitam, ja augstais bits zemajā baitā ir vienāds ar 0; pretējā gadījumā šai vērtībai OBLIGĀTI ir jābūt lielākai par vienu baitu. Ja baitu skaits ir lielāks par vienu baitu, augstais bits katrā secīgajā baitā norāda, vai tiek izmantots papildu baits. Ja otrā baita augstais bits ir vienāds ar 1, tad šai vērtībai OBLIGĀTI jāizmanto papildu trešais baits. Ja trešā baita augstais bits ir vienāds ar 1, tad šai vērtībai OBLIGĀTI jāizmanto papildu ceturtais baits. Ceturtā baita augstais bits OBLIGĀTI ir jāignorē. Vērtība sastāv no septiņiem katra baita zemajiem bitiem, kas apvienoti. Zemie, vismazāk nozīmīgie biti atrodas pirmajā baitā, un katrs nākamais baits satur augstākas kārtas bitus nekā iepriekšējais baits.

**Ieraksta dati:** ieraksta datu komponents satur laukus, kas atbilst noteiktam ieraksta tipam un ietver pārējo ieraksta daļu. Lauku secība un struktūra noteiktam ieraksta tipam, kas norādīts sadaļā Ierakstu uzskaitījums, ir norādīta attiecīgajā ieraksta tipa sadaļā Ieraksti. Kopējam ieraksta datu komponenta izmēram OBLIGĀTI ir jābūt vienādam ar ieraksta lielumu. Ieraksta datu komponenta lauki var saturēt vienkāršas vērtības, vērtību masīvus, vairāku lauku struktūras, lauku masīvus un struktūru masīvus.

#### XLSB ieraksta piemērs ####

Tālāk norādītais ieraksta veids un ieraksta lielums nosaka **BrtCommentText** ierakstu, kura izmērs ir 200 baiti:

11111101 00000100 11001000 00000001 [Ieraksta lauki]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, kas ir vienāds ar 512. Ieraksta tipa vērtība ir 125 + 512 vai 637, kas atbilst **BrtCommentText** ieraksta tipam. Nākamais baits ir 11001000, kas norāda zemu vērtību 72 un ieraksta lielumu prasa otru baitu. Otrais baits ir 00000001, kas norāda lielāku vērtību 1 * 128 un ka ieraksta lielumam nav nepieciešams papildu baits. Ieraksta lielums ir 72 + 128 vai 200, kas norāda ieraksta datu komponenta kopējo lielumu baitos. Ieraksta datu komponenta laukus norāda **BrtCommentText**.

## Atsauces Nr.

* [[MS-XLSB] — Excel (.xlsb) binārais faila formāts](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


