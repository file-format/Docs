{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KONFIGURACJA - Plik konfiguracyjny",
  "description":"Poznaj format pliku CONFIG z przykładem CONFIG i interfejsami API, które mogą tworzyć i otwierać pliki CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Czym jest plik CONFIG?
Plik CONFIG jest znany jako plik konfiguracyjny; służy do konfigurowania parametrów i ustawień podstawowych dla kilku programów komputerowych. Niektóre programy odczytują tylko swoje **pliki konfiguracyjne** podczas uruchamiania. Inni okresowo sprawdzają pliki konfiguracyjne pod kątem zmian.

## KONFIG Format pliku
**Format pliku CONFIG** jest używany do procesów serwera, aplikacji i ustawień systemu operacyjnego. Programista może napisać kod, który poinstruuje oprogramowanie, aby wielokrotnie odczytywało pliki konfiguracyjne po określonym czasie i stosowało zmiany do bieżącego procesu. Nie ma ostatecznych standardów ani mocnych konwencji dotyczących pliku CONFIG sysntax. Na przykład plik Web.config firmy Microsoft należy do formatu pliku CONFIG, który składa się z zestawów tagów opartych na [XML](https://docs.fileformat.com/web/xml/); można edytować za pomocą programu Microsoft Visual Studio lub dowolnego innego edytora tekstu.

## Przykładowe pliki konfiguracyjne:
Ponieważ pliki konfiguracyjne nie są tworzone zgodnie z żadnymi regułami, standardami ani konwencjami, pliki te mogły zostać zapisane przy użyciu różnych formatów. Plik .config może być oparty na XML, [JSON](https://docs.fileformat.com/web/json/) lub dowolnym innym formacie. Poniżej przedstawiono przykłady plików konfiguracyjnych dla dobrze znanych systemów operacyjnych i oprogramowania:

### Pliki konfiguracyjne w systemie Linux
Każdy program linuksowy jest plikiem wykonywalnym zawierającym listę **kodów operacyjnych**, które procesor wykonuje w celu wykonania typowych operacji. Działanie niemal każdego programu można dostosować do własnych wymagań, zmieniając jego pliki konfiguracyjne. Kilka plików konfiguracyjnych w systemie Linux znajduje się w katalogu /etc. Pliki konfiguracyjne można podzielić na następujące kategorie:
|Kategoria|Przykład| Komentarze|
---|---|---|
|Dostęp do plików|/etc/host.conf|Instruuje serwer domeny sieciowej, jak wyszukiwać nazwy hostów.|
|Uruchamianie i logowanie/wylogowanie|/etc/rc.d/rc.local|Nieoficjalne. Można wywołać z rc, rc.sysinit lub /etc/inittab.|
|System plików|/etc/mtools.conf|Konfiguracja wszystkich operacji (mkdir, kopiowanie, formatowanie itp.) na systemie plików typu DOS.|
|Administracja systemem|/etc/shells|Przechowuje listę możliwych „powłok” dostępnych dla systemu.|
|Sieć|/etc/gated.conf|Konfiguracja dla gated. Używany tylko przez bramowanego demona.|
|Polecenia systemowe|/etc/logrotate.conf|Konfiguracja Dynamic Linkera.|
|Daemony|/etc/httpd.conf|Plik konfiguracyjny dla Apache, serwera WWW. Tego pliku zwykle nie ma w /etc.|
|Programy użytkownika| /etc/lynx.cfg| Ustawienia proxy|
### Przykład pliku AWS CONFIG
Często używane ustawienia konfiguracyjne i poświadczenia można zapisać w plikach CONFIG, które są obsługiwane przez AWS CLI. Plik CONFIG musi być zwykłym plikiem tekstowym w następującym formacie:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Przykład pliku SSH CONFIG
Plik konfiguracyjny po stronie klienta OpenSSH nosi nazwę CONFIG i jest przechowywany w katalogu .ssh. Plik SSH CONFIG składa się z następującej struktury:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Przykładowy plik Python CONFIG
Plik Python CONFIG może wyglądać tak:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Bibliografia

* [Zrozumienie plików konfiguracyjnych systemu Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Konfiguracja i ustawienia pliku poświadczeń](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Pliki konfiguracyjne w Pythonie](https://martin-thoma.com/configuration-files-in-python/)

