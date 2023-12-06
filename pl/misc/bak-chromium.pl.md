{
"data": "2023-06-12",
  "keywords": [
"piecz",
"plik bak",
"Zakładki BAK Chromowane",
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
"title": "Format pliku BAK - Kopia zapasowa zakładek Chromium",
  "description":"Dowiedz się o formacie zakładek BAK Chromium i interfejsach API, które umożliwiają tworzenie i otwieranie plików BAK.",
"linktitle": "Zakładki BAK Chromium",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "12.06.2023"
}

## Czym jest plik BAK?

Plik .bak w kontekście przeglądarek internetowych opartych na Chromium, takich jak Google Chrome i Microsoft Edge, jest w zasadzie plikiem kopii zapasowej Twoich zakładek. Te zakładki są zapisywane w postaci zwykłej listy tekstowej, a używanym formatem pliku jest JSON. Celem tych plików .bak jest zabezpieczenie zakładek poprzez utworzenie kopii zapasowej, którą można przywrócić w przypadku przypadkowego usunięcia lub utraty.

Przeglądarki oparte na Chromium, w tym Google Chrome, rutynowo tworzą te pliki kopii zapasowych i zwykle nadają im nazwę "Bookmarks.bak". Zasadniczo są to migawki zakładek z określonego momentu.

## Jak użyć pliku .bak do przywrócenia zakładek

1. **Znajdź plik kopii zapasowej:** Zwykle znajduje się on w określonym folderze powiązanym z Twoim profilem Chromium. Dokładna lokalizacja może się różnić w zależności od systemu operacyjnego.

W systemie Windows: zajrzyj do `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

W systemie macOS: Wyszukaj w `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

W systemie Linux: Sprawdź `~/.config/chromium/Default/Bookmarks.bak`.

3. Upewnij się, że Twoja przeglądarka Chromium jest zamknięta.
4. Zmień nazwę pliku "Bookmarks.bak", usuwając rozszerzenie ".bak", tak aby nazywał się po prostu "Bookmarks".
5. Uruchom Chroma.

Zmieniając nazwę pliku .bak na "Zakładki", Chromium użyje go jako bieżącego pliku zakładek, a poprzednie zakładki powinny zostać przywrócone.

## Kopia zapasowa zakładek Chromium

Tworzenie kopii zapasowych zakładek Chromium to mądry środek ostrożności, który pozwala mieć pewność, że nie utracisz ważnych zapisanych stron internetowych i adresów URL. Chromium to przeglądarka typu open source, która stanowi bazę dla innych przeglądarek, takich jak Google Chrome i Microsoft Edge. Aby utworzyć kopię zapasową zakładek Chromium, wykonaj następujące kroki:

## Metoda 1: Ręczna kopia zapasowa

1. **Otwórz Chromium**: Uruchom przeglądarkę Chromium na swoim komputerze.

2. **Dostęp do zakładek**: Kliknij trzy pionowe kropki (ikona menu) w prawym górnym rogu okna przeglądarki. W menu rozwijanym najedź kursorem na "Zakładki", aby wyświetlić podmenu zakładek.

3. **Eksportuj zakładki**: W podmenu zakładek kliknij "Menedżer zakładek". Spowoduje to otwarcie nowej karty zawierającej Twoje zakładki.

4. **Eksportuj zakładki**: Na karcie menedżera zakładek kliknij ponownie trzy pionowe kropki (zwykle w prawym górnym rogu), aby otworzyć menu menedżera zakładek. Z tego menu wybierz opcję "Eksportuj zakładki".

5. **Wybierz lokalizację**: Wybierz, gdzie chcesz zapisać wyeksportowany plik zakładek na swoim komputerze. Domyślna nazwa pliku to "bookmarks.html", ale możesz ją zmienić, jeśli wolisz. Zapisz go w lokalizacji, którą zapamiętasz.

6. **Zapisz**: Kliknij przycisk "Zapisz" lub "Eksportuj", aby zapisać swoje zakładki jako plik HTML.

Kopia zapasowa Twoich zakładek została utworzona w postaci pliku HTML. Możesz skopiować ten plik na dysk zewnętrzny lub do przechowywania w chmurze w celu bezpiecznego przechowywania.

## Metoda 2: Synchronizacja z kontem Google (jeśli dotyczy)

Jeśli jesteś zalogowany na konto Google w Chromium, możesz także skorzystać z wbudowanej funkcji synchronizacji, aby zapewnić bezpieczeństwo i synchronizację zakładek na różnych urządzeniach. W ten sposób kopia zapasowa zakładek zostanie automatycznie utworzona na Twoim koncie Google.

1. **Otwórz Chromium**: Uruchom przeglądarkę Chromium i upewnij się, że jesteś zalogowany na swoim koncie Google.

2. **Włącz synchronizację**: Kliknij trzy pionowe kropki (ikona menu) w prawym górnym rogu okna przeglądarki i przejdź do "Ustawienia".

3. **Synchronizacja i usługi Google**: W zakładce Ustawienia kliknij "Synchronizacja i usługi Google" na lewym pasku bocznym.

4. **Synchronizuj swoje dane**: w sekcji "Synchronizuj" upewnij się, że "Zakładki" są włączone. Spowoduje to zsynchronizowanie zakładek z kontem Google.

Kopia zapasowa Twoich zakładek zostanie teraz automatycznie utworzona i zsynchronizowana z Twoim kontem Google. Możesz uzyskać do nich dostęp, logując się na swoje konto Google na dowolnym urządzeniu z Chromium lub inną przeglądarką obsługującą synchronizację Google.

Pamiętaj, aby okresowo tworzyć ręczne kopie zapasowe zakładek, zwłaszcza jeśli chcesz mieć kopię lokalną, która nie jest zależna wyłącznie od synchronizacji Twojego konta Google.

## Jak otworzyć plik BAK

Jeśli chcesz zbadać surowe dane kopii zapasowej zakładek, możesz otworzyć plik "Bookmarks.bak" za pomocą różnych edytorów tekstu, takich jak Microsoft Visual Studio Code (dostępny na wielu platformach), Microsoft Notepad (dla użytkowników systemu Windows), Apple TextEdit (dla użytkowników komputerów Mac) lub dowolny inny wybrany edytor tekstu. Umożliwi to wyświetlenie zakładek i metadanych zawartych w pliku.

Możesz otworzyć plik "Bookmarks.bak" i przeglądać jego zawartość za pomocą różnych programów do edycji tekstu i edytorów kodu. Oto kilka często używanych opcji:

1. Kod Visual Studio (kod VS)
2. Notatnik (Windows)
3. Edycja tekstu (Mac)
4. Wzniosły tekst
5. Notatnik++
6. Atom
7. nano i Vim (Linux)
8. WordPad (Windows)

## Inne pliki BAK

Oto inne typy plików, które korzystają z rozszerzenia **.bak**.

**Baza danych**
- [BAK - Plik kopii zapasowej bazy danych](/pl/database/bak/)
- [BAK - Ustawa o Swiftpage! Kopia zapasowa bazy danych](/pl/database/bak-act/)
- [BAK - Kopia zapasowa bazy danych Microsoft SQL Server](/pl/database/bak-sqlserver/)

**Gra**
- [BAK - Kopia zapasowa świata Terraria lub gracza](/pl/game/bak-terraria/)

**Różne**
- [BAK - Plik kopii zapasowej](/pl/misc/bak-backup/)
- [BAK - Kopia zapasowa partytury finału 2012](/pl/misc/bak-finale/)
- [BAK - Kopia zapasowa MobileTrans](/pl/misc/bak-mobiletrans/)
- [BAK – kopia zapasowa projektu wideo VEGAS](/pl/misc/bak-vegas/)

**Ustawienia**
- [BAK – Kopia zapasowa programu uruchamiającego Holo](/pl/settings/bak-holo/)

## Bibliografia
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
