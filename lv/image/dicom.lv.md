{
  "date": "2019-10-11",
  "keywords": [
"dicom fails",
"dicom faila formātā",
"kas ir dicom fails",
"failu",
"dicom piemērs",
"dicom faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM — digitālās attēlveidošanas un sakaru faila formāts",
  "description": "Uzziniet par DICOM faila formātu un API, kas var izveidot un atvērt DICOM failus.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-lvm"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DICOM fails?

DICOM ir digitālās attēlveidošanas un sakaru saīsinājums medicīnā un attiecas uz medicīnas informātikas jomu. DICOM tiek izmantots dažādu pārdevēju medicīniskās attēlveidošanas ierīču, piemēram, printeru, serveru, skeneru utt., integrācijai, un tajā ir arī katra pacienta identifikācijas dati, lai nodrošinātu unikalitāti. DICOM failus var koplietot starp divām pusēm, ja tās spēj saņemt attēlu datus DICOM formātā. DICOM komunikācijas daļa ir lietojumprogrammas slāņa protokols un izmanto TCP/IP, lai sazinātos starp entītijām. Tīmekļa pakalpojumu atbalstītās versijas ir 1.0, 1.1, 2 vai jaunākas versijas.

## Vēsture ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. Otrā versija tika izlaista 1988. gadā, kas bija populārāka pārdevēju vidū, taču drīz vien tika saprasts, ka arī otrajai versijai ir nepieciešami uzlabojumi. Standarta 3. versija tika izlaista 1993. gadā kā DICOM. 3.0 joprojām ir jaunākā versija, taču tā ir nepārtraukti atjaunināta kopš 1993. gada.

## DICOM faila formāts ##

DICOM ir faila formāta definīcijas un tīkla sakaru protokola kombinācija. DICOM izmanto paplašinājumu .DCM. .DCM pastāv divos dažādos formātos, ti, formātā 1.x un formātā 2.x. DCM Format 1.x ir pieejams arī divās versijās - parastajā un paplašinātajā. DICOM tīmekļa pakalpojumiem tiek izmantoti HTTP un HTTPS protokoli.

### Faila galvene ###

Faila galvenē ir 128 baitu faila preambula un 4 baitu DICOM prefikss.

**Preambula # 128 baiti**|**Prefikss # 4 baiti D, I, C, M**

**Preambula** tiek izmantota, lai piekļūtu attēliem un citiem datiem DICOM failā, nodrošinot saderību ar bieži lietotiem attēlu failu formātiem.

**Prefikss** satur virkni DICM kā lielos burtus.

### Datu kopa ###

Katrā failā ir jāietver viena datu kopa, kas pārstāv SOP gadījumu un SOP klasi ar saistīto IOD. Datu kopa ir reālās pasaules informācijas attēlojums. Datu kopa satur datu elementus, un datu elementi satur šī objekta atribūtu vērtības. Atribūtu struktūra ir norādīta IOD. DICOM datu objekts sastāv no vairākiem atribūtiem, tostarp tādiem vienumiem kā nosaukums, ID utt., kā arī viens īpašs atribūts, kas satur attēla pikseļu datus.

### Datu elementi ###

Datu elements sastāv no datu elementa Tag, Vērtības garuma un datu elementa vērtības. Ir 5 veidu datu elementi, proti, 1. tipa obligātie datu elementi, 1. C tipa nosacījuma datu elementi, 2. tipa obligātie datu elementi, 2. tipa nosacījuma datu elementi un 3. tipa neobligātie datu elementi. Pamata Trīs datu elementu struktūru veidi ir šādi.

**Datu elements ar nepārprotamu VR**

|Grupas numurs|Elementa numurs|Vērtības attēlojums|Rezervēts|Vērtības garums|Vērtības lauks
---|---|---|---|---|---|
|2 baiti|2 baiti|2 baiti|2 baiti # 0x00, 0x00|4 baiti|vērtības garuma baiti

**Datu elements ar nepārprotamu VR**

|Grupas numurs|Elementa numurs|Vērtības attēlojums|Vērtības garums|Vērtības lauks
---|---|---|---|---|
|2 baiti|2 baiti|2 baiti|2 baiti|vērtības garuma baiti

**Datu elements ar netiešu VR**


|Grupas numurs|Elementa numurs|Vērtības garums|Vērtības lauks
---|---|---|---|
|2 baiti|2 baiti|4 baiti|vērtības garuma baiti

1. **Datu elementa tags**: sakārtots vesels skaitlis, kas apzīmē grupas numuru un elementa numuru
1. **Vērtību reprezentācijas VR**: VR ir rakstzīmju virkne, kas attēlo datu elementa VR.
1. **Vērtības garums**: vai neparakstīts vesels skaitlis ir precīzs vērtības lauka garums.
1. **Vērtības lauks**: apraksta datu elementu vērtības.

## Pārsūtīšanas sintakse ##

Pārsūtīšanas sintakse ir noteikumu kopums kodēšanai, lai nepārprotami attēlotu abstraktākas sintakses. Ar pārsūtīšanas sintakses palīdzību saziņas entītijas vienojas par kopīgām kodēšanas metodēm, kuras tās atbalsta.

## SOP ##

IOD un DIMSE savienība definē SOP klasi. SOP klases definīcija satur noteikumus un semantiku, kas var ierobežot pakalpojumu izmantošanu DIMSE pakalpojumu grupā vai IOD atribūtus. Pakalpojuma elementu piemēri ir Store, Get, Find, Move utt. Objektu piemēri ir CT attēli, MR attēli, kā arī grafiku saraksti, drukas rindas utt.

## Pakalpojumi ##

DICOM sniedz dažādus pakalpojumus, kas galvenokārt saistīti ar datu pārraidi. Katrs no tiem ir īsi aprakstīts zemāk:


**Veikals:** DICOM veikala pakalpojums nosūta attēlus vai citus objektus uz attēlu arhivēšanas un sakaru sistēmu (PACS) vai serveri.


**Uzglabāšanas saistības:** Krātuves saistību pakalpojums tiek izmantots, lai apstiprinātu, ka attēls ir pastāvīgi saglabāts ierīcē jebkura veida datu nesējā.


**Vaicājums/izgūšana:** šis pakalpojums ļauj darbstacijai atrast attēlu vai citu objektu sarakstus un pēc tam izgūt tos no PACS.


**Modalitātes darba saraksts:** modalitātes darba sarakstu pakalpojums sniedz to attēlveidošanas procedūru sarakstu, kuras ir ieplānojušas attēlu iegūšanas ierīcei.


**Drukāt:** Šis pakalpojums sūta attēlus uz printeri.

## Portu numuri, izmantojot IP ##

DICOM izmanto šādus TCP un UDP portus:

1. 104
1. 2761
1. 2762
1. 11112

## Atsauces Nr.

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)


