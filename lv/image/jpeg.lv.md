{
  "date": "2019-11-25",
  "keywords": [
"jpeg failu",
"jpeg faila formāts",
"kas ir jpeg fails",
"failu",
"jpeg piemērs",
"jpeg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG - attēla faila formāts",
  "description": "Uzziniet par JPEG failu formātu un API, kas var izveidot un atvērt JPEG failus.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-lvg"
}
},
  "lastmod": "2020-08-08"
}

## Kas ir JPEG fails? ##

JPEG ir attēla formāta veids, kas tiek saglabāts, izmantojot zudumu saspiešanas metodi. Izvades attēls saspiešanas rezultātā ir kompromiss starp krātuves lielumu un attēla kvalitāti. Lietotāji var pielāgot saspiešanas līmeni, lai sasniegtu vēlamo kvalitātes līmeni, vienlaikus samazinot krātuves lielumu. Ja attēlam tiek piemērota saspiešana 10:1, attēla kvalitāte tiek ietekmēta niecīgi. Jo augstāka ir saspiešanas vērtība, jo lielāka ir attēla kvalitātes pasliktināšanās.

## Faila formāta specifikācijas ##

JPEG attēla faila formātu standartizēja Apvienotā fotogrāfiju ekspertu grupa, un līdz ar to arī nosaukumu JPEG. Formāts ir izvēlēts fotoattēlu glabāšanai un pārsūtīšanai tīmeklī. Gandrīz visās operētājsistēmās tagad ir skatītāji, kas atbalsta JPEG attēlu vizualizāciju, kas bieži tiek saglabāti arī ar JPG paplašinājumu. Pat tīmekļa pārlūkprogrammas atbalsta JPEG attēlu vizualizāciju. Pirms iedziļināties JPEG faila formāta specifikācijās, ir jāmin kopējais JPEG izveides darbību process.

### JPEG saspiešanas soļi ###

**Transformācija:** krāsu attēli no RGB tiek pārveidoti par spilgtuma/krāsas attēlu (acs ir jutīga pret spilgtumu, nevis krāsainību, tāpēc krāsainā daļa var zaudēt daudz datu un tādējādi to var ļoti saspiest.

**Uz leju paraugu ņemšana:** Dūnas paraugu ņemšana tiek veikta krāsainajam komponentam, nevis spilgtuma komponentam. Lejušā paraugu ņemšana tiek veikta attiecībā 2:1 horizontāli un 1:1 vertikāli (2h 1 V). Tādējādi attēla izmērs samazinās, jo netiek aizskarts y” komponents, un nav manāms attēla kvalitātes zudums.

**Kārtošana grupās:** katra krāsu komponenta pikseļi ir sakārtoti 8 × 2 pikseļu grupās, ko sauc par datu vienībām”, ja rindu vai kolonnu skaits nav reizināts ar 8, apakšējā rinda un galējās labās kolonnas tiek dublētas.

**Diskrētā kosinusa transformācija:** katrai datu vienībai tiek izmantota diskrētā kosinusa transformācija (DCT), lai izveidotu pārveidoto komponentu karti 8 × 8 formātā. DCT ir saistīta ar zināmu informācijas zudumu datora aritmētikas ierobežotās precizitātes dēļ. Tas nozīmē, ka pat bez kartes būs zināms attēla kvalitātes zudums, taču tas parasti ir mazs.

**Kvantēšana:** katrs no 64 pārveidotajiem komponentiem datu vienībā tiek dalīts ar atsevišķu skaitli, ko sauc par kvantizācijas koeficientu (QC) un pēc tam noapaļots līdz veselam skaitlim. Šeit informācija tiek zaudēta neatgriezeniski, liela kvalitātes kontrole rada lielākus zaudējumus. Kopumā lielākā daļa JPEG ierīču ļauj izmantot JPEG standartā ieteiktās kvalitātes kontroles tabulas.

**Kodējums:** katras datu vienības 64 kvantizētie pārveidotie koeficienti (kas tagad ir veseli skaitļi) tiek kodēti, izmantojot RLE un Hafmana kodēšanas kombināciju.

**Galvenes pievienošana:** pēdējā darbība pievieno galvenes un visus izmantotos JPEG parametrus un izvada rezultātu.

JPEG dekodētājs izmanto apgrieztās darbības, lai ģenerētu sākotnējo attēlu no saspiestā attēla.

### Faila struktūra ###

JPEG attēls tiek attēlots kā segmentu secība, kur katrs segments sākas ar marķieri. Katrs marķieris sākas ar 0xFF baitu, kam seko marķiera karodziņš, lai attēlotu marķiera veidu. Lietderīgā slodze, kam seko marķieris, atšķiras atkarībā no marķiera veida. Tālāk ir norādīti izplatītākie JPEG marķieru veidi.

|Īsais nosaukums|Baiti|Payload|Vārds|Komentāri
---|---|---|---|---|
|SOI|0xFF, 0xD8|nav|Attēla sākums|
|S0F0|0xFF, 0xC0|mainīgs izmērs|Kadra sākums|
|S0F2|0xFF, 0xC2|mainīgs izmērs|Sākt kadram|
|DHT|0xFF, 0xC4|mainīgs izmērs|Definējiet Hafmana tabulas|
|DQT|0xFF, 0xDB|mainīgs izmērs|Definēt kvantēšanas tabulu(-as)|
|DRI|0xFF, 0xDD|4 baiti|Definējiet restartēšanas intervālu|
|SOS|0xFF, 0xDA|mainīgs izmērs|Skenēšanas sākums|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|nav|Restartēt|
|APPn|0xFF, 0xE//n//|mainīgs izmērs|Pielietojums specifisks|
|COM|0xFF, 0xFE|mainīgs izmērs|Komentārs|
|EOI|0xFF, 0xD9|nav|Attēla beigas|

Entropijas kodētos datos pēc jebkura 0xFF baita kodētājs pirms nākamā baita ievieto 0x00 baitu, lai nešķiet, ka tur, kur tas nav paredzēts, ir marķieris, tādējādi novēršot kadrēšanas kļūdas. Dekoderiem šis 0x00 baits ir jāizlaiž. Šis paņēmiens, ko sauc par [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (skatiet JPEG specifikācijas sadaļu F.1.2.3), tiek lietots tikai entropijas kodētiem datiem, nevis marķiera lietderīgās slodzes datiem. Tomēr ņemiet vērā, ka entropijas kodētiem datiem ir daži savi marķieri; īpaši atiestatīšanas marķierus (0xD0 līdz 0xD7), ko izmanto, lai izolētu neatkarīgus entropijas kodētu datu gabalus, lai nodrošinātu paralēlu dekodēšanu, un kodētāji var brīvi ievietot šos atiestatīšanas marķierus ar regulāriem intervāliem (lai gan ne visi kodētāji to dara).

