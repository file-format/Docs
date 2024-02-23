{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Aflați despre formatul fișierului MCA și despre API-urile care pot crea și deschide fișiere MCA.",
  "title": "MCA - Format de fișier Minecraft Anvil Region",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-roa"
}
},
  "lastmod": "2022-12-13"
}

## Ce este un fișier MCA?

Formatul de fișier Minecraft Anvil region este un format de stocare a datelor care este folosit pentru a stoca bucăți de teren dintr-o Lume Minecraft în popularul joc video **Minecraft**. Lumea Minecraft este formată din regiuni, în care fiecare regiune este împărțită în bucăți. Formatul de fișier MCA permite stocarea eficientă a unor cantități mari de date de joc, cum ar fi locația blocurilor și entităților dintr-o anumită porțiune din lumea jocului. Fișierele MCA trebuie combinate cu alte fișiere MCA pentru a genera o lume întreagă.

Pe lângă stocarea datelor de joc, formatul de fișier Anvil region include și suport pentru diverse alte tipuri de date, cum ar fi datele și metadatele jucătorului. Acest lucru permite stocarea eficientă a tuturor informațiilor necesare pentru a recrea complet o anumită bucată din lumea jocului, inclusiv locația blocurilor, entităților și a altor obiecte de joc.

## Format de fișier MCA - Mai multe informații

Formatul de fișier al regiunii Anvil este o variantă a formatului NBT (Named Binary Tag), care este o structură ierarhică de tip arbore pentru stocarea datelor într-un fișier binar. Acest lucru permite stocarea eficientă a structurilor de date complexe într-un format compact și ușor de citit.

### Bucăți în fișierul MCA

În Minecraft, o bucată este o zonă de bloc de 16x16x16 din lumea jocului care este încărcată în memorie și redată pe ecranul jucătorului. Formatul de fișier Anvil region stochează toate datele pentru o anumită bucată într-un singur fișier, care poate fi apoi încărcat rapid în memorie atunci când este necesar. Acest lucru permite stocarea eficientă și accesul rapid la datele jocului, ceea ce este important pentru a asigura o experiență de joc fluidă și fără întreruperi.

### Dimensiune mică a fișierului MCA

Una dintre caracteristicile cheie ale formatului de fișier al regiunii Anvil este utilizarea compresiei. Acest lucru permite stocarea eficientă a unor cantități mari de date, fără a sacrifica calitatea datelor sau viteza cu care acestea pot fi accesate. Acest lucru se realizează folosind o varietate de tehnici, cum ar fi compresia gzip și compresia de date în bucăți.

Formatul de fișier comprimat al fișierelor MCA îl face o parte importantă a sistemului de stocare și gestionare a datelor din joc. Utilizarea eficientă a compresiei și a suportului pentru diferite tipuri de date permite stocarea eficientă și accesul rapid la datele de joc, asigurând o experiență de joc fluidă și fără întreruperi pentru jucători.

## Structura formatului fișierului MCA

Structura internă a formatelor de fișiere a fișierelor MCA constă din:
 * Antet și a
 * Încărcătură utilă

### Antet MCA

Antetul unui fișier de regiune MCA începe cu un antet de 8 KiB care este împărțit în două tabele de 4 KiB. Primul tabel conține offset-urile bucăților din fișierul regiune în sine, în timp ce al doilea tabel oferă marcaje temporale pentru ultimele actualizări ale acestor bucăți.

### Sarcina utilă MCA

Sarcina utilă MCA constă din bucăți, în care datele pentru fiecare bucată încep cu un câmp (big-endian) de patru octeți. Acest câmp indică lungimea exactă a fragmentelor de date rămase în octeți. Datele ultimei bucăți sunt completate pentru a avea o lungime multiplu de 4096B. Fișierele în care ultima bucată nu este completată nu sunt acceptate de Minecraft.

## Cum să deschideți fișierele MCA

Puteți deschide și edita fișiere MCA folosind programul MCEdit, care este un editor gratuit, open source pentru Minecraft. Puteți să [download MCEdit](https://www.mcedit.net/) de pe site-ul web oficial și să îl utilizați pentru a deschide și vizualiza conținutul fișierului dvs. de regiune Anvil.

După ce ați instalat MCEdit, puteți deschide fișierul pentru regiunea Anvil urmând acești pași:

 1. Porniți MCEdit și faceți clic pe butonul Deschidere” din colțul din stânga sus al ferestrei.

 1. În caseta de dialog Open World”, navigați la locația fișierului pentru regiunea Anvil și selectați-l.

 1. Faceți clic pe butonul Deschidere” pentru a deschide fișierul în MCEdit.

 1. MCEdit va încărca fișierul și va afișa conținutul acestuia în fereastra principală. Apoi puteți utiliza instrumentele și caracteristicile din MCEdit pentru a vizualiza, edita și extrage date din fișierul regiunii Anvil.

## Referințe

* [Editor mondial pentru Minecraft](https://www.mcedit.net/)

* [Despre Minecraft](https://www.minecraft.net/)

* [Format de fișier regiune](https://minecraft.fandom.com/wiki/Region_file_format)


