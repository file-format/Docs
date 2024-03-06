{
  "date": "2019-12-09",
  "keywords": [
"zip fails",
"zip faila formāts",
"kas ir zip fails",
"failu",
"zip piemērs",
"zip faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIP",
  "description": "Kas ir ZIP fails un API, kas var izveidot un atvērt ZIP failus.",
  "linktitle": "ZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-lvp"
}
},
  "lastmod": "2019-12-09"
}

## Kas ir ZIP fails? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## Īsa ZIP faila formāta vēsture

ZIP faila formāta vēsture aizsākās līdz tiesas procesam, ko System Enhancement Associates (SEA) ierosināja pret PKWARE par tās ARC utilīta izmantošanu bez atļaujām attiecībā uz tās preču zīmi un produkta izskatu un lietotāja interfeisu. Pirms tam Fils Katzs bija pārrakstījis SEA pirmkodu un izlaidis PKXARC, ARC ekstraktoru un PKARC, failu kompresoru, kā bezmaksas programmatūru MS-DOS balstītām sistēmām. Zaudējot tiesas prāvā, PKWARE vairs nevarēja izmantot neko, kas saistīts ar ARC. Šeit tika izveidota jauna failu saspiešana ar nosaukumu ZIP, kas tika iekļauta PKZIP utilītprogrammā PKWARE, Inc.

Katz izlaida ZIP faila formāta specifikācijas publiskajā domēnā, vienlaikus saglabājot īpašumtiesības uz viņa saspiešanas un ekstrakcijas utilītu, piemēram, PKZIP. ZIP saspiešanas sistēma varēja (un spēj) arhivēt failus mapē, izmantojot 32 bitu cikliskās dublēšanas pārbaudes ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritmu, lai saspiestu failu izmērus. Atšķirībā no ARC, .ZIP mapes ietvēra direktoriju failu, kas spēlēja kriptogrāfa kodu grāmatas lomu, glabājot informāciju, kas nepieciešama saspiesto failu renderēšanai.

## Atbalstītās saspiešanas metodes ZIP

Saskaņā ar .ZIP faila formāta specifikācijām tiek atbalstītas šādas saspiešanas metodes.

* Uzglabāt - nenozīmē saspiešanu

* Sarauties

* Samazinājums (tas nozīmē saspiešanas koeficientus no 1. līdz 4. līmenim)

* Eksplodēt

* Iztukšojiet

* Deflat64

* BZIP2

* LZMA (EFS)

* WavPack

* PPMd I versija, 1. versija


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## ZIP faila formāta specifikācijas

ZIP failiem ir iespēja saglabāt vairākus failus, izmantojot dažādas saspiešanas metodes, tajā pašā laikā atbalsta faila saglabāšanu bez saspiešanas. Katrs fails tiek saglabāts/saspiests atsevišķi, kas palīdz tos izvilkt vai pievienot jaunus, visam arhīvam nepiemērojot saspiešanu vai dekompresiju.

### Kopējais ZIP faila formāts

Katrs Zip fails ir strukturēts šādi:


|ZIP faila formāts
---|
|Lokālā faila galvene 1
| Faila dati 1
|Datu deskriptors 1
|Vietējā faila galvene 2
|Faila dati 2
|Datu deskriptors 2
| ....
| ....
| Vietējā faila galvene N
|Faila dati N
|Datu deskriptors N
|Arhīva atšifrēšanas galvene
|Arhivēt papildu datu ierakstu
|Centrālais direktorijs

ZIP faila formāts arhivēšanai izmanto 32 bitu CRC algoritmu. Lai atveidotu saspiestos failus, ZIP arhīva beigās ir direktorijs, kurā tiek saglabāti ietvertie faili un to atrašanās vieta arhīva failā. Tādējādi tam ir kodēšanas loma, lai iekapsulētu informāciju, kas nepieciešama saspiesto failu renderēšanai. ZIP lasītāji izmanto direktoriju, lai ielādētu failu sarakstu, neizlasot visu ZIP arhīvu. Formāts saglabā divas direktoriju struktūras kopijas, lai nodrošinātu lielāku aizsardzību pret datu zudumu.

Katrs ZIP arhīva fails tiek attēlots kā atsevišķs ieraksts, kur katrs ieraksts sastāv no vietējā faila galvenes, kam seko saspiestā faila dati. Arhīva beigās esošajā direktorijā ir atsauces uz visiem šiem failu ierakstiem. ZIP failu lasītājiem vajadzētu izvairīties no vietējo failu galveņu lasīšanas, un visa veida failu saraksts ir jālasa no direktorija. Šis direktorijs ir vienīgais avots derīgiem failu ierakstiem arhīvā, jo failus var pievienot arī arhīva beigās. Tāpēc, ja lasītājs no sākuma lasa vietējās ZIP arhīva galvenes, tas var nolasīt nederīgus (dzēstus) ierakstus, kā arī tos, kas nav daļa no direktorija, kas tiek dzēsts no arhīva.

Failu ierakstu secībai centrālajā direktorijā nav jāsakrīt ar failu ierakstu secību arhīvā.

### ZIP failu ieraksti

Ieraksti ZIP failā tiek sakārtoti viens pēc otra, kur katrs ieraksts sastāv no:

* Vietējā faila galvene

* Izvēles papildu datu lauki

* Lietotāja dati (pēc izvēles saspiesti/pēc izvēles šifrēti)


Katra ieraksta vietējā faila galvenē ir informācija par failu, piemēram, komentārs, faila lielums un faila nosaukums. Papildu datu laukos (neobligāti) var ievietot informāciju par ZIP formāta paplašināšanas opcijām.

#### Vietējā faila galvene

Vietējā faila galvenē ir īpaša lauka struktūra, kas sastāv no vairāku baitu vērtībām. Visas vērtības tiek saglabātas mazā baitu secībā, kur lauka garums skaita garumu baitos. Visas ZIP faila struktūras katram faila ierakstam izmanto 4 baitu parakstus. Centrālā direktorija paraksta beigas ir 0x06054b50, un to var atšķirt, izmantojot savu unikālo parakstu. Tālāk ir norādīta lokālā faila galvenē saglabātās informācijas secība.


|Nobīde|Baiti|Apraksts
---|---|---|
|0|4|Vietējā faila galvenes paraksts # 0x04034b50 (lasīt kā maza izmēra numuru)
|4|2|Izvilkšanai nepieciešamā versija (minimums)
|6|2|Vispārējas nozīmes bitu karodziņš
|8|2|Saspiešanas metode
|10|2|Faila pēdējās modifikācijas laiks
|12|2|Faila pēdējās modifikācijas datums
|14|4|CRC-32
|18|4|Saspiests izmērs
|22|4|Nesaspiests izmērs
|26|2|Faila nosaukuma garums (n)
|28|2|Papildu lauka garums (m)
|30|n|Faila nosaukums
|30+n|m|Papildu lauks

#### Centrālā direktorija faila galvene


|Nobīde|Baiti|Apraksts
---|---|---|
|0|4|Centrālā direktorija faila galvenes paraksts # 0x02014b50
|4|2|Versiju veidojis
|6|2|Izņemšanai nepieciešamā versija (minimums)
|8|2|Vispārējas nozīmes bitu karodziņš
|10|2|Saspiešanas metode
|12|2|Faila pēdējās modifikācijas laiks
|14|2|Faila pēdējās modifikācijas datums
|16|4|CRC-32
|20|4|Saspiests izmērs
|24|4|Nesaspiests izmērs
|28|2|Faila nosaukuma garums (n)
|30|2|Papildu lauka garums (m)
|32|2|Faila komentāra garums (k)
|34|2|Diska numurs, kurā sākas fails
|36|2|Iekšējie faila atribūti
|38|4|Ārējie faila atribūti
|42|4|Lokālā faila galvenes relatīvā nobīde. Šis ir baitu skaits starp pirmā diska sākumu, kurā atrodas fails, un vietējā faila galvenes sākumu. Tas ļauj programmatūrai, kas nolasa centrālo direktoriju, lai atrastu faila atrašanās vietu ZIP failā.
|46|n|Faila nosaukums
|46+n|m|Papildu lauks
|46+n+m|k|Failu komentārs

#### Centrālā direktorija ieraksta beigas


|Nobīde|Baiti|Apraksts
---|---|---|
|0|4|Centrālā direktorija paraksta beigas # 0x06054b50
|4|2|Šī diska numurs
|6|2|Disks, kurā sākas centrālā direktorija
|8|2|Centrālā direktorija ierakstu skaits šajā diskā
|10|2|Kopējais centrālo direktoriju ierakstu skaits
|12|4|Centrālā direktorija lielums (baitos)
|16|4|Centrālā direktorija sākuma nobīde attiecībā pret arhīva sākumu
|20|2|Komentāra garums (n)
|22|n|Komentēt

## Atsauces

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [PKZip faila struktūra](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


