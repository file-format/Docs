{
  "date": "2019-10-11",
  "keywords": [
"gif failu",
"gif faila formātā",
"kas ir gif fails",
"failu",
"gif piemērs",
"gif faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF — attēla faila formāts",
  "description": "Uzziniet par GIF faila formātu un API, kas var izveidot un atvērt GIF failus.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GIF fails? ##

GIF vai grafiskais apmaiņas formāts ir ļoti saspiesta attēla veids. Unisys piederošais GIF izmanto LZW saspiešanas algoritmu, kas nepasliktina attēla kvalitāti. Katram attēlam GIF parasti pieļauj līdz 8 bitiem uz pikseļu un līdz 256 krāsām visā attēlā. Pretstatā [JPEG](/image/jpeg/) attēlam, kas var attēlot līdz pat 16 miljoniem krāsu un diezgan pieskaras cilvēka acs robežām. Kad parādījās internets, GIF joprojām bija labākā izvēle, jo tiem bija nepieciešams mazs joslas platums un tie bija saderīgi ar grafiku, kas patērē vienkrāsainas zonas. Animēts GIF apvieno vairākus attēlus vai kadrus vienā failā un parāda tos secībā, lai ģenerētu animētu klipu vai īsu video. Krāsu ierobežojumi ir līdz 256 katram kadram, un, visticamāk, tie ir vismazāk piemēroti citu attēlu un fotoattēlu reproducēšanai ar krāsu gradientu.

## GIF faila formāts ##

Konceptuāli GIF failiem ir fiksēta izmēra grafiskais apgabals, ko aizpilda nulle vai vairāk attēlu. Daži GIF faili sadala fiksēta izmēra grafisko apgabalu vai blokus apakšattēlos, kas animēta GIF gadījumā var darboties kā animēti kadri. GIF formātā bitkartes datu glabāšanai tiek izmantots pikseļu dziļums no 1 līdz 8 bitiem. Attēlu saglabāšanai vienmēr tiek izmantoti RGB krāsu modeļa un paletes dati. Atkarībā no versijas noteikta garuma galvene (GIF87a vai GIF89a) nosaka tipiska GIF faila sākumu.

Pašlaik ir pieejamas divas GIF versijas: 87a un 89a. Pirmais ir sākotnējais GIF formāts, bet otrais ir jaunais GIF formāts. Šajā faila formātā bloku raksturlielumi un pikseļu izmēri ir minēti fiksēta garuma loģiskā ekrāna deskriptorā. Globālās krāsu tabulas esamību un lielumu var norādīt ekrāna deskriptors, kas izseko papildu informāciju, ja tāda ir. Reklāmkadri ir faila pēdējais baits, kurā ir viens ASCII semikola baits. Tipisks GIF87a faila izkārtojums ir šāds:

### Virsraksts ###

Galvenei ir seši baiti, un to izmanto, lai norādītu faila veidu kā GIF. Lai gan loģiskā ekrāna deskriptors ir atdalīts no faktiskās galvenes, tomēr dažreiz tas tiek uzskatīts par otro galveni. Tā pati struktūra, kas tiek izmantota galvenes glabāšanai, var saglabāt loģiskā ekrāna deskriptoru. Visi GIF faili sākas ar 3 baitu parakstu un izmanto rakstzīmes GIF kā identifikatoru. Versija ir arī trīs baitu liela un deklarē GIF faila versiju.

### Loģiskā ekrāna deskriptors ###

Fiksēta garuma attēla deskriptors norāda ekrāna un krāsu informāciju, kas nepieciešama, lai izveidotu GIF attēlu. Laukos Augstums un Platums ietver mazāko ekrāna izšķirtspējas vērtību, kas ir obligāta, lai parādītu attēla datus. Ja displeja ierīce nespēj parādīt norādīto izšķirtspēju, ir jāveic mērogošana, lai atbilstoši parādītu attēlu. Ekrāna un krāsu kartes informācija tiek parādīta četros tālāk esošās tabulas apakšlaukos (turpretim bits 0 ir vismazāk nozīmīgais bits):


|Bits|Apakšlauki
---|---|
|0-2|Globālās krāsu tabulas lielums
|3|Krāsu tabulas kārtošanas karogs
|4-6|Krāsu izšķirtspēja
|7|Globālais krāsu tabulas karogs

#### Globālā krāsu tabula ####

Izvēles globālā krāsu tabula tiek novietota tieši aiz loģiskā ekrāna deskriptora. Šī tabula ir kartēta, lai indeksētu pikseļu krāsu datus attēla datos. Ja nav globālās krāsu tabulas, katrs attēls GIF failā izmanto savu vietējo krāsu. Ja trūkst gan globālās, gan vietējās krāsu tabulas, labāk ir nodrošināt noklusējuma krāsu tabulu. Trīs baitu trīskāršu sērija veido krāsu tabulas elementus. Katrs baits raksturo RGB krāsas vērtību. Sarkanā, zaļā un zilā krāsa tiek izmantota kā katra krāsu tabulas elementa vērtības. Globālās krāsu tabulas ieraksti sasniedz ne vairāk kā 256 ierakstus, un tie vienmēr ir divi pakāpē.

#### Attēla dati ####

Attēla datos tiek glabāts nekodētu simbolu baits, kam seko saistīts apakšsaraksts, kā arī LZW kodētie dati.

#### Reklāmkadri ####

Reklāmkadri ir viens datu baits, kas ir faila pēdējā rakstzīme. Šī baita vērtība pastāvīgi ir 3 Bh, un tā norāda datu straumes beigas. Katram GIF failam ir jābūt reklāmkadri katra faila pēdējā.

## Atsauces Nr.

* [GIF faila formāts](https://en.wikipedia.org/wiki/GIF)


