---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ faila veidlapaat
linktitle: ARJ
description: Lnopelniet par ARJ faila formātu un API, kas var izveidot un atvērt ARJ failus.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Kas ir ARJ fails? ##

ARJ (arhivējis Roberts Jungs) ir augstas efektivitātes saspiests arhīva fails, ko izstrādājis Roberts K. Jungs. ARJ tika izstrādāts DOS un agrīnām Windows versijām deviņdesmito gadu sākumā. ARJ faili ir noderīgi, lai dublētu vai koplietotu lielu skaitu failu, jo jums nav jāseko līdzi visiem šiem failiem un ir jāapstrādā tikai viens fails. ARJ arhīva failiem tiek izmantots paplašinājums .arj.

## ARJ faila formāts ##

ARJ failā ir divu veidu galvenes:

- Galvenā galvene: arhīva sākumā ir viena galvenā galvene.
- Lokālās galvenes: vietējās galvenes ir pirms katra faila.

|Nobīde|Tips|Skaits|Apraksts|
|---|---|---|---|
|0000h|word|1|ID=0EA60h|
|0002h|vārds|1|galvenes pamatizmērs|
|0004h|baits|1|Galvenes izmērs|
|0005h|baits|1|Arhīva versijas numurs|
|0006h|baits|1|Nepieciešams minimālais versijas numurs|
|0007h|baits|1|Resursdatora OS:</br> 0 — MS-DOS</br> 1 - PRIMOS</br> 2 — UNIX</br> 3 - AMIGA</br> 4 — MAC-OS (System xx)</br> 5 — OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - NĀKAMAIS</br> 9 - VAX VMS|
|0008h|baits|1|Iekšējie karodziņi, bitkarte:</br> 0 - nav paroles / paroles</br> 1 - rezervēts</br> 2 - fails turpinās nākamajā diskā</br> 3 - ir pieejams faila sākuma pozīcijas lauks</br> 4 ceļu tulkojums ( \ uz / )|
|0009h|baits|1|Saspiešanas metode:</br> 0 - saglabāts</br> 1 - saspiests visvairāk</br> 2 - saspiests</br> 3 - saspiests ātrāk</br> 4 - saspiests visātrāk|
|000Ah|baits|1|Faila tips:</br> 0 - binārs</br> 1–7 bitu teksts</br> 2 — komentāra galvene</br> 3 - direktorijs</br> 4 - sējuma etiķete|
|000Bh|baits|1|rezervēts|
|000Ch|dword|1|Sākotnējā faila datums/laiks MS-DOS formātā|
|0010h|dword|1|Saspiestā faila lielums|
|0014h|dword|1|Sākotnējā faila lielums|
|0018h|dword|1|oriģinālā faila CRC-32|
|001Ah|word|1|Faila specifikācijas pozīcija faila nosaukumā|
|001Ch|word|1|Faila atribūti|
|001Eh|word|1|Resursdatora dati|
|?|dword|1|Paplašināta faila sākuma pozīcija|
|????h|dword|1|CRC-32 no pamata galvenes|
|????h|word|1|Pirmās paplašinātās galvenes izmērs|
|????h+SIZ+2|dword|1|CRC-32 no paplašinātās galvenes|
|????h+SIZ+6|baits|?|Saspiests fails|

## Atsauces Nr.

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

