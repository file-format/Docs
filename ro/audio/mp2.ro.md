{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "fișier mp2", "extensie", "format", "ce este un fișier mp2", "muzică", "format fișier mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MP2 și despre API-urile care pot crea, converti și deschide fișiere MP2.",
  "title" :"MP2 – Format fișier audio MPEG Layer 2",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Ce este un fișier MP2?

Un fișier MP2 care este numit și fișier MPA este un fișier audio comprimat cu stratul II de MPEG-1 sau MPEG-2; un format de compresie audio cu pierderi definit de ISO/IEC 11172-3 alături de MPEG-1 Audio Layer I și MPEG-1 Audio Layer III ([MP3](/ro/audio/mp3/)), pentru a reduce dimensiunea fișierului audio. Întrucât, MP3 este mai popular decât MP2 datorită dimensiunii sale mai mici și disponibilității pe internet. Prin urmare, MP2 este încă un standard vital pentru difuzarea audio.

## Format de fișier MP2

MPEG Audio Layer II (MP2) este algoritmul de bază al standardelor MP3. Codificarea MPEG-1 Audio Layer 2 a fost obținută din codecul audio MUSICAM. A început ca proiect Digital Audio Broadcast (DAB) în Germania, ca parte a programului de cercetare EUREKA. Eureka 147 conținea trei elemente principale: codificarea transmisiei și multiplexarea, modularea COFDM și codarea audio MUSICAM (model de mascare universală sub-bandă integrată codare și multiplexare). MUSICAM a fost una dintre puținele codificări care a reușit să atingă o calitate audio ridicată la rate de biți în intervalul de la 64 la 192 kbit/s pe canal monofonic. Scopul a fost de a oferi întârziere redusă, complexitate redusă, robustețe a erorilor, unități de acces scurte și îndeplinirea cerințelor tehnice de difuzare, telecomunicații și înregistrare pe medii de stocare digitale.

MP2 este un codificator audio sub-bandă, care poate fi comprimat în domeniul timpului cu un banc de filtre cu întârziere redusă care generează 32 de componente ale domeniului de frecvență. Prin comparație, MP3 este un encoder audio transformat cu banc de filtre hibride, ceea ce înseamnă că compresia aplicată în domeniul frecvenței după o transformare hibridă din domeniul timpului. Codificatorul MP2 poate exploata redundanțe între canale folosind codificarea de intensitate „stereo comună” opțională.

### Specificații pentru formatul fișierului MP2

Formatul de fișier MP2 se bazează pe cadre digitale succesive de 1152 de intervale de eșantionare cu patru formate posibile:

- format mono
- format stereo
- format stereo comun codificat cu intensitate (irelevanță stereo)
- format dublu canal (necorelat).
Câteva specificații tehnice importante ale MP2 sunt prezentate în tabelul de mai jos:

|Specificație| Descriere|
---|---|
|**Rate de eșantionare**| 32, 44,1 și 48 kHz|
|**Rate de biți**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 și 384 kbit/s|
|**Rate de eșantionare suplimentare**|16, 22,05 și 24 kHz|
|**Rate de biți suplimentare**|8, 16, 24, 40 și 144 kbit/s|
|**Suport multicanal**|Până la 5 canale audio cu gamă completă și un canal LFE (canal de îmbunătățire a frecvenței joase)|

## Referințe ##

* [MPEG-1 Audio Layer II - După Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

