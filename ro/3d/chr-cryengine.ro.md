{
"data":"2023-10-11",
   "keywords":[
"chr",
"fișier chr",
"fișier de caractere chr cryengine",
"cum se deschide un fișier chr",
"fişier",
"extensie fișier chr",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier CHR - Fișier de caractere CryENGINE",
   "description":"Aflați despre formatul de fișier CHR CryENGINE Character și despre API-urile care pot crea și deschide fișiere CHR.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Ce este un fișier CHR?

Fișierul CHR în contextul CryENGINE se referă la un **Fișier de caractere CryENGINE**. CryENGINE este un motor de joc dezvoltat de Crytek și aceste fișiere sunt folosite pentru stocarea modelelor de caractere și a datelor asociate pentru utilizare în jocuri video și alte aplicații în timp real.

## Fișierul de caractere CryENGINE

Un fișier de caractere CryENGINE conține de obicei următoarele componente:

1. **Character Model**: Acesta este modelul 3D al personajului, inclusiv geometria, texturile și animațiile acestuia. Aceste modele sunt adesea create folosind software precum Autodesk Maya sau Blender și apoi importate în CryENGINE.
    




















2. **Date de animație**: CryENGINE acceptă animații complexe pentru personaje, așa că fișierul ".chr" poate include diverse animații, cum ar fi mersul, alergarea, săritul și multe altele. Aceste animații sunt de obicei stocate ca date cheie.
    




















3. **Informații de montaj**: Rigging se referă la procesul de creare a structurii scheletului pentru modelul de caractere, care permite aplicarea animațiilor modelului. Fișierul ".chr" poate conține informații despre ierarhia oaselor și despre modul în care rețeaua personajului este conectată la acest schelet.
    




















4. **Date despre materiale și textură**: informații despre materialele utilizate pe modelul de caractere și hărțile de textura asociate pot fi incluse în fișierul ".chr". CryENGINE acceptă randarea fizică, astfel încât aceste materiale pot fi destul de detaliate.
    




















5. **Date fizice**: Dacă personajul este destinat să interacționeze cu lumea jocului, fișierul ".chr" poate include date fizice, cum ar fi forme de coliziune sau constrângeri pentru fizica ragdoll.
    




















6. **Setări de configurare**: Diverse setări de configurare legate de comportamentul personajului în lumea jocului, cum ar fi comportamentul AI sau evenimentele scriptate, pot face, de asemenea, parte din fișierul ".chr".

## CryENGINE

CryENGINE este un motor de joc puternic dezvoltat de Crytek, compania germană de jocuri video. Este cunoscut pentru capacitățile sale grafice de ultimă oră și a fost folosit pentru a crea jocuri video uimitoare din punct de vedere vizual și avansate din punct de vedere tehnologic. Iată câteva caracteristici și informații cheie despre CryENGINE:

1. **Grafica și randare**: CryENGINE este renumit pentru capabilitățile sale grafice avansate. Acceptă funcții precum iluminarea globală în timp real, iluminarea și umbrele dinamice de înaltă calitate, randarea fizică (PBR) și texturile de înaltă rezoluție. Aceste caracteristici contribuie la crearea unor lumi de joc uimitoare și realiste din punct de vedere vizual.
    




















2. **Physics Engine**: CryENGINE include un motor fizic încorporat care permite interacțiuni realiste între obiecte din lumea jocului. Acceptă funcții precum fizica corpului rigid, fizica corpului moale și fizica ragdoll, făcându-l potrivit pentru crearea de medii dinamice și imersive.
    




















3. **Teren și vegetație**: CryENGINE oferă instrumente pentru crearea unor medii exterioare vaste și detaliate. Acceptă editarea terenului, plasarea vegetației și sistemele meteorologice dinamice, permițând dezvoltatorilor să creeze setări exterioare expansive și realiste.
    




















4. **Animarea personajelor**: CryENGINE include instrumente robuste pentru animarea personajelor. Suportă platforme complexe de caractere, animație facială și sistem de arbore de amestec care le permite dezvoltatorilor să creeze mișcări și animații realiste ale personajelor.
    




















5. **Sistem AI**: Motorul dispune de un sistem AI care permite crearea de NPC-uri inteligente (personaje non-jucatoare) și AI inamic. Dezvoltatorii pot scrie comportamentul și interacțiunile AI pentru a crea experiențe de joc provocatoare și captivante.
       





















6. **Scriptare**: CryENGINE folosește un limbaj de scripting numit "Schematyc", care permite dezvoltatorilor să creeze logica de joc și interacțiuni. În plus, acceptă C++ pentru nevoi de programare mai avansate.

## Formate de fișiere utilizate de CryENGINE

Iată câteva dintre tipurile de fișiere comune asociate cu CryENGINE:

1. **cryproj**: fișiere de proiect CryENGINE. Aceste fișiere stochează setări și configurații specifice proiectului pentru un anumit proiect de joc.
    




















2. **.level**: fișierele de nivel conțin date 3D despre lumea jocului, inclusiv teren, obiecte, iluminare și alte setări specifice nivelului. Nivelurile sunt o componentă fundamentală a designului jocului în CryENGINE.
    




















3. **.cgf**: Character Geometry Format. Aceste fișiere conțin date de model 3D pentru personaje, obiecte și alte active ale jocului. Fișierele CGF pot include geometrie, texturi și date de animație.
    




















4. **.chrparams**: Fișiere cu parametrii caracterului. Aceste fișiere stochează setări și configurații pentru modelele de personaje și animațiile acestora.
    




















5. **.dds**: Format Texture DirectX. CryENGINE utilizează de obicei fișiere DDS pentru a stoca texturi, inclusiv hărți difuze, hărți normale și alte tipuri de texturi.
    




















6. **.cryshader**: fișiere CryENGINE Shader. Aceste fișiere definesc modul în care materialele și obiectele sunt redate în lumea jocului, specificând shaders, proprietățile materialelor și multe altele.
    




















7. **.crytif**: Fișier de informații privind textura. Aceste fișiere stochează informații suplimentare despre texturi, cum ar fi setările de compresie, mipmap-urile și alte detalii legate de texturi.
    




















8. **.cdf**: Fișier de definire a caracterelor. Fișierele CDF sunt folosite pentru a defini elementele de caractere și proprietățile acestora, inclusiv atașamente, stări de animație și setări legate de caractere.
    




















9. **.dds**: CryENGINE folosește și fișiere DDS (DirectDraw Surface) pentru diferite hărți de textură, cum ar fi hărți normale, hărți speculare și hărți difuze.
    




















10. **.anim**: Fișiere de animație. Aceste fișiere stochează date de animație pentru personaje și obiecte, inclusiv cadre cheie, poziții osoase și secvențe de animație.
    




















11. **.xml**: fișierele XML pot fi utilizate pentru diferite configurații și definiții de date în CryENGINE, cum ar fi logica jocului, comportamentul AI și multe altele.
    




















12. **.pak**: [Fișiere PAK](/ro/game/pak/) sunt fișiere de arhivă utilizate pentru a împacheta activele și resursele jocului, făcându-l mai eficient pentru distribuirea și încărcarea jocului.

## Cum se deschide fișierul CHR?

Programele care deschid fișierele CHR includ

- **Crytek CryENGINE SDK** (probă gratuită) pentru Windows

**SubTip:** Fișiere de imagine 3D

## Alte dosare CHR

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.chr**.

**3D**
- [CHR - CryENGINE Character File](/ro/3d/chr-cryengine/)
- [CHR - Fișier cu caractere 3ds Max](/ro/3d/chr-3ds/)

**Font și joc**
- [CHR - Set de caractere Borland](/ro/font/chr/)
- [CHR - Clubul de literatură Doki Doki! Fișier de caractere](/ro/game/chr-doki/)

## Referințe
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

