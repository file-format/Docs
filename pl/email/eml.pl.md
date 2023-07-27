{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Wiadomość e-mail",
  "description":"Poznaj format pliku EML i interfejsy API, które mogą tworzyć i otwierać pliki EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Czym jest plik EML?

Format pliku EML reprezentuje wiadomości e-mail zapisane za pomocą programu Outlook i innych odpowiednich aplikacji. Prawie wszyscy klienci poczty e-mail obsługują ten format plików ze względu na jego zgodność ze standardem RFC-822 Internet Message Format Standard. Microsoft Outlook to domyślne oprogramowanie do otwierania typów wiadomości EML. Pliki EML mogą być używane do zapisywania na dysku, a także wysyłania do odbiorców za pomocą protokołów komunikacyjnych.

## Krótka historia EML

Specyfikacje formatu plików EML są dostępne zgodnie ze standardowym formatem [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Przed RFC-822, RFC-733 rządził zasadami wymiany komunikatów sieciowych do 1982 roku, ten pierwszy powstał jako ulepszenie lateral przez ustanowienie standardów ARPA. W tym samym czasie Microsoft stworzył własne moduły COM do rozwoju własnego klienta pocztowego, czyli Outlook Express. RFC-822 został ustanowiony jako zastrzeżony format, gdy firma Microsoft odeszła od otwartego standardu i stworzyła format pliku [PST](/pl/email/pst/), w którym wiadomości e-mail są zapisywane w wysoce ustrukturyzowanym formacie bazy danych. Spowodowało to problemy dla użytkowników klientów poczty e-mail firm innych niż Microsoft, gdy wiadomości e-mail były przekazywane z programu Microsoft Outlook.

W 2001 roku standard 822 został rozszerzony do 2822 - Internet Message Format, który jest obecnie używany do tworzenia, odczytywania i wysyłania wiadomości EML w formacie MIME RFC-822.

## Specyfikacje formatu plików EML

Pliki EML składają się z dwóch wyróżniających się sekcji:

* Nagłówki - Zawiera informacje o nagłówku wiadomości
* Treść wiadomości — zawiera szereg informacji, które mogą obejmować treść wiadomości, osadzone obrazy i załączniki

### Informacje o nagłówkach ###

Plik EML składa się z informacji nagłówków i opcjonalnie treści wiadomości. Każda linia nagłówka w EML składa się z dwóch części oddzielonych dwukropkiem „:”. Pierwszy nazywa się Nazwa nagłówka, a następny po dwukropku to treść nagłówka. Do takich nagłówków należą na przykład:

* Adres e-mail nadawcy
* Adres e-mail odbiorcy
* Temat e-maila
* Znacznik czasu i daty wiadomości

**Przykładowy nagłówek**

Z:<John@bmw.eml.light.com>

Do:<Andy@fileformat.com>

Data: czw., 8 marca 2018 r. 10:43:37 +0100

Temat: kontrolka bmw eml

### Treść wiadomości ###

Treść wiadomości EML zawiera podstawowe informacje o wiadomości e-mail w postaci tekstu, hiperłączy i załączników. Treść wiadomości e-mail może zawierać zwykły czytelny tekst, ale nie jest to konieczne. W takim przypadku treść wiadomości może być pusta lub zawierać zaszyfrowane dane załączników.

Treść treści wiadomości jest opisana przez jej Content-Type, co umożliwia aplikacjom czytającym odczytywanie informacji w odpowiednich formatach. W rzeczywistości reprezentuje charakter i format dokumentu. Struktura typu MIME lub typu zawartości jest bardzo prosta; składa się z typu i podtypu, dwóch łańcuchów oddzielonych znakiem „/”. Brak miejsca jest dozwolone. `Typ` reprezentuje kategorię i może być typem dyskretnym lub wieloczęściowym. Podtyp jest specyficzny dla każdego typu. Lista typów należących do kategorii Content-Type jest długa, ale niektóre ważne typy treści to:


|**Typ**|**Opis**|**Przykłady podtypów**
---|---|---|
|text|Reprezentuje format czytelny dla człowieka|text/plain, text/html, text/css, text/javascript
|image|Reprezentuje obraz dowolnego typu z wyłączeniem wideo|image/bmp, image/png, image/jpg, image/gif
|audio|Reprezentuje dowolny format pliku audio|audio/mdi, audio/wav
|application|Reprezentuje dowolny rodzaj danych binarnych|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Reprezentacja załącznika w treści EML ###

Treść EML zawiera granice dla każdego typu zawartości, który zawiera. Załącznik w treści wiadomości jest identyfikowany przez jego Content-Type i Content-Disposition, jak pokazano w poniższym przykładzie:

Typ zawartości: tekst/zwykły; zestaw znaków # "windows-1252"; name#"apple app store.txt"
Treść-dyspozycja: załącznik; nazwa pliku#"sklep z aplikacjami Apple.txt"
Kodowanie przesyłania treści: base64
Identyfikator załącznika X: f_jkhztmd02

Jak widać, ustawienie Content-Disposition na attach umożliwia aplikacjom odczytującym pobieranie informacji o załączniku, takich jak nazwa pliku załącznika i kodowanie transferu. Po informacji nagłówka załącznika następuje zakodowana treść załącznika, którą należy przeczytać.

#### Przykład arkusza kalkulacyjnego jako załącznika ####

Typ zawartości: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Treść-dyspozycja: załącznik; nazwa pliku#"english_spodr.xlsx"
Kodowanie przesyłania treści: base64
Identyfikator załącznika X: f_jkhztmd43

## Bibliografia

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

