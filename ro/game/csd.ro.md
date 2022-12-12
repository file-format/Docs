{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul și API-urile CSD Steam Game Data Backup File.",
  "title" :"Format fișier CSD - fișier de rezervă a datelor jocului Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Ce este un fișier CSD?

Un fișier CSD este un fișier de rezervă a jocului generat de serviciul de jocuri **Steam** care permite utilizatorilor să descarce și să gestioneze jocuri **Valve**. Conține datele de rezervă legate de jocuri care pot fi folosite pentru a restaura un joc șters. Steam poate să restaureze jocul dintr-un fișier CSD numai dacă jocul a fost descărcat, instalat și corectat prin Steam. Pentru a restabili jocul din fișierul CSD, utilizați opțiunea Steam → Backup and Restore Gamesteam și selectați fișierul.

## Format de fișier CSD - Mai multe informații

Structura internă a formatului de fișier CSD nu este disponibilă public, iar specificațiile sale de format de fișier nu sunt disponibile pentru referință de către dezvoltatori. Fișierele CSD sunt însoțite de fișierele CSM și ISS, care sunt, de asemenea, formate de fișiere de joc Steam.

### Unde să găsești fișierele de rezervă Steam?

Întregul fișier de rezervă Steam poate fi găsit în următoarele locații:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Configurații personalizate și scripturi de configurare
* \downloads\ - Conținut personalizat pentru jocuri multiplayer
* \maps\ - Hărți personalizate care au fost instalate sau descărcate în timpul jocurilor multiplayer
* \materials\ - Texturi și skinuri personalizate
* \SAVE\ - Jocuri salvate pentru un singur jucător

Cu toate acestea, locația jocurilor create de terți poate fi diferită și este determinată de dezvoltatorul jocului.

### Restaurare din fișierul de rezervă CSD

Instalați Steam și conectați-vă la contul Steam corect (consultați Instalarea Steam pentru instrucțiuni suplimentare)
* Lansați Steam
* Faceți clic pe „Steam” în colțul din stânga sus al aplicației Steam
* Selectați „Fă backup și restaurați jocuri...”
* Selectați „Restaurați o copie de rezervă anterioară”
* Navigați la locația fișierelor de rezervă ale jocului
* Continuați prin ferestrele Steam pentru a instala jocurile necesare.

## Referințe

* [Folosirea funcției Steam Backup](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

