{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik P7S - Cyfrowo podpisana wiadomość e-mail",
  "description":"Poznaj format pliku P7S i API, które mogą tworzyć i otwierać pliki P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Czym jest plik P7S?

Plik P7S to podpis cyfrowy otrzymywany wraz z cyfrowo podpisaną wiadomością e-mail. Obecność tego pliku jako załącznika do wiadomości e-mail potwierdza, że wiadomość e-mail została wysłana z autentycznego źródła. Dzięki temu nadawca ma zainstalowany na swoim komputerze certyfikat podpisywania wiadomości e-mail. Gdy tak podpisana wiadomość e-mail jest wysyłana z komputera użytkownika, dołączany jest do niej plik P7S zawierający nazwę nadawcy. Klienci poczty e-mail obsługujący podpisane wiadomości e-mail mogą wyświetlać informacje o nadawcy.

## Format pliku P7S — więcej informacji

S/MIME (Secure/Multipurpose Internet Mail Extensions) Pliki P7S zawierają informacje w formacie zwykłego tekstu, który jest czytelny dla człowieka. Klienci poczty e-mail, tacy jak Microsoft Outlook, Apple Mail i Mozilla Thunderbird, obsługują odczytywanie podpisanych cyfrowo informacji z wiadomości e-mail S/MIME. Podpisanie wiadomości e-mail weryfikuje tożsamość nadawcy i informuje odbiorcę, że wiadomość jest autentyczna. Gdy wiadomości e-mail są pobierane z klientów poczty e-mail (jako [EML](/pl/email/eml/) lub [MSG](/pl/email/msg/)), te pliki P7S są dołączane do tych wiadomości e-mail.

Plik P7S zawiera następujące informacje:

* Źródło pochodzenia wiadomości e-mail
* Data i godzina wysłania,
* Czy został zmodyfikowany podczas transmisji

Te informacje są osadzone przy użyciu technologii Public-Key Cryptography Standard #7 (PKCS7) do cyfrowego dołączania zaszyfrowanych podpisów do wiadomości e-mail.

## Bibliografia ##

* [Narzędzie do podpisywania firmy Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

