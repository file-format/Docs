{
"data": "2023-06-12",
  "keywords": [
"piecz",
"plik bak",
"Kopia zapasowa bazy danych Microsoft SQL Server",
"co to jest plik bak",
"jak otworzyć plik bak",
"plik",
"rozszerzenie pliku bak",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku BAK - Kopia zapasowa bazy danych Microsoft SQL Server",
  "description":"Dowiedz się o formacie kopii zapasowej BAK SQL Server i interfejsach API, które umożliwiają tworzenie i otwieranie plików BAK.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "12.06.2023"
}

## Czym jest plik BAK?

Plik ".bak" w kontekście Microsoft SQL Server to format pliku kopii zapasowej używany do przechowywania kopii bazy danych SQL Server. Pliki te zawierają migawkę bazy danych w określonym momencie, w tym jej schemat, dane i inne powiązane informacje. Są one generowane przy użyciu wbudowanej funkcji tworzenia kopii zapasowych i przywracania SQL Server i służą kilku kluczowym celom:

1. **Odzyskiwanie danych:** Pliki .bak umożliwiają odzyskanie bazy danych w przypadku utraty danych, uszkodzenia lub innych problemów. Przywracając bazę danych z pliku .bak, możesz przywrócić ją do poprzedniego stanu, minimalizując przestoje i utratę danych.

2. **Migracja i klonowanie:** Pliki kopii zapasowych są często używane do migracji baz danych pomiędzy serwerami lub tworzenia kopii baz danych do celów testowania, programowania lub raportowania. Oferują spójny i wydajny sposób przenoszenia baz danych pomiędzy środowiskami.

3. **Odzyskiwanie do określonego momentu:** SQL Server umożliwia odzyskiwanie do określonego momentu przy użyciu plików .bak. Oznacza to, że możesz przywrócić bazę danych do określonego momentu, który może mieć kluczowe znaczenie dla zgodności z przepisami lub audytu danych.

4. **Odzyskiwanie po awarii:** Pliki .bak stanowią kluczową część planowania odzyskiwania po awarii. Zapewniają, że Twoje dane są bezpieczne i można je szybko przywrócić w przypadku awarii sprzętu, klęsk żywiołowych lub innych katastrofalnych zdarzeń.

## Utwórz plik .BAK w SQL Server

Aby utworzyć plik .bak w programie SQL Server, zwykle używasz poleceń SQL Server Management Studio (SSMS) lub Transact-SQL (T-SQL), takich jak BACKUP DATABASE lub BACKUP LOG. Oto uproszczony przykład tworzenia kopii zapasowej bazy danych przy użyciu języka T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Przywróć plik .BAK w SQL Server

Aby odtworzyć bazę danych z pliku .bak, możesz użyć polecenia RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Jak otworzyć plik BAK w SQL Server?

Aby otworzyć i uzyskać dostęp do danych przechowywanych w pliku ".bak", zazwyczaj trzeba przywrócić je do instancji Microsoft SQL Server. Oto ogólne kroki otwierania pliku ".bak" przy użyciu SQL Server Management Studio (SSMS):

1. **Uruchom SQL Server Management Studio**: Otwórz SSMS na swoim komputerze. Zwykle można go znaleźć w menu Start lub wyszukując "SQL Server Management Studio".

2. **Połącz się z instancją SQL Server**: W SSMS połącz się z instancją SQL Server, w której chcesz przywrócić bazę danych. Aby wykonać tę operację, będziesz potrzebować niezbędnych uprawnień.

3. **Przywróć bazę danych**:

A. W panelu Eksplorator obiektów po lewej stronie rozwiń instancję SQL Server.

B. Rozwiń węzeł "Bazy danych".

C. Kliknij prawym przyciskiem myszy "Bazy danych" i wybierz "Przywróć bazę danych".

4. **Określ źródło i miejsce docelowe**:

A. Na stronie "Ogólne" okna dialogowego "Przywróć bazę danych" wprowadź nazwę nowej bazy danych w polu "Do bazy danych". Będzie to nazwa przywróconej bazy danych.

B. W sekcji "Źródło" wybierz "Urządzenie" jako typ nośnika kopii zapasowej.

C. Kliknij przycisk "..." obok pola "Urządzenie", aby wyszukać plik ".bak", który chcesz przywrócić.

D. Wybierz plik ".bak", który chcesz otworzyć, i kliknij "OK".

5. **Opcje przywracania**: Przejrzyj i skonfiguruj opcje przywracania według potrzeb. Możesz określić, czy zastąpić istniejącą bazę danych, ustawić opcje odzyskiwania i nie tylko. Pamiętaj, aby ustawić te opcje zgodnie ze swoimi wymaganiami.

6. **Rozpocznij przywracanie**: Po skonfigurowaniu opcji przywracania kliknij przycisk "OK" w oknie dialogowym "Przywróć bazę danych". SQL Server rozpocznie proces przywracania.

7. **Dostęp do przywróconej bazy danych**: Po pomyślnym przywróceniu możesz uzyskać dostęp do przywróconej bazy danych w SQL Server Management Studio, tak jak w przypadku każdej innej bazy danych. Można uruchamiać zapytania, przeglądać tabele i pracować z danymi w bazie danych.

## Inne pliki BAK

Oto inne typy plików, które korzystają z rozszerzenia **.bak**.

**Baza danych**
- [BAK - Plik kopii zapasowej bazy danych](/pl/database/bak/)
- [BAK - Ustawa o Swiftpage! Kopia zapasowa bazy danych](/pl/database/bak-act/)

**Gra**
- [BAK - Kopia zapasowa świata Terraria lub gracza](/pl/game/bak-terraria/)

**Różne**
- [BAK - Plik kopii zapasowej](/pl/misc/bak-backup/)
- [BAK – Kopia zapasowa zakładek Chromium](/pl/misc/bak-chromium/)
- [BAK - Kopia zapasowa partytury finału 2012](/pl/misc/bak-finale/)
- [BAK - Kopia zapasowa MobileTrans](/pl/misc/bak-mobiletrans/)
- [BAK – kopia zapasowa projektu wideo VEGAS](/pl/misc/bak-vegas/)

**Ustawienia**
- [BAK – Kopia zapasowa programu uruchamiającego Holo](/pl/settings/bak-holo/)

## Bibliografia
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
