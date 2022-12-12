{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik CRL - Lista Unieważnionych Certyfikatów",
  "description":"Poznaj format pliku CRL i interfejsy API, które mogą tworzyć i otwierać pliki CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Czym jest plik CRL?

Plik CRL (Certificate Revocation List) to czarna lista cyfrowych certyfikatów X.509, które urząd certyfikacji (CA) unieważnia przed przypisaną im datą unieważnienia. Zawiera informacje o problemie i dacie unieważnienia, które umożliwiają administratorom bezpieczeństwa blokowanie certyfikatów cyfrowych, których dotyczy problem. CRL nie zawiera wygasłych certyfikatów, ponieważ jej głównym celem jest powiadamianie o niezaufanych i nieważnych certyfikatach.

Aplikacje, które mogą **otwierać pliki CRL**, obejmują OpenSSL, Microsoft IIS Server i Citrix NetScaler.

## Format pliku CRL — więcej informacji

Pliki CRL zawierają informacje w standardzie X.509, który określa również semantykę udostępniania informacji o kluczu publicznym. Inne informacje zawarte w pliku CRL mogą obejmować termin, na jaki certyfikaty zostały unieważnione, przyczynę unieważnienia, numer seryjny unieważnionego certyfikatu oraz znacznik czasu.


### Najważniejsze powody dodawania certyfikatów do listy CRL

Może być kilka przyczyn unieważnienia certyfikatu Twojej witryny i dodania jej do listy CRL. Niektóre z nich mogą być;

1. Klucz prywatny Twojego certyfikatu został naruszony
1. Twój certyfikat jest nieważny lub został błędnie wydany przez urząd certyfikacji
1. Zmieniają się dane organizacyjne powiązane z certyfikatem i urząd certyfikacji wystawia nowy certyfikat
1. Każdy inny nieunikniony powód, dla którego certyfikat został unieważniony

## Bibliografia

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force's (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Lista unieważnionych certyfikatów](https://en.wikipedia.org/wiki/Certificate_revocation_list)

