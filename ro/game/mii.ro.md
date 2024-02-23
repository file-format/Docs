{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier MGX Age of Empires 2 Expansion Replay și despre API-urile care pot crea și deschide fișiere MGX.",
  "title" : "Fișier MII - Wii Virtual Avatar File Format",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-ro",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Ce este un fișier MII?

Un fișier MII este un format de fișier avatar virtual folosit pentru a stoca avatare virtuale pe consola de jocuri Nintendo Wii. Aceste fișiere conțin informații precum aspectul, mișcările și animațiile avatarului. Acestea pot fi folosite în jocuri, aplicații de rețele sociale și alte programe software de pe Wii. Un fișier MII conține și alte caracteristici despre avatar, cum ar fi sexul, culoarea părului, culoarea pielii, trăsăturile feței și tipul de ochi.

Puteți deschide un fișier MII utilizând [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Format de fișier MII

Formatul fișierului MII este definit în detaliu pe [Wii Brew](https://wiibrew.org/wiki/Mii_data). Șirurile dintr-un fișier MII sunt stocate în format Unicode (UTF-16), big-endian.

### Bloc MI

Datele fișierului MII sunt stocate pe Wiimote în două blocuri. Fiecare bloc are 750 de octeți lungime, cu 2 octeți CRC, ceea ce îl face un total de 752 de octeți. Fiecare bloc începe cu o valoare de 4 octeți (RNCD”) care pare a fi numărul magic pentru formatul de fișier MII.

## Cum se creează fișiere MII?

Există câteva moduri diferite de a crea avatare pentru Nintendo Wii:

1. `Folosirea canalului Mii încorporat pe Wii:` Acest canal vă permite să creați avatare personalizate folosind o varietate de instrumente, inclusiv trăsături faciale, forma corpului și îmbrăcăminte. După ce ți-ai creat avatarul, îl poți salva ca fișier Mii și îl poți folosi în jocuri și alte programe software de pe Wii.

1. `Folosirea aplicației Mii Maker pe Nintendo 3DS:` Aplicația Mii Maker vă permite să creați avatare personalizate folosind ecranul tactil și camera de pe Nintendo 3DS. După ce ți-ai creat avatarul, îl poți salva ca fișier Mii și îl poți transfera pe Wii printr-o conexiune wireless.

1. `Folosirea de software terță parte:` Unii dezvoltatori au creat software care vă permite să creați avatare personalizate pentru Wii. Acest software este de obicei conceput pentru a fi utilizat pe un computer și poate necesita pași suplimentari pentru a transfera avatarul pe Wii.

1. Folosirea avatarelor prefabricate:” Unele jocuri și alte programe software de pe Wii pot veni cu avatare prefabricate pe care le puteți utiliza.

În toate cazurile, trebuie să aveți un cont Nintendo pentru a vă crea și salva avatarul pe Wii.

## Referințe

* [Editorul meu avatar](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


