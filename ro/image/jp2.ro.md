{
  "date" : "2019-10-11",
  "keywords" :[ "fișier jp2", "format fișier jp2", "ce este un fișier jp2", "fișier", "exemplu jp2", "extensie fișier jp2", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Format fișier imagine",
  "description":"Aflați despre formatul de fișier JP2 și despre API-urile care pot crea și deschide fișiere JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Ce este un fișier JP2? ##

JPEG 2000 (**JP2**) este un sistem de codare a imaginilor și un standard de comprimare a imaginii de ultimă generație. Utilizează tehnologia wavelet pentru a codifica conținut fără pierderi în orice calitate simultan. În plus, fără nicio penalizare substanțială în eficiența codării, JPEG 2000 are capacitatea de a accesa și de a decoda eficient același conținut într-o varietate de alte rezoluții și calități. Fluxurile de cod din JPEG 2000 sunt semnificativ scalabile, având regiuni de interes care oferă facilitatea pentru acces aleatoriu spațial.

JPEG 2000 se remarcă a fi unul dintre cele mai scalabile standard. Diferite părți ale unei imagini pot fi stocate folosind diverse calități. O creștere remarcabilă a performanței poate fi obținută prin ordonarea fluxului de cod într-o varietate de moduri. Cu toate acestea, JP2 necesită codoare/decodore complexe și dificile din punct de vedere computațional, ca rezultat al acestei flexibilități. În comparație cu JPEG, JPEG 2000 produce doar artefacte de sunet care fac inele lângă marginea imaginii și pot fi neclare, în timp ce JPEG utilizează blocuri de artefacte vizuale de 8×8 care pot fi atât artefacte de sunet, cât și de blocare. Posedă până la 16384 de componente diverse cu dimensiunile terapixelilor și o precizie care poate fi de până la 38 de biți/probă.

## Istorie ##

În 2000, comitetul Joint Photographic Experts Group a proiectat JP2 cu obiectivul de a-și îmbunătăți propriul standard JPEG bazat pe transformarea cosinusului discret cu această nouă metodă bazată pe wavelet. Comitetul JPEG și-a propus să ofere metodele de bază fără taxe de licență. în licența JP2, câștigând concurență între 20 de companii, au câștigat cu o mustață. JPEG 2000 a fost declarat ca standard ISO, deși majoritatea browserelor web nu sunt pregătite să dea o mână de ajutor JPEG 2000 din 2017.

## Componente ale sistemului de codare a imaginilor JPEG 2000 ##

Următoarele sunt principalele părți care constituie suita completă de standarde pentru JPEG 2000.


|Partea|Titlu|Descriere|Număr
---|---|---|---|
|Partea 1|Sistem de codificare de bază| Definește sintaxa fluxului de cod. Diferite etape implicate în decodarea imaginilor JPEG 2000. Explică formatul de bază al fișierului JP2, metadatele și drepturile IP care trebuie furnizate.|ISO/IEC 15444-1
|Partea 2|Extensii|Definește extensiile pentru fluxul de cod în format de fișier și permite demonstrații de eșantionare HDR, specificarea spațiului de culoare, decuparea, transformările geometrice; diverse animații, metadate și fluxuri multiple de coduri.|ISO/IEC 15444-2
|Partea 3|Motion JPEG 2000 (MJ2 sau MJP2)|Introduceți un format de fișier pentru secvențele de mișcare, codând imagini într-un flux de cod independent.|ISO/IEC 15444-3
|Partea 4|Conformitate|Scrie tehnici de testare pentru codificarea și decodificarea și verifică fișierele atât pentru fluxurile de cod bare, cât și pentru fișierele JP2.|ISO/IEC 15444-4
|Partea 5|Software de referință|Constă din două pachete de cod sursă (Java, C) care implementează sistemul de codare Core și sunt disponibile sub licențe open-source.|ISO/IEC 15444-5
|Partea 6|Format de fișier imagine compus|Definește formatul de fișier JPM și permite crearea de imagini a documentelor cu mai multe pagini pentru aplicații de tip fax. Suportă utilizarea JBIG2 și JPEG.|ISO/IEC 15444-6
|Partea 8|JPEG 2000 Securizat (JPSEC)|Asigură securitatea tranzacțiilor, conținutului și tehnologiilor și permite fluxuri securizate JPEG 2000 de biți.|ISO/IEC 15444-8
|Partea 9|JPIP|Definește instrumente într-un mediu de rețea pentru a accesa metadate și imagini și precizează protocoale interactive și eficiente|ISO/IEC 15444-9
|Partea 10|JP3D|Extensie volumetrică a părții 1 și introduce dimensiunea Z. Extinde conceptul de plăci, blocuri de cod, incinte și caracteristici de accesibilitate 3D pentru regiunile de interes.|ISO/IEC 15444-10
|Partea 11|JPWL|Se ocupă de transmisia bine organizată printr-o rețea fără fir predispusă la erori. Această extensie este compatibilă cu decodorele|ISO/IEC 15444-11
|Partea 13|Encoder de nivel de intrare|Definește implementarea unui codificator de nivel de intrare a sistemului de codare de bază.|ISO/IEC 15444-13
|Partea 14|JPXML|O reprezentare în XML și explică segmentele de marcare și metodele de accesare a datelor interne ale imaginilor.|ISO/IEC 15444-14
|Partea 15|HTJ2K (Subdezvoltare)|Specifică un algoritm alternativ de codificare a blocurilor. Algoritmul oferă un randament crescut de zece ori și codare/decodare fără pierderi.|

## Format fișier JP2 ##

JPEG 2000 definește formatul fișierului, precum și fluxul de cod în același mod ca JPEG-1. Deși mostrele de imagine sunt descrise exclusiv de JPEG 2000, totuși JPEG-1 include și alte informații suplimentare despre spațiul de culoare și rezoluția esențială pentru codificarea imaginii. Dacă o imagine este stocată ca fișier JPEG 2000, **.jp2** este folosit ca extensie. Acest format de fișier se îmbunătățește și mai mult prin extensia JPEG 2000 partea 2, care definește mecanismele de animație și configurarea numeroaselor fluxuri de cod într-o singură imagine. Extensia **.jpx** este utilizată când imaginile se salvează folosind acest format de fișier extins. Deoarece datele fluxului de cod nu sunt considerate a fi salvate în principal în fișiere, deci nu este definită nicio extensie standard în acest scop. Deși în scopuri de testare, primește frecvent extensia **.jpc** sau **.j2k**. Spre deosebire de JPEG-1, JPEG 2000 alege un mod diferit de codificare a metadatelor în format XML. Standardul 12234-1.4 (de către comitetul ISO TC42) este folosit ca referință între etichetele Exif și componentele XML. JPEG 2000 poate conține un standard ISO, XMP.

### Bucăți ###
Fișierele JPEG 2000 constau din bucăți consecutive. Fiecare bucată are antet de 8 octeți: dimensiunea fragmentului de 4 octeți (big-endian, octetul mare mai întâi) și tipul de fragment de 4 octeți - una dintre semnăturile predefinite: „jP” sau „jP2”.

A doua bucată trebuie să fie de tip „ftyp” și să aibă un subtip la offset 8. JPEG 2000 definit prin subtip care trebuie să fie una dintre valorile: „jp2” (tip de fișier \*.JP2), „jp20” (fișier tip \*.JPA), "jpm " (tip de fișier \*.JPM), "jpx " (tip de fișier \*.JPX).

Repetând bucăți, până când este detectat tipul necunoscut, compunem fișier imagine/video JPEG 2000.

### Transformarea culorii ###

Inițial, este necesară transformarea imaginilor din spațiul de culoare RGB în alt spațiu de culoare. În acest scop, există două moduri: Transformarea ireversibilă a culorii (ICT) și Transformarea culorii reversibilă (RCT). Fostul folosește spațiul de culoare YC,,B,,C,,R, și trebuie implementat în virgulă fixă/floating, în timp ce mai târziu un spațiu de culoare YUV modificat și de natură reversibilă.// //Nu este limitat la modelul RGB, JPEG Limba 2000 folosește transformarea mai multor componente.

### Tiglare ###

Când se termină transformarea culorii, imaginea se transformă în regiuni dreptunghiulare numite plăci care pot fi transformate și codificate separat. Dimensiunea tuturor plăcilor va avea aceeași, sau întreaga imagine poate fi considerată ca o singură placă. Decoderul beneficiază de avantajul plăcii și consumă mai puțină memorie sau poate codifica parțial unele plăci. Deși această tehnică are un dezavantaj de degradare a calității imaginii.

### Transformarea wavelet ###

Imaginea după placare este transformată prin wavelet care poate fi fie ireversibilă, fie reversibilă și implementată prin utilizarea schemei de convoluție sau de ridicare.

### Rata compresiei ###

În funcție de caracteristicile fizice ale unei imagini, se obține un câștig de compresie de 20% Predicția redundanței spațiale a JPEG 2000 joacă un rol vital în procesul de compresie și imaginile de înaltă rezoluție tind să câștige cel mai mult avantaj.

## Aplicații deservite de standardul ##

* Înregistrarea, editarea și stocarea videoclipurilor HD bazate pe cadre
* Imagini medicale și biometrie
* imagini din satelit, teledetecție și detecție a mișcării
* Comunicare client/server, distribuție și stocare în rețea.
* Cinema digital, contribuție live HDTV, materiale audio-vizuale digitalizate

## Referințe ##

* [Prezentare generală despre JPEG 2000](https://jpeg.org/jpeg2000/)
* [Sistem de codificare a imaginilor JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

