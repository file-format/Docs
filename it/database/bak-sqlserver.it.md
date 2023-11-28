{
"data": "2023-06-12",
  "keywords": [
"bak",
"file bak",
"Backup del database di Microsoft SQL Server",
"cos'è un file bak",
"come aprire il file bak",
"file",
"estensione del file bak",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file BAK - Backup del database di Microsoft SQL Server",
  "description":"Informazioni sul formato di backup di BAK SQL Server e sulle API in grado di creare e aprire file BAK.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent" : "database"
}
},
"lastmod": "2023-06-12"
}

## Cos'è un file BAK?

Un file ".bak", nel contesto di Microsoft SQL Server, è un formato di file di backup utilizzato per archiviare copie di un database SQL Server. Questi file contengono uno snapshot del database in un momento specifico, inclusi schema, dati e altre informazioni correlate. Vengono generati utilizzando la funzionalità di backup e ripristino integrata di SQL Server e servono a diversi scopi cruciali:

1. **Recupero dati:** i file .bak forniscono un mezzo per ripristinare un database in caso di perdita di dati, danneggiamento o altri problemi. Ripristinando un database da un file .bak, puoi riportarlo a uno stato precedente, riducendo al minimo i tempi di inattività e la perdita di dati.

2. **Migrazione e clonazione:** i file di backup vengono spesso utilizzati per migrare i database tra server o creare copie di database a scopo di test, sviluppo o reporting. Offrono un modo coerente ed efficiente per spostare i database tra ambienti.

3. **Recupero point-in-time:** SQL Server consente di eseguire il ripristino point-in-time utilizzando file .bak. Ciò significa che puoi ripristinare un database a un momento specifico nel tempo, il che può essere fondamentale per la conformità normativa o il controllo dei dati.

4. **Disaster Recovery:** i file .bak rappresentano una parte fondamentale della pianificazione del ripristino di emergenza. Garantiscono che i tuoi dati siano al sicuro e possano essere ripristinati rapidamente in caso di guasti hardware, disastri naturali o altri eventi catastrofici.

## Creare un file .BAK in SQL Server

Per creare un file .bak in SQL Server, in genere si utilizzano comandi SQL Server Management Studio (SSMS) o Transact-SQL (T-SQL) come BACKUP DATABASE o BACKUP LOG. Ecco un esempio semplificato di come potresti creare un backup del database utilizzando T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Ripristinare un file .BAK in SQL Server

Per ripristinare un database da un file .bak, puoi utilizzare il comando RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Come aprire il file BAK in SQL Server?

Per aprire e accedere ai dati archiviati in un file ".bak", in genere è necessario ripristinarlo in un'istanza di Microsoft SQL Server. Di seguito sono riportati i passaggi generali per aprire un file ".bak" utilizzando SQL Server Management Studio (SSMS):

1. **Avvia SQL Server Management Studio**: apri SSMS sul tuo computer. In genere è possibile trovarlo nel menu Start o cercando "SQL Server Management Studio".

2. **Connetti a un'istanza di SQL Server**: in SSMS, connettiti all'istanza di SQL Server in cui desideri ripristinare il database. Avrai bisogno delle autorizzazioni necessarie per eseguire questa operazione.

3. **Ripristina database**:

UN. Nel riquadro Esplora oggetti sul lato sinistro, espandere l'istanza di SQL Server.

B. Espandi il nodo "Database".

C. Fare clic con il tasto destro su "Database" e selezionare "Ripristina database".

4. **Specificare origine e destinazione**:

UN. Nella pagina "Generale" della finestra di dialogo "Ripristina database" inserire nel campo "Al database" un nome per il nuovo database. Questo sarà il nome del database ripristinato.

B. Nella sezione "Origine", scegli "Dispositivo" come tipo di supporto di backup.

C. Fare clic sul pulsante "..." accanto al campo "Dispositivo" per cercare il file ".bak" che si desidera ripristinare.

D. Seleziona il file ".bak" che desideri aprire e fai clic su "OK".

5. **Opzioni di ripristino**: esamina e configura le opzioni di ripristino secondo necessità. È possibile specificare se sovrascrivere un database esistente, impostare opzioni di ripristino e altro. Assicurati di impostare queste opzioni in base alle tue esigenze.

6. **Avviare il ripristino**: una volta configurate le opzioni di ripristino, fare clic sul pulsante "OK" nella finestra di dialogo "Ripristina database". SQL Server inizierà il processo di ripristino.

7. **Accesso al database ripristinato**: dopo un ripristino riuscito, è possibile accedere al database ripristinato in SQL Server Management Studio proprio come qualsiasi altro database. È possibile eseguire query, visualizzare tabelle e lavorare con i dati all'interno del database.

## Altri file BAK

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.bak**.

**Banca dati**
- [BAK - File di backup del database](/it/database/bak/)
- [BAK - Atto Swiftpage! Backup del database](/it/database/bak-act/)

**Gioco**
- [BAK - Terraria World o Backup del giocatore](/it/game/bak-terraria/)

**Varie**
- [BAK - File di backup](/it/misc/bak-backup/)
- [BAK - Backup dei segnalibri di Chromium](/it/misc/bak-chromium/)
- [BAK - Backup della partitura di Finale 2012](/it/misc/bak-finale/)
- [BAK - Backup MobileTrans](/it/misc/bak-mobiletrans/)
- [BAK - Backup progetto video VEGAS](/it/misc/bak-vegas/)

**Impostazioni**
- [BAK - Backup di Holo Launcher](/it/settings/bak-holo/)

## Riferimenti
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
