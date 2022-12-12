{
  "date" : "2019-11-25",
  "keywords" :[ "fișier jpeg", "format fișier jpeg", "ce este un fișier jpeg", "fișier", "exemplu jpeg", "extensie fișier jpeg", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Format fișier imagine",
  "description":"Aflați despre formatul de fișier JPEG și despre API-urile care pot crea și deschide fișiere JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Ce este un fișier JPEG? ##

Un JPEG este un tip de format de imagine care este salvat folosind metoda compresiei cu pierderi. Imaginea de ieșire, ca rezultat al compresiei, este un compromis între dimensiunea stocării și calitatea imaginii. Utilizatorii pot ajusta nivelul de compresie pentru a atinge nivelul de calitate dorit, reducând în același timp dimensiunea de stocare. Calitatea imaginii este afectată neglijabil dacă imaginea este aplicată compresie 10:1. Cu cât valoarea compresiei este mai mare, cu atât este mai mare degradarea calității imaginii.

## Specificații de format de fișier ##

Formatul de fișier imagine JPEG a fost standardizat de Joint Photographic Experts Group și, prin urmare, denumirea JPEG. Formatul a fost alegerea de stocare și transmitere a imaginilor fotografice pe web. Aproape toate sistemele de operare au acum vizualizatoare care acceptă vizualizarea imaginilor JPEG, care sunt adesea stocate și cu extensia JPG. Chiar și browserele web acceptă vizualizarea imaginilor JPEG. Înainte de a intra în specificațiile formatului de fișier JPEG, trebuie menționat procesul general al pașilor implicați în crearea JPEG.

### Pași de compresie JPEG ###

**Transformare:** Imaginile color sunt transformate din RGB într-o imagine de luminanță/crominanță (Ochiul este sensibil la luminanță, nu la crominanță, astfel încât partea de crominanță poate pierde multe date și astfel poate fi foarte comprimată.

**Eșantionarea în jos:** Eșantionarea în jos se face pentru componenta colorată și nu pentru componenta de luminanță. Eșantionarea în jos se face fie într-un raport de 2:1 pe orizontală și 1:1 pe verticală (2h 1 V). Astfel, imaginea se reduce în dimensiune, deoarece componenta „y” nu este atinsă, nu există o pierdere vizibilă a calității imaginii.

**Organizarea în grupuri:** Pixelii fiecărei componente de culoare sunt organizați în grupuri de 8×2 pixeli numite „unități de date” dacă numărul de rânduri sau coloane nu este un multiplu de 8, rândul de jos și coloanele din dreapta sunt duplicate.

**Transformarea cosinusului discret:** Transformarea cosinusului discret (DCT) este apoi aplicată fiecărei unități de date pentru a crea o hartă 8×8 a componentelor transformate. DCT implică o anumită pierdere de informații din cauza preciziei limitate a aritmeticii computerizate. Aceasta înseamnă că chiar și fără hartă va exista o oarecare pierdere a calității imaginii, dar este în mod normal mică.

**Cuantificare:** Fiecare dintre cele 64 de componente transformate din unitatea de date este împărțită la un număr separat numit „Coeficientul de cuantizare (QC)” și apoi rotunjită la un număr întreg. Aici informațiile se pierd iremediabil, QC mare provoacă mai multe pierderi. În general, cele mai multe implementări JPEG permit utilizarea tabelelor QC recomandate de standardul JPEG.

**Codificare:** Cei 64 de coeficienți transformați cuantificați (care sunt acum numere întregi) ai fiecărei unități de date sunt codificați folosind o combinație de codare RLE și Huffman.

**Adăugarea antetului:** Ultimul pas adaugă antetul și toți parametrii JPEG folosiți și scoate rezultatul.

Decodorul JPEG folosește pașii în sens invers pentru a genera imaginea originală din cea comprimată.

### Structura fișierului ###

O imagine JPEG este reprezentată ca o secvență de segmente în care fiecare segment începe cu un marcator. Fiecare marker începe cu 0xFF octet urmat de marcator pentru a reprezenta tipul de marker. Sarcina utilă urmată de marker este diferită în funcție de tipul de marker. Tipurile obișnuite de marcare JPEG sunt enumerate mai jos:

|Scurt Nume|Bytes|Payload|Nume|Comentarii
---|---|---|---|---|
|SOI|0xFF, 0xD8|niciuna|Începutul imaginii|
|S0F0|0xFF, 0xC0|dimensiune variabilă|Începutul cadrului|
|S0F2|0xFF, 0xC2|dimensiune variabilă|Start fo Frame|
|DHT|0xFF, 0xC4|dimensiune variabilă|Definește tabelele Huffman|
|DQT|0xFF, 0xDB|dimensiune variabilă|Definiți tabel(e) de cuantizare|
|DRI|0xFF, 0xDD|4 octeți|Definiți intervalul de repornire|
|SOS|0xFF, 0xDA|dimensiune variabilă|Start of Scan|
|RSTn|0xFF, 0xD//n//(/ro//n//#0..7)|niciuna|Reporniți|
|APPn|0xFF, 0xE//n//|dimensiune variabilă|specific aplicației|
|COM|0xFF, 0xFE|dimensiune variabilă|Comentariu|
|EOI|0xFF, 0xD9|niciuna|Sfârșitul imaginii|

În cadrul datelor codificate cu entropie, după orice octet 0xFF, un octet 0x00 este inserat de codificator înainte de următorul octet, astfel încât să nu pară să existe un marker unde nu este intenționat niciunul, prevenind erorile de încadrare. Decodoarele trebuie să omite acest octet 0x00. Această tehnică, numită [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (vezi secțiunea de specificații JPEG F.1.2.3), este aplicată numai datelor codificate cu entropie, nu și datelor de marcare a sarcinii utile . Rețineți totuși că datele codificate cu entropie au câțiva markeri proprii; în special markerii de resetare (0xD0 prin 0xD7), care sunt utilizați pentru a izola bucăți independente de date codificate cu entropie pentru a permite decodarea paralelă, iar codificatorii sunt liberi să introducă acești markeri de resetare la intervale regulate (deși nu toți codificatorii fac acest lucru).

