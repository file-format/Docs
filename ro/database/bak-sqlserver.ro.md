{
"data": "2023-06-12",
  "keywords": [
"bak",
"fișier bak",
"Copia de rezervă a bazei de date Microsoft SQL Server",
"ce este un fișier bak",
"cum se deschide fișierul bak",
"fişier",
"extensie de fișier bak",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format de fișier BAK - Backup baze de date Microsoft SQL Server",
  "description":"Aflați despre formatul BAK SQL Server Backup și despre API-urile care pot crea și deschide fișiere BAK.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Ce este un fișier BAK?

Un fișier ".bak", în contextul Microsoft SQL Server, este un format de fișier de rezervă utilizat pentru a stoca copii ale unei baze de date SQL Server. Aceste fișiere conțin un instantaneu al bazei de date la un anumit moment în timp, inclusiv schema, datele și alte informații conexe. Acestea sunt generate folosind funcționalitatea de backup și restaurare încorporată a SQL Server și servesc mai multe scopuri cruciale:

1. **Recuperare date:** fișierele .bak oferă un mijloc de a recupera o bază de date în caz de pierdere a datelor, corupție sau alte probleme. Prin restaurarea unei baze de date dintr-un fișier .bak, o puteți reveni la o stare anterioară, minimizând timpul de nefuncționare și pierderea de date.

2. **Migrare și clonare:** Fișierele de rezervă sunt adesea folosite pentru a migra baze de date între servere sau pentru a crea copii ale bazelor de date pentru testare, dezvoltare sau raportare. Ele oferă o modalitate consistentă și eficientă de a muta bazele de date între medii.

3. **Recuperare punct-in-time:** SQL Server vă permite să efectuați recuperarea punct-in-time folosind fișiere .bak. Aceasta înseamnă că puteți restaura o bază de date într-un anumit moment din timp, ceea ce poate fi crucial pentru conformitatea cu reglementările sau pentru auditarea datelor.

4. **Recuperare în caz de dezastru:** fișierele .bak sunt o parte critică a planificării recuperării în caz de dezastru. Acestea asigură că datele dumneavoastră sunt în siguranță și pot fi restaurate rapid în cazul unor defecțiuni hardware, dezastre naturale sau alte evenimente catastrofale.

## Creați un fișier .BAK în SQL Server

Pentru a crea un fișier .bak în SQL Server, utilizați de obicei comenzi SQL Server Management Studio (SSMS) sau Transact-SQL (T-SQL), precum BACKUP DATABASE sau BACKUP LOG. Iată un exemplu simplificat despre cum puteți crea o copie de rezervă a bazei de date folosind T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Restaurați un fișier .BAK în SQL Server

Pentru a restaura o bază de date dintr-un fișier .bak, puteți utiliza comanda RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Cum se deschide fișierul BAK în SQL Server?

Pentru a deschide și a accesa datele stocate într-un fișier ".bak", de obicei trebuie să le restaurați într-o instanță Microsoft SQL Server. Iată pașii generali pentru a deschide un fișier ".bak" folosind SQL Server Management Studio (SSMS):

1. **Lansați SQL Server Management Studio**: deschideți SSMS pe computer. De obicei, îl puteți găsi în meniul Start sau căutând "SQL Server Management Studio".

2. **Conectați-vă la o instanță SQL Server**: în SSMS, conectați-vă la instanța SQL Server în care doriți să restaurați baza de date. Veți avea nevoie de permisiunile necesare pentru a efectua această operațiune.

3. **Restaurați baza de date**:

A. În panoul Object Explorer din partea stângă, extindeți instanța SQL Server.

b. Extindeți nodul "Băzuri de date".

c. Faceți clic dreapta pe "Baze de date" și selectați "Restaurați baza de date".

4. **Specificați sursa și destinația**:

A. În pagina "General" a casetei de dialog "Restaurare baza de date", introduceți un nume pentru noua bază de date în câmpul "Către baza de date". Acesta va fi numele bazei de date restaurate.

b. În secțiunea "Sursă", alegeți "Dispozitiv" ca tip de suport de rezervă.

c. Faceți clic pe butonul "..." de lângă câmpul "Dispozitiv" pentru a căuta fișierul ".bak" pe care doriți să îl restaurați.

d. Selectați fișierul ".bak" pe care doriți să îl deschideți și faceți clic pe "OK".

5. **Opțiuni de restaurare**: revizuiți și configurați opțiunile de restaurare după cum este necesar. Puteți specifica dacă să suprascrieți o bază de date existentă, să setați opțiuni de recuperare și multe altele. Asigurați-vă că setați aceste opțiuni în funcție de cerințele dvs.

6. **Inițiați restaurarea**: după ce ați configurat opțiunile de restaurare, faceți clic pe butonul "OK" din caseta de dialog "Restaurare baza de date". SQL Server va începe procesul de restaurare.

7. **Accesați baza de date restaurată**: după o restaurare cu succes, puteți accesa baza de date restaurată în SQL Server Management Studio la fel ca orice altă bază de date. Puteți executa interogări, puteți vizualiza tabele și puteți lucra cu datele din baza de date.

## Alte fișiere BAK

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.bak**.

**Bază de date**
- [BAK - Fișier de copiere a bazei de date](/ro/database/bak/)
- [BAK - Swiftpage Act! Backup baze de date](/ro/database/bak-act/)

**Joc**
- [BAK - Terraria World sau Player Backup](/ro/game/bak-terraria/)

**Diverse**
- [BAK - Fișier de rezervă](/ro/misc/bak-backup/)
- [BAK - Backup marcaje Chromium](/ro/misc/bak-chromium/)
- [BAK - Backup scor final 2012](/ro/misc/bak-finale/)
- [BAK - Backup MobileTrans](/ro/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/ro/misc/bak-vegas/)

**Setari**
- [BAK - Backup Holo Launcher](/ro/settings/bak-holo/)

## Referințe
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
