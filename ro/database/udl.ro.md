{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extensie", "fișier udl", "format fișier udl", "Tipul fișierului bazei de date", "Format fișierului bazei de date", "ce este un fișier udl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier UDL și despre API-urile care pot crea și deschide fișiere UDL.",
  "title" :"UDL - Fișier Microsoft Universal Data Link",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Ce este un fișier UDL?
Fișierul cu extensia .udl se numește fișier Microsoft Universal Data Link; specificarea atributelor de conectare; utilizat de aplicațiile Windows pentru a stabili o conexiune cu baza de date. Fișierul UDL conține șirul de conexiune pentru o sursă de date OLE DB; cu nume de utilizator și parolă și proprietăți esențiale ale șirului de conexiune. Pentru a evita specificarea directă manuală a proprietăților într-un șir de conexiune, o casetă de dialog Data Link Properties poate fi folosită pentru a salva informațiile de conectare într-un fișier .udl ca alternativă.

## Format de fișier UDL
Practic, un fișier UDL (Universal Data Link) este un fișier text simplu care constă dintr-un șir de conexiune la baza de date cu anumite atribute sau proprietăți. Odată ce fișierul UDL este creat, acesta poate fi testat utilizând SQL Server Management Studio pentru a verifica conectivitatea.

### Proprietățile șirului de conexiune
Următoarele proprietăți pot fi setate într-un UDL pentru a asigura conectivitatea corespunzătoare:

- **Nume server**: locația serverului în care se află baza de date pe care doriți să o accesați.
- **Opțiuni de autentificare**
- **Autentificare Windows**: Autentificare la SQL Server folosind datele de conectare ale contului Windows al utilizatorului conectat în prezent.
- **SQL Server Authentication**: autentificare folosind ID-ul de conectare și parola.
- **Active Directory - Integrat**: autentificare integrată cu o identitate Azure Active Directory; poate fi folosit și pentru autentificarea Windows la SQL Server.
- **Active Directory - Parolă**: ID utilizator și autentificare cu parolă cu o identitate Azure Active Directory.
- **Active Directory - Universal cu suport MFA**: autentificare interactivă cu o identitate Azure Active Directory.
- **Active Directory - Service Principal**: Autentificare cu un principal de serviciu Azure Active Directory.
- **SPN server**: dacă utilizați o conexiune de încredere, puteți specifica un nume principal de serviciu (SPN) pentru server.
- **Nume utilizator**: introduceți ID-ul de utilizator pe care să îl utilizați pentru autentificare atunci când vă conectați la sursa de date.
- **Parolă**: introduceți parola de utilizat pentru autentificare când vă conectați la sursa de date.
- **Parolă goală**: când este bifată, permite furnizorului specificat să utilizeze o parolă goală în șirul de conexiune.
- **Permite salvarea parolei**: Permite salvarea parolei cu șirul de conexiune.
- **Utilizați criptare puternică pentru date**: datele care sunt transmise prin conexiune vor fi criptate.
- **Certificat server de încredere**: certificatul serverului va fi validat.
- **Bază de date**: numele bazei de date pe care doriți să o accesați.
- **Atașați un fișier de bază de date ca nume de bază de date**: Specifică numele fișierului principal pentru o bază de date atașabilă.

## Referințe ##

* [Componente de acces la date Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Configurație Universal Data Link (UDL)](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

