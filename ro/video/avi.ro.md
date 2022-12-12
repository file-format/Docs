{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Compressed Audio Video", "Fișier", "Extensie", "File Format", "Multimedia Container", "XVid", "DivX", "Codec-uri", "Resource Interchange File Format", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier AVI - Un fișier audio-video intercalat",
  "description":"Aflați despre formatul de fișier AVI și despre API-urile care pot crea și deschide fișiere AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier AVI? ##

Formatul de fișier **AVI** este un format de fișier container multimedia Audio Video care a fost introdus de Microsoft. Deține datele audio și video create și comprimate folosind mai multe codecuri (Codificatoare/Decodificatoare), cum ar fi **XVid** și **DivX**. Deoarece pot fi utilizate diferite codecuri pentru a codifica conținutul AVI, aplicațiile de preluare, adică playerele AVI, ar trebui să le poată deschide numai dacă au instalate codecurile necesare cu care a fost creat conținutul AVI. Formatul este acceptat implicit pe toate platformele **Microsoft Windows**, precum și pe aproape toate celelalte platforme majore. Mai multe aplicații și API-uri oferă capacitatea de a crea/salva, citi și converti AVI în alte formate populare, cum ar fi MP4, MOV, WMV etc.

## Format de fișier AVI ##

Un fișier cu extensia .avi este un fișier AVI. Este un sub-format al formatului de fișier de schimb de resurse (RIFF). RIFF organizează datele în blocuri, sau „bucăți”, care sunt identificate cu o etichetă FourCC. Un fișier AVI este pur și simplu o „buncătură” într-un fișier formatat RIFF.

În prima sub-porțiune, antetul fișierului este identificat prin eticheta „hdrl”; conținutul său include lățimea, înălțimea și rata de cadre ale videoclipului. În a doua sub-porțiune, eticheta de mișcare reprezintă rata de cadre a videoclipului. Videoclipul AVI este format din datele audio/vizuale reale din această bucată. Există, de asemenea, o a treia subporțiune opțională cu eticheta „idx1”, care indică poziția în fișier a bucăților de date individuale care aparțin fișierului.

### Limitări ###

* Informațiile despre raportul de aspect nu pot fi codificate în specificația originală AVI, deși specificația ulterioară OpenDML (AVI 2.0) oferă o metodă standardizată
* Deși fișierele AVI sunt utilizate pe scară largă în post-producția de film și televiziune, diferite abordări pentru adăugarea unui cod de timp la acestea concurează, afectând capacitatea de utilizare a formatului.
* Un fișier video codificat în AVI nu poate utiliza o tehnică de compresie care necesită date viitoare ale cadrelor dincolo de cadrul care este codat (cadru B)
* Este problematic să utilizați fișiere AVI cu rate de biți variabile (VBR) (cum ar fi audio MP3 la rate de eșantionare sub 32 kHz)
* Un fișier AVI care codifică filme de lung metraj cu definiție standard, așa cum este utilizat în mod obișnuit, este probabil să genereze o supraîncărcare de aproximativ 5 MB pe oră, în funcție de modul în care este utilizat fișierul
* Subtitrările trebuie să fie codificate hard în fluxul video sau distribuite într-un fișier separat în cazul în care fișierele AVI nu pot găzdui atașamente, cum ar fi fonturile și subtitrările

## Scurt istoric ##

AVI a fost introdus de Microsoft în 1992 cu scopul de a oferi un format de fișier audio și video mai robust și mai avansat. Formatul a devenit rapid popular odată cu utilizarea internetului, permițând persoanelor să partajeze fișiere video direct și indirect prin stocarea media bazată pe cloud.

## Referințe ##

* [AVI - De Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

