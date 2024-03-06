{
  "date": "2021-08-16",
  "keywords": [
"nrg fails",
"nrg faila formāts",
"kas ir nrg fails",
"failu",
"nrg piemērs",
"nrg faila paplašinājums",
"pagarinājumu",
"formātā",
"nrg kājene",
"nrg faila formāts",
"Nero Burning Rom",
"Nero AG"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par NRG failu formātu un API, kas var izveidot un atvērt NRG failus.",
  "title": "NRG - diska attēla faila formāts",
  "linktitle": "NRG",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nr-lvg"
}
},
  "lastmod": "2021-08-16"
}

## Kas ir NRG fails?

Attēla faila formāts, kas izveidots, izmantojot optisko disku, tiek uzskatīts par NRG faila formātu. Šo formātu Nero ir īpaši izveidojis Nero Burning Rom utilītai. Tiek uzskatīts, ka diska attēlu glabāšanai tiek izmantots šis formāts, kas ir piemērots šiem konkrētajiem failiem. Šie faili var būt precīzas kompaktdiska vai DVD kopijas formā, vai arī tiem var būt vairāki faili, kurus var uzstādīt kā disku. Citi populārāki failu formāti, piemēram, [ISO](/compression/iso/) failu formāti, ir tie, kuros šos failus var konvertēt uz dažām pamata utilītprogrammām. Galvenokārt NRG faili tiek izmantoti, lai izveidotu dažu svarīgu datu vai disku dublējumus vai kopijas.

## NRG faila formāts ##

Šo faila formātu Nero AG izstrādāja kā diska attēla formātu. Tam bija īpaša utilīta Nero Burning Rom īpašība, jo tā tika izstrādāta diska attēlu glabāšanai. Tās pirmā versija tika norādīta, lai saglabātu vērtības kā 32 bitu veselus skaitļus. Tomēr tā otrā versija tika palaista, un tajā bija atbalsts 64 bitu veseliem skaitļiem.

## Tehniskā specifikācija ##

Faila sākumā šis formāts nesaglabā tā datus kā galveni. Tāpat kā kājene, tā ir pievienota faila beigās. IFF gabalu veidā tiek saglabāta attēla informācija. Pirmā gabala nobīdi var iegūt, nolasot NRG kājeni no faila pēdējiem 8 līdz 12 baitiem. Visās NRG faila formāta versijās ir pievienoti gabali, DAOI, kompaktdiska teksts, sesijas informācijas nesēja veids, diska informācija, Relo un ķēdes beigas. Baitu secība ir liela, un visas veselo skaitļu vērtības saglabāšanas laikā ir neparakstītas.

### Galvenie gabali ###

#### Bižu lapa ####

Šī norādes lapa ir viegli pieejama visās NRG failu formāta versijās. **CUEX** gabals nozīmē fiksēta lieluma savienojuma blokus, un katrs no tiem apzīmē norādes punktu.

#### DAO informācija ####

Šī informācija ir pieejama arī visās NRG formāta versijās. **DAOI** gabalos tiek glabāta atbilstošā specifiskā informācija divās daļās. Tās pirmā daļa sastāv tikai no sesijas datiem. Tās otrā daļa tikai atkārto pelēko informāciju, kas saistīta ar izsekošanu, un tā ir tikai vienu reizi katram ierakstam.

#### CD teksts ####

Tas ir pieejams NRG otrajā versijā. **CDTX** gabals sastāv no CD teksta pakotnes neapstrādātas savienojuma, kurā katram ir 18 baiti.

#### Paplašināta celiņa informācija ####

Tas ir pieejams visās NRG faila formāta versijās. Šīs daļas tiek izmantotas, lai saglabātu izsekošanas informāciju reizē sesiju izsekojumam. Šie dati tiek atkārtoti tikai vienu reizi katram ierakstam.

#### Sesijas informācija ####

Tas ir pieejams arī katrā NRG faila formāta versijā. Informācija par sesijas daļām ir jāizmanto, lai ātri skenētu sesijas attēlu un pēc tam izsekotu skaitu.

#### Ķēdes beigas ####

Gala gabals nozīmē signālus, ka tagad vairs nav jālasa gabali, un tas ir pieejams arī visās NRG versijās.


## Atsauces Nr.

* [NRG — Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))



