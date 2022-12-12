{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku LRC - Co to jest plik LRC?",
  "description":"Dowiedz się o pliku LRC Lyric i interfejsach API, które mogą tworzyć i otwierać pliki LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Czym jest plik LRC?

Plik LRC to tekstowy plik tekstowy, który zawiera tekst piosenki audio. Gdy utwór audio jest odtwarzany za pomocą odtwarzacza muzyki lub oprogramowania odtwarzacza audio na komputerze, plik LRC jest odczytywany równolegle i wyświetlany wraz z upływem czasu. Pliki LRC zawierają punkty kontrolne do wyświetlania tekstu podczas odtwarzania utworu. Ogólnie rzecz biorąc, pliki LRC mają taką samą nazwę jak odpowiadające im pliki audio, takie jak audio.mp3 i audio.lrc. Pliki LRC są podobne do plików z napisami, takich jak [SRT](/pl/video/srt/).

## Format pliku LRC — więcej informacji

Pliki w formacie tekstowym LRC są zapisywane jako zwykłe pliki tekstowe i można je otwierać i edytować w pliku tekstowym. Zawartość pliku LRC zawiera informacje o kolorze do wyświetlania tekstu tekstu.

## Formaty LRC

Istnieje wiele formatów plików LRC, które zostały opracowane w czasie. Te

### Prosty format LRC

Znaczniki czasu linii są w formacie [mm:ss.xx], gdzie mm to minuty, ss to sekundy, a xx to setne części sekundy.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Prosty format rozszerzony

Obejmuje możliwość zmiany i określenia płci tekstu za pomocą M: Mężczyzna, K: Kobieta, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Ulepszony format LRC

Ulepszony format LRC jest rozszerzoną wersją prostego formatu LRC. Dodaje znacznik czasu programu Word w formacie<mm:ss.xx> na końcu poprzedniego słowa.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Bibliografia

* [Format plików tekstowych LRC – Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

