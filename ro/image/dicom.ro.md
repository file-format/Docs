{
  "date" : "2019-10-11",
  "keywords" :[ "fișier dicom", "format fișier dicom", "ce este un fișier dicom", "fișier", "exemplu dicom", "extensie fișier dicom", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Format de fișier pentru imagini și comunicații digitale",
  "description":"Aflați despre formatul de fișier DICOM și despre API-urile care pot crea și deschide fișiere DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DICOM?

DICOM este acronimul pentru imagistica digitală și comunicații în medicină și se referă la domeniul informaticii medicale. DICOM este utilizat pentru integrarea dispozitivelor de imagistică medicală, cum ar fi imprimante, servere, scanere etc. de la diverși furnizori și, de asemenea, conține date de identificare ale fiecărui pacient pentru unicitate. Fișierele DICOM pot fi partajate între două părți dacă acestea sunt capabile să primească date de imagine în format DICOM. Partea de comunicare a DICOM este protocolul de nivel de aplicație și utilizează TCP/IP pentru a comunica între entități. Versiunile acceptate de serviciile web sunt 1.0, 1.1, 2 sau mai recente.

## Istorie ##

DICOM a fost dezvoltat în comun de American College of Radiology (ACR) și National Electrical Manufacturers Association (NEMA) pentru schimbul și vizualizarea de imagini medicale, cum ar fi RMN-uri, scanări CT și imagini cu ultrasunete. Inițial, a fost greu să decodezi imaginile pe care le produceau mașinile. Prin urmare, ACR și NEMA au format împreună o echipă în 1983, care a lansat primul său standard, ACR/NEMA 300 în 1985. A doua versiune a fost lansată în 1988, care a fost mai populară în rândul vânzătorilor, dar în curând s-a realizat că a doua versiune are nevoie și de îmbunătățire. A treia versiune a standardului a fost lansată în 1993 ca „DICOM”. 3.0 este încă cea mai recentă versiune, dar a fost actualizată continuu din 1993.

## Format fișier DICOM ##

DICOM este o combinație între definirea formatului de fișier și un protocol de comunicații în rețea. DICOM folosește extensia .DCM. .DCM există în două formate diferite, adică formatul 1.x și formatul 2.x. Formatul DCM 1.x este disponibil și în două versiuni normală și extinsă. Protocoalele HTTP și HTTPS sunt utilizate pentru serviciile web ale DICOM.

### Antet fișier ###

Antetul fișierului conține preambul de fișier de 128 de octeți și prefix DICOM de 4 octeți.

**Preambul # 128 de octeți**|**Prefixul # 4 octeți „D, I, C, M**

**Preambul** este utilizat pentru a accesa imaginile și alte date din fișierul DICOM, oferind compatibilitate cu formatele de fișiere imagine utilizate în mod obișnuit.

**Prefixul** conține șirul „DICM” ca caractere majuscule.

### Set de date ###

Fiecare fișier trebuie să conțină un singur set de date reprezentând instanța SOP și clasa SOP cu IOD aferent. Setul de date este reprezentarea informațiilor din lumea reală. Setul de date conține elemente de date, iar elementele de date conțin valori ale atributelor acelui obiect. Structura atributelor este specificată în IOD. Un obiect de date DICOM constă dintr-un număr de atribute, inclusiv elemente precum numele, ID-ul etc., precum și un atribut special care conține datele pixelilor imaginii.

### Elemente de date ###

Elementul de date este format din elementul de date Tag, lungimea valorii și valoarea pentru elementul de date. Există 5 tipuri de elemente de date și anume elemente de date obligatorii de tip 1, elemente de date condiționate de tip 1C, elemente de date obligatorii de tip 2, elemente de date condiționate de tip 2C și elemente de date opționale de tip 3. De bază Trei tipuri de structuri ale elementelor de date sunt după cum urmează.

**Element de date cu un VR explicit**

|Numărul grupului|Numărul elementului|Reprezentarea valorii|Rezervat|Lungimea valorii|Câmpul valorii
---|---|---|---|---|---|
|2 octeți|2 octeți|2 octeți|2 octeți # 0x00, 0x00|4 octeți|„Lungimea valorii octeți”

**Element de date cu un VR explicit**

|Numărul grupului|Numărul elementului|Reprezentarea valorii|Lungimea valorii|Câmpul valorii
---|---|---|---|---|
|2 octeți|2 octeți|2 octeți|2 octeți|„Lungimea valorii octeți”

**Element de date cu un VR implicit**


|Numărul grupului|Numărul elementului|Lungimea valorii|Câmpul valorii
---|---|---|---|
|2 octeți|2 octeți|4 octeți|„Lungimea valorii octeți”

1. **Etichetă element de date**: un număr întreg ordonat care reprezintă numărul grupului și numărul elementului
1. **Reprezentarea valorii VR**: VR este un șir de caractere care reprezintă VR-ul elementului de date.
1. **Lungimea valorii**: este un întreg fără semn care reprezintă lungimea explicită a câmpului de valoare.
1. **Câmp de valoare**: Descrie valorile elementelor de date.

## Transfer Syntax ##

Sintaxa de transfer este un set de reguli pentru codificare pentru a reprezenta fără ambiguitate sintaxe mai abstracte. Cu ajutorul sintaxei de transfer, entitățile care comunică negociază tehnicile comune de codare pe care le suportă.

## SOP-uri ##

Unirea IOD și DIMSE definește o clasă SOP. Definiția SOP Class conține regulile și semantica care pot restricționa utilizarea serviciilor din Grupul de servicii DIMSE sau Atributele IOD. Exemple de Elemente de serviciu sunt Store, Get, Find, Move etc. Exemple de obiecte sunt imagini CT, imagini MR, dar includ și liste de programare, cozi de imprimare etc.

## Servicii ##

DICOM oferă diverse servicii, în principal legate de comunicarea datelor. Fiecare dintre ele este descris pe scurt mai jos:


**Store:** Serviciul DICOM Store trimite imagini sau alte obiecte către un sistem de arhivare și comunicare a imaginilor (PACS) sau un server.


**Angajament de stocare:** Serviciul de angajament de stocare este utilizat pentru confirmarea faptului că o imagine a fost stocată permanent pe dispozitiv pe orice tip de suport.


**Interogare/preluare:** Acest serviciu permite unei stații de lucru să găsească listele de imagini sau alte obiecte și apoi să le preia din PACS.


**Lista de lucru pentru modalități:** Serviciul pentru lista de lucru pentru modalități oferă o listă a procedurilor de imagistică care au fost programate pentru a fi executate de un dispozitiv de achiziție de imagini.


**Imprimare:** Acest serviciu trimite imagini la imprimantă.

## Numere de port prin IP ##

DICOM utilizează următoarele porturi TCP și UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Referințe ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

