---
date: 2020-08-12
keywords: flif, .flif, format de fișier flif, cum se deschide fișierele flif, extensia .flif, extensia flif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier FLIF
linktitle: FLIF
description: "Aflați despre formatul de fișier FLIF și despre API-urile care pot crea și deschide fișiere FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Ce este un fișier FLIF? ##

FLIF (Free Lossless Image Format) este un format de imagine fără pierderi care utilizează extensia .flif pentru fișierele sale. FLIF pretinde că depășește [PNG](/ro/image/png/), [WebP] fără pierderi (/ro/image/webp/), BPG fără pierderi și JPEG 2000 fără pierderi în ceea ce privește raportul de compresie. FLIF folosește intercalarea progresivă, datorită căreia orice descărcare parțială a imaginii poate fi folosită ca codificare cu pierderi pentru întreaga imagine.

## Scurt istoric ##

FLIF a fost anunțat în septembrie 2015, iar versiunea alfa a fost lansată în octombrie 2015. În septembrie 2016, a fost lansată prima versiune stabilă a FLIF.

## Design FLIF ##

FLIF folosește o variantă de CABAC (codare aritmetică binară adaptativă la context), MANIAC (codificare aritmetică a numărului întreg aproape de zero meta-adaptativ) pentru compresie. MANIAC este un algoritm de codare a entropiei dezvoltat de Jon Sneyers și Pieter Wuille. În MANIAC, contextele sunt noduri de arbori de decizie care sunt învățate în timpul codificării în mod dinamic. Acest lucru face ca modelul de context să fie mai specific imaginii și are ca rezultat o compresie mai bună. FLIF are următoarele caracteristici:

- Suporta compresia fara pierderi
- Suportă compresie cu pierderi cu preprocesare a codificatorului
- Suportă în tonuri de gri, RGB și RGBA
- Suportă adâncimea de culoare de la 1 la 16 biți pe canal
- Suportă fișiere întrețelate și neîntrețelate
- Acceptă decodarea progresivă a fișierelor descărcate parțial
- Suporta animatii
- Suportă profiluri de culoare ICC încorporate, metadate Exif și XMP
- Are suport limitat pentru comprimarea fișierelor raw ale camerei (RGGB)

## Format fișier FLIF ##

Un fișier FLIF are următoarele patru părți:

## Antet principal ##

Antetul principal conține metadatele principale, inclusiv lățimea, înălțimea, adâncimea culorii, numărul de cadre.

|Tip|Valoare|Descriere|
|---|---|---|
|4 octeți|„FLIF”|Magie|
|4 biți|3 = ni still; 4 = eu încă; 5 = ni anim; 6 = i anim|Interlacing, animation|
|4 biți|1 = Tonuri de gri; 3 = RGB; 4 = RGBA|Numărul de canale (nb_channels)|
|1 octet|'0','1','2' ('0'=personalizat)|Bytes per canal (Bpc)|
|varint|width-1|Width|
|varint|height-1|Inaltime|
|varint|nb_frames-2 (doar dacă animație)|Numărul de cadre (nb_frames)|

## Bucăți de metadate ##

Această parte conține metadate non-pixel, cum ar fi Exif/XMP, profil de culoare ICC etc., care este codificat folosind compresia DEFLATE. Aceste bucăți sunt definite în mod similar cu bucățile PNG, cu diferența fiind că dimensiunea mandrinei este codificată cu un număr variabil de octeți. Numele blocurilor pot avea 4 litere (4 octeți) sau o valoare sub 32, indicând o bucată neopțională.

Următorul este un exemplu de mandrine opționale:

|Nume bucată|Descriere|Conținut (după DEFLATE-decompresie)|
|---|---|---|
|iCCP|profil de culoare ICC|date brute de profil de culoare ICC|
|eXif|Metadate Exif|Antetul „Exif\0\0” urmat de un antet TIFF și datele EXIF|
|eXmp|Metadate XMP|XMP conținut într-un pachet xpacket doar pentru citire, fără umplutură|

### Convenția de denumire ###

- **Prima literă**: majuscule este folosită pentru critici și minuscule este folosită pentru fragmente non-critice.
- **A doua literă**: majuscul este folosit pentru public și minuscul este folosit pentru fragmente private
- **A treia literă**: majuscule este folosită pentru mandrinele necesare pentru afișarea corectă a imaginii, iar literele mici nu sunt importante pentru afișarea imaginii.
- **A patra literă**: majuscule este folosită pentru mandrinele care pot fi copiate în siguranță în orb. Mandrinele cu litere mici depind de datele imaginii.

## Al doilea antet ##

Acesta conține informații cu privire la codificarea efectivă a pixelilor.

|Tip|Descriere|Condiție|Valoare implicită|
|---|---|---|---|
|1 octet|octet NUL (0x00), numele porțiunii unui flux de biți FLIF16||
|uni_int(1,16)|Biți pe pixel ai canalelor|Bpc == '0': repeat(nb_channels)|8 dacă Bpc == '1', 16 dacă Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Numărul de bucle|nb_frames > 1||
|uni_int(0,60_000)|Întârziere cadre în ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flag: are_custom_cutoff_and_alpha|||
|uni_int(1.128)|cutoff|are_custom_cutoff_and_alpha|2|
|uni_int(2.128)|divizor alfa|are_cutoff_personalizat_și_alpha|19|
|uni_int(0,1)|Flag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|are_custom_bitchance||
|variabilă|Transformări (vezi mai jos)|||
|uni_int(1) = 0|Bit indicator: realizat cu transformări|||
|uni_int(0,2)|Predictor de pixeli invizibil|alpha_zero && intercalat && intervalul alfa include zero||

**Canale**

|Număr canal|Descriere|
|---|----|
|0|Roșu sau Gri|
|1|Verde|
|2|Albastru|
|3|Alfa|

**Transformări**

|Tip|Descriere|
|---|---|
|uni_int(1) = 1|bit indicator: încă nu a fost finalizat|
|uni_int(0,13)|Identificator de transformare|
|variabilă|Date de transformare (depinde de transformare)|

Transformarea este folosită pentru a modifica datele pixelilor pentru o compresie mai bună și pentru a ține evidența valorilor pixelilor care apar efectiv.

## Date pixeli ##

Această parte conține datele reale de pixeli codificate folosind codificarea entropiei MANIAC. Pixelii pot fi codificați utilizând codificare intercalată sau neîntrețesată.

### Metoda întrețesut ###

În această metodă, sunt definite nivelurile de zoom. Zoomlevel 0 este folosit pentru imaginea completă, zoomlevel 1 este folosit pentru toate rândurile cu numere pare, zoomlevel 2 este utilizat pentru toate coloanele cu numere pare ale nivelului de zoom 1. Cu alte cuvinte, fiecare nivel de zoom par 2k este o versiune redusă a eșantionului imagine, la scara 1:2^k. Nivelurile de zoom sunt codificate de la cel mai mare la cel mai mic.

### Metoda neîntrețesă ###

În această metodă, codificarea arborilor MANIAC începe imediat urmată de codificarea pixelilor.

## Referințe ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

