{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "fișier", "extensie", "format", "ce este un fișier amr", "muzică", "format fișier amr", "fișier amr", "conversie fișier amr în mp3", "redați fișierul amr"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier AMR și despre API-urile care pot crea, converti și deschide fișiere AMR.",
  "title" :"AMR - Fișier de codec adaptiv cu mai multe rate",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Ce este un fișier AMR?
Fișierul cu extensia .amr este un format de date audio relevant pentru codecul audio **Adaptive Multi-Rate**; constă dintr-un codec de vorbire în bandă îngustă cu mai multe rate, care codifică semnale în bandă îngustă la o rată de biți de 4,75-12,2 kbit/s, cu o voce de calitate cu taxă începând de la 7,4 kbit/s; folosește adaptarea legăturii pentru a selecta una dintre cele opt rate de biți diferite bazate pe.

## Format de fișier AMR
Formatul de fișier AMR utilizează multe tehnici de codare, algoritmul ACELP (Algebraic Code Excited Linear Prediction) fiind una dintre cele mai bune tehnici; conceput pentru comprimarea sunetului vorbit uman într-un mod mai eficient. AMR a fost setat ca codec standard de voce sau de vorbire de către 3GPP în 1999. Formatul de fișier AMR este, de asemenea, utilizat pentru a stoca sunetul vorbit prin utilizarea codecului audio **Adaptive Multi-Rate**, care este folosit de multe telefoane inteligente pentru a stoca înregistrarea. discursuri.

### Structura formatului de fișier
AMR (Adaptive Multi-Rate) este un format audio; utilizat pe scară largă în diverse aplicații și dispozitive mobile, de obicei în player/recorder audio sau în aplicații de tip VoIP. AMR poate fi clasificat în continuare ca:

1. AMR-NB (Bandă îngustă)
2. AMR-WB (bandă largă)

De obicei, AMR se referă la AMR-NB. Formatul de fișier AMR are următoarea structură:

Fiecare fișier AMR conține un antet de 6 octeți care recunoaște fișierul ca audio AMR. Acest antet este întotdeauna setat la:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Acest lucru este de obicei similar în toate fișierele AMR-NB. Dacă antetul urmează un standard, este probabil ca fișierul să fie corupt și să nu fie utilizat. fișierul AMR constă dintr-un număr întreg de cadre audio împachetate. Aceste cadre compun fiecare 20 ms de sunet. Fiecare cadru poate fi codificat folosind oricare dintre modurile AMR-NB valide (0-7, 8 SID în modul DTX). Deoarece cadrele pot fi codificate la rate de biți diferite, această metodă tipică se numește Adaptive Multi-Rate (AMR).
#### Moduri AMR
Mai jos sunt diferitele moduri AMR și ratele de biți corespunzătoare:

|MOD| RAȚELE DE BIȚI|
---|---|
|0| AMR 4.75 - Codifică la 4,75 kbit/s|
|1 | AMR 5.15 - Codifică la 5,15 kbit/s|
|2 | AMR 5.9 - Codifică la 5,9 kbit/s|
|3 | AMR 6.7 - Codifică la 6,7 kbit/s|
|4 | AMR 7.4 - Codifică la 7,4 kbit/s|
|5 | AMR 7.95 - Codifică la 7,95 kbit/s|
|6 | AMR 10.2 - Codifică la 10,2 kbit/s|
|7 | AMR 12.2 - Codifică la 12,2 kbit/s|

Mărimea cadrului modurilor AMR în octeți (inclusiv octetul antetului) este prezentată mai jos:

|CMR |MOD |DIMENSIUNEA CADRU (în octeți)|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5,15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Referințe ##

* [Codec audio Adaptive Multi-Rate - De Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Format RTP Payload și Format de stocare a fișierelor pentru codecurile audio AMR și AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

