{
  "date" : "2021-10-20",
  "keywords" :[ "fișier sfar", "format fișier sfar", "ce este un fișier sfar", "fișier", "exemplu sfar", "Extensie fișier DLC Mass Effect 3", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier SFAR Mass Effect 3 și despre API-urile care pot crea și deschide fișiere SFAR.",
  "title" :"SFAR - Fișier DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Ce este un fișier SFAR?

Un fișier cu extensia .sfar este un fișier de date de joc folosit de Mass Effect 3 pentru a-și stoca DLC (conținut descărcabil) într-o arhivă comprimată, proprietară. Mass Effect 3 este un joc creat de Electronic Arts, o companie de premieră în dezvoltare de jocuri. Conținutul DLC stocat într-un fișier SFAR este folosit pentru a extinde jocul cu conținut și caracteristici suplimentare.

## Format de fișier SFAR - Mai multe informații

Fișierele SFAR sunt stocate/salvate ca fișiere de arhivă comprimate în format de fișier binar. Acestea folosesc atât algoritmi de compresie LZX, cât și LZMA pentru comprimarea conținutului. Fișierele SFAR pot fi deschise utilizând Editorul DLC care vine în pachet cu ME3 Explorer. Pe lângă SFAR, Editorul DLC poate extrage și alte fișiere de joc, cum ar fi [PCC](/ro/game/pcc/).

## Specificații de format de fișier SFAR

Un fișier SFAR este împărțit în următoarele patru bucăți principale.

### Antet SFAR

Antetul SFF conține informații despre diferitele bucăți care compun fișierul.

### Tabel de fișiere SFAR

Tabelul de fișiere SFAR conține o listă de intrări de fișier în care fiecare intrare are o lungime de 30 de octeți.

### Tabel de dimensiuni bloc

Dimensiunea blocului conține mai multe intrări, unde fiecare intrare are o lungime de 2 byes. Această valoare specifică dimensiunea blocului corespunzătoare unei intrări din tabelul de fișiere.

### Blocuri

Blocurile de bloc dintr-un fișier SFAR conțin datele din fișierul SFAR.

## Referințe

* [Format de fișier DLC SFAR - Cercetare](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

