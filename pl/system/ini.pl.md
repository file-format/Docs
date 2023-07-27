{
  "date" : "2021-07-07",
  "keywords" :["INI", "rozszerzenie", "plik", "format", "system", "inicjacja", "rozszerzenie katalogu", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - format pliku inicjującego",
  "description":"Poznaj format pliku INI i interfejsy API, które mogą tworzyć i otwierać pliki INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Czym jest plik INI? ##

Plik INI to dokument konfiguracyjny wiadomości dla programów komputerowych, który zawiera klucze publiczne dla cech i sekcji, które organizują atrybuty w ramach i gramatyce. Te dokumenty konfiguracji formatu plików systemowych biorą swoją nazwę od rozszerzenia katalogu systemu operacyjnego MS-DOS INI, co oznacza inicjację. To spopularyzowało tę formę instalacji oprogramowania. Wiele programów w innych aplikacjach używa różnych rozszerzeń nazw plików, takich jak CONF i [CFG](/pl/system/cfg/), chociaż format ten ustanowił nieoficjalny standard w wielu sytuacjach konfiguracyjnych.

## Krótka historia plików INI##

Początkowo główną techniką konfiguracji programu systemu Windows był format pliku tekstowego, który składał się z wierszy tekstu z jedną kluczową parą w wierszu, podzielonych na sekcje. Sterowniki urządzeń, kroje pisma i uruchamiające programy uruchamiające były przechowywane w tym formacie. Indywidualne ustawienia były również powszechnie przechowywane w plikach INI przez aplikacje.
Do wersji Windows 3.1x format był obsługiwany na 16-bitowych platformach Microsoft Windows. Począwszy od systemu Windows 95, Microsoft zaczął zachęcać programistów do używania rejestru systemu Windows zamiast plików INI do konfiguracji.

## Plik INI — specyfikacje formatu pliku

### Klucze/Właściwości ###

Klucz/właściwość jest najbardziej podstawowym elementem pliku INI. Symbol równości (=) oddziela nazwę i wartość każdego klucza. Po lewej stronie znaku równości znajduje się miejsce, w którym wyświetlana jest nazwa. Znak równości i średnik są w systemie Windows dyskretnymi literami, dlatego nie mogą być użyte w kluczu. W wartości można użyć dowolnego znaku.

```
name=value
```

### Sekcje ###

Komentarz do sekcji pojawia się w nawiasach kwadratowych ([]) w osobnym wierszu. Po zdefiniowaniu sekcji wszystkie klucze są powiązane z tą sekcją. Sekcje kończą się na następnym oznaczeniu sekcji lub na końcu dokumentu; nie ma określonego separatora „końca sekcji”. Sekcji nie można układać w stosy; można je nazwać tylko raz i nie trzeba ich łączyć.

```
[section]
a=a
b=b
```

### Zmiana funkcji ###

Format pliku INI nie ma globalnie akceptowanej definicji. Wiele aplikacji komputerowych zawiera funkcje dodatkowe do już wymienionych. Poniższa lista zawiera niektóre wspólne cechy, które mogą, ale nie muszą być uwzględnione w każdym indywidualnym programie.

* Uwagi
* Znaki ucieczki
* Zduplikowane nazwy


## Przykład INI ##

Przykładowy plik INI wygląda następująco:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Odniesienie ##

* [DMP — Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

