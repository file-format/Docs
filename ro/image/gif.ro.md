{
  "date" : "2019-10-11",
  "keywords" :[ "fișier gif", "format fișier gif", "ce este un fișier gif", "fișier", "exemplu gif", "extensie fișier gif", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Format fișier imagine",
  "description":"Aflați despre formatul de fișier GIF și despre API-urile care pot crea și deschide fișiere GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GIF? ##

Un GIF sau Graphical Interchange Format este un tip de imagine foarte comprimată. Deținut de Unisys, GIF folosește algoritmul de compresie LZW care nu degradează calitatea imaginii. Pentru fiecare imagine, GIF-ul permite de obicei până la 8 biți pe pixel și sunt permise până la 256 de culori pe imagine. Spre deosebire de o imagine [JPEG](/ro/image/jpeg/), care poate afișa până la 16 milioane de culori și atinge destul de mult limitele ochiului uman. Când a apărut internetul, GIF-urile au rămas cea mai bună alegere, deoarece aveau nevoie de lățime de bandă redusă și compatibile pentru graficele care consumă zone solide de culoare. Un GIF animat combină numeroase imagini sau cadre într-un singur fișier și le afișează într-o secvență pentru a genera un clip animat sau un scurt videoclip. Limitările de culoare sunt de până la 256 pentru fiecare cadru și sunt probabil cele mai puțin potrivite pentru reproducerea altor imagini și fotografii cu gradient de culoare.

## Format fișier GIF ##

Din punct de vedere conceptual, fișierele GIF au o zonă grafică de dimensiune fixă umplută cu zero sau mai multe imagini. Unele fișiere GIF împart zona sau blocurile grafice de dimensiuni fixe în sub-imagini capabile să funcționeze ca cadre animate în cazul GIF animat. Formatul GIF folosește adâncimi de pixeli de 1 până la 8 biți pentru a stoca datele bitmap. Modelul de culori RGB și datele paletei sunt întotdeauna folosite pentru a stoca imaginile. În funcție de versiune, un antet cu lungime fixă ("GIF87a" sau "GIF89a") definește începutul unui fișier GIF tipic.

În prezent, sunt disponibile două versiuni de GIF: 87a și 89a. Primul este formatul GIF original, în timp ce al doilea este noul format GIF. În acest format de fișier, caracteristicile blocurilor și dimensiunile pixelilor sunt menționate într-un descriptor de ecran logic de lungime fixă. Existența și dimensiunea unui tabel global de culori pot fi specificate de descriptorul de ecran, care urmărește detalii suplimentare dacă sunt prezente. Trailer-ul este ultimul octet al fișierului care conține un singur octet de punct și virgulă ASCII. Un aspect tipic de fișier GIF87a este următorul:

### Antet ###

Antetul conține șase octeți și este folosit pentru a specifica tipul de fișier ca GIF. Deși descriptorul de ecran logic este separat de antetul real, totuși, uneori, este considerat al doilea antet. Aceeași structură care este folosită pentru a stoca antetul poate stoca descriptorul de ecran logic. Toate fișierele GIF încep cu semnătura de 3 octeți și utilizează caracterele „GIF” ca identificator. Versiunea are, de asemenea, o dimensiune de trei octeți și declară versiunea fișierului GIF.

### Descriptor de ecran logic ###

Un descriptor de imagine cu lungime fixă specifică ecranul și informațiile de culoare necesare pentru a crea imaginea GIF. Câmpurile Height și Width includ cea mai mică valoare a rezoluției ecranului, obligatorie pentru a afișa datele imaginii. Dacă dispozitivul de afișare nu este capabil să afișeze rezoluția specificată, va fi necesară scalarea pentru a afișa în mod adecvat imaginea. Informațiile pe ecran și pe harta culorilor sunt afișate în cele patru subcâmpuri ale tabelului de mai jos (în timp ce bitul 0 este bitul cel mai puțin semnificativ):


|Biți|Subcâmpuri
---|---|
|0-2|Dimensiunea tabelului global de culori
|3|Pavilion de sortare a tabelului de culori
|4-6|Rezoluție de culoare
|7|Drapeau de masă globală de culori

#### Tabel global de culori ####

Un tabel global de culori opțional este plasat imediat după descriptorul de ecran logic. Acest tabel a fost mapat pentru a indexa datele de culoare a pixelilor din datele imaginii. În absența unui tabel global de culori, fiecare imagine din fișierul GIF își folosește culoarea locală. Este mai bine să furnizați un tabel de culori implicit dacă lipsesc atât Tabelul de culori global, cât și cel local. O serie de triple de trei octeți compun elementele tabelului de culori. Fiecare octet caracterizează o valoare de culoare RGB. Culorile roșu, verde și albastru sunt folosite ca valori ale fiecărui element de tabel de culori. Intrările din Tabelul de culori global ajung la maximum 256 de intrări și reprezintă întotdeauna o putere de două.

#### Date imagine ####

Datele imaginii stochează un octet de simboluri necodificate, urmate de lista legată de sub- împreună cu datele codificate LZW.

#### Remorcă ####

Trailerul reprezintă un singur octet de date care este ultimul caracter din fișier. Valoarea acestui octet este permanent 3Bh și specifică sfârșitul fluxului de date. Fiecare fișier GIF trebuie să aibă trailerul în ultimul fișier.

## Referințe ##

* [Format fișier GIF](https://en.wikipedia.org/wiki/GIF)

