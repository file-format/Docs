{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik HTACCESS - format pliku Apache HTACCESS",
  "description" :"Twój przewodnik po formacie pliku, aby dowiedzieć się, co to jest plik HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik HTACCESS?

Plik HTACCESS to plik konfiguracyjny Apache, który zapewnia mechanizm umożliwiający zmiany konfiguracji dla różnych folderów / katalogów witryny. Zawiera dyrektywy konfiguracyjne, które mają zastosowanie do katalogu i podkatalogów.

Plik HTACCESS wykonuje szereg kontroli, takich jak zdefiniowanie strony indeksu witryny, wyświetlanie strony błędu 404 (nie znaleziono strony), wykonywanie przekierowań stron 301 lub 302, blokowanie dostępu z określonego adresu IP lub innych witryn. Korzystanie z plików .htaccess spowalnia zatem ogólną wydajność serwera Apache [HTTP](/pl/web/http/).

## Format pliku HTACCESS

Pliki HTACCESS są zapisywane na dysku w formacie zwykłego pliku tekstowego. Oznacza to, że możesz otwierać i edytować te pliki w dowolnym edytorze tekstu. Nie ma nazwy przed „.” w pliku .htaccess, pokazując, że jest to plik ukryty w folderze.

## Typowe zastosowania pliku HTACCESS

Oto pięć typowych zastosowań pliku HTACCESS.

### Mod_Rewrite

Plik HTACCESS może służyć do wyznaczania i zmiany sposobu wyświetlania użytkownikom adresów URL i stron internetowych w witrynie.

### Uwierzytelnianie

Uwierzytelnianie można uzyskać za pomocą .htaccess, tworząc plik passowrd o nazwie .htpasswd. Dzięki temu odwiedzający witrynę mogą podać hasło, jeśli chcą odwiedzić określoną sekcję strony internetowej.

### Niestandardowe strony błędów

Możesz tworzyć niestandardowe strony błędów, takie jak 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not found i 500 Internal Error z plikiem .htaccess. Spowoduje to jednak spowolnienie działania serwera, ponieważ wszystkie kontrole będą wykonywane podczas uzyskiwania dostępu do stron.

### Typy MIME

Pliki Apache HTACCESS można modyfikować, aby zawierały typy MIME (Multipurpose Internet Mail Extensions). Dzięki temu serwer może obsługiwać dostarczanie plików aplikacji, które nie były obsługiwane przez witrynę.

### SSI

Włączenie po stronie serwera (SSI) działa jako świetna oszczędność czasu na stronie internetowej. SSI można włączyć, wstawiając następujący kod do pliku .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Przykład pliku Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Bibliografia

* [Samouczek serwera Apache HTTP: pliki .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

