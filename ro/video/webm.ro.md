---
date: 2019-10-11
keywords: WEBM, Ce este un fișier WEBM, WEBM File Format
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Aflați despre formatul de fișier WEBM și despre API-urile care pot crea și deschide fișiere WEBM."
title: WEBM - WebM Video File Format
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Ce este un fișier WEBM?

Un fișier cu extensia .webm este un fișier video bazat pe formatul de fișier WebM deschis, fără drepturi de autor. A fost conceput pentru partajarea video pe web și definește structura containerului de fișiere, inclusiv formatele video și audio. WebM este 100% gratuit, implementând de înaltă calitate bazat pe tehnologii deschise, cum ar fi HTML, HTTP și TCP/IP, care sunt deschise pentru implementare oricui. WebM a fost conceput special pentru a difuza videoclipuri pe web, ceea ce îl face optimizat pentru streaming cu o amprentă de calcul redusă. Acest lucru îl face potrivit pentru redarea videoclipurilor pe orice dispozitiv, în special netbook-uri, handheld-uri și tablete cu putere redusă.

## Format de fișier WEBM

Structura fișierului WebM se bazează pe un subset de format de fișier container Matroska [MKV](/ro/video/mkv/). Fluxurile video disponibile într-un fișier WebM sunt comprimate folosind tehnologiile de compresie VP8 sau VP9 care sunt foarte eficiente în compresie. În mod similar, fluxurile audio dintr-un fișier WebM sunt comprimate folosind codecurile Vorbis sau Opus care au fost dezvoltate de [Xiph Foundation](https://www.xiph.org/). Toate aceste videoclipuri și codecuri audio sunt fără drepturi de autor și pot fi folosite fără nicio taxă.

Următoarele sunt specificațiile rezumate pentru formatul de fișier WebM.

|Câmp|Descriere|
---|---|
|de tip MIME |video/webm|
|Tip MIME numai audio |audio/webm|
|Identificator de tip uniform| org.webmproject.webm|
|Nume codec video| VP8 sau VP9|
|Nume codec audio| Vorbis sau Opus|

### Elemente WebM

WebM, fiind un subset al specificațiilor Matroska, oferă suport pentru unele dintre funcționalitățile Matroska. Mai jos este o descriere a elementelor suportate.

#### EBML

|Nume |Descriere|
---|---|
|EBML|Setați caracteristicile EBML ale datelor de urmat. Fiecare document EBML trebuie să înceapă cu aceasta.|
|EBMLVersion |Versiunea parserului EBML folosită pentru a crea fișierul.|
|EBMLReadVersion|Versiunea minimă de EBML pe care trebuie să o accepte un parser pentru a citi acest fișier.|
|EBMLMaxIDLength |Lungimea maximă a ID-urilor pe care le veți găsi în acest fișier (4 sau mai puțin în Matroska).|
|EBMLMaxSizeLength|Lungimea maximă a dimensiunilor pe care le veți găsi în acest fișier (8 sau mai puțin în Matroska). Aceasta nu anulează dimensiunea elementului indicată la începutul unui element. Elementele care au o dimensiune indicată care este mai mare decât ceea ce este permis de EBMLMaxSizeLength vor fi considerate nevalide.|
|DocType|Un șir care descrie tipul de document care urmează acestui antet EBML ("webm" în cazul nostru).|
|DocTypeVersion|Versiunea interpretorului DocType folosită pentru a crea fișierul.|
|DocTypeReadVersion|Versiunea minimă de DocType pe care trebuie să o accepte un interpret pentru a citi acest fișier.|

#### Elemente globale

Momentan, este suportat doar elementul `Void` care este folosit pentru a anula datele deteriorate, pentru a evita comportamentele neașteptate la utilizarea datelor deteriorate. Conținutul este eliminat. Folosit și pentru a rezerva spațiu într-un subelement pentru utilizare ulterioară.

#### Segment
Acest element conține toate celelalte elemente de nivel superior (nivelul 1). De obicei, un fișier Matroska este compus din 1 segment.

#### Meta Căutare informații

Următoarele informații de căutare sunt acceptate.

|Nume element |Descriere|
---|---|
|SeekHead |Conține poziția altui element de nivel 1.|
|Căutare |Conține o singură intrare de căutare pentru un element EBML.|
|SeekID |ID-ul binar corespunzător numelui elementului.|
|SeekPosition |Poziția elementului în segment în octeți (0 = primul element de nivel 1).|

## Referințe

* [WebM](https://www.webmproject.org/)
* [Arhivele de coduri WebM](https://www.webmproject.org/code/#webp-repositories)

