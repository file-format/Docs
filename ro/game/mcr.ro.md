{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Aflați despre formatul fișierului MCR și despre API-urile care pot crea și deschide fișiere MCR.",
  "title": "MCR - Format de fișier Minecraft Region",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-ror"
}
},
  "lastmod": "2022-12-14"
}

## Ce este un fișier MCR?

Formatul de fișier Minecraft MCR este un format de date folosit de Minecraft pentru a stoca bucăți de teren dintr-o Lume Minecraft. Se bazează pe formatul NBT (Named Binary Tag), care a fost dezvoltat de dezvoltatorii popularului motor de joc open-source, Minecraft Forge. Tipul de fișier MCR a fost introdus la început și a fost înlocuit ulterior cu [MCA file format](/game/mca/).

## Format de fișier MCR

Formatul de fișier MCR este structurat ca o serie de etichete binare denumite, fiecare dintre ele conține un anumit tip de date. Eticheta de nivel superior este eticheta Level”, care conține toate datele pentru un singur nivel de joc. În cadrul etichetei Level, există câteva alte etichete numite care stochează diferite tipuri de date, cum ar fi eticheta Date”, care stochează informații despre lumea jocului și etichetele Entities” și TileEntities”, care stochează date despre obiecte de joc și, respectiv, entități tile din lume.

## Ce se află în formatul fișierului MCR?

În formatul de fișier Minecraft MCR, o regiune este o zonă de bloc de 32x32 din lumea jocului. Formatul MCR împarte lumea jocului în regiuni pentru a gestiona datele mai eficient și pentru a permite încărcarea și salvarea mai rapidă a nivelurilor de joc. Fiecare regiune este stocată într-un fișier separat, iar formatul de fișier MCR utilizează un sistem de coordonate pentru a identifica poziția fiecărei regiuni în lumea jocului. Coordonatele unei regiuni sunt determinate de coordonatele blocului din colțul din stânga jos al regiunii. De exemplu, o regiune cu coordonate (-1,0) ar fi situată o regiune la stânga și zero regiuni în jos de la originea lumii de joc.

## Specificații pentru formatul fișierului MCR

Specificațiile formatului fișierului MCR sunt disponibile publicului. Specificațiile pentru formatul NBT, pe care se bazează formatul MCR, sunt disponibile pe site-ul Minecraft Forge. În plus, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) are și informații detaliate despre formatul fișierului MCR, inclusiv structura acestuia și diferitele tipuri de date pe care le acceptă.

### Date comprimate în fișierele MCR

Formatul de fișier Minecraft MCR acceptă compresia. Formatul de fișier MCR se bazează pe [NBT format](https://minecraft.fandom.com/wiki/NBT_format) care permite stocarea datelor într-o formă comprimată. Acest lucru ajută la reducerea dimensiunii fișierelor MCR și la eficientizarea transferului și stocării acestora. Aceasta este o caracteristică importantă a formatului de fișier MCR, deoarece permite jucătorilor să partajeze date mari de teren Minecraft World cu alții.

## Referințe

* [Editor mondial pentru Minecraft](https://www.mcedit.net/)

* [Despre Minecraft](https://www.minecraft.net/)

* [Format de fișier regiune](https://minecraft.fandom.com/wiki/Region_file_format)

* [Format NBT](https://minecraft.fandom.com/wiki/NBT_format)


