{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "plik", "rozszerzenie", "format", "czym jest format pliku m4b", "muzyka", "format pliku m4b", "M4b vs MP3", "specyfikacja formatu pliku m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików M4B i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki M4B.",
  "title" :"M4B - format pliku audiobooka MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Czym jest plik M4B?

Plik z rozszerzeniem .m4b to audiobook powszechnie używany przez książki Apple i iTunes. Dźwięk używany w tym formacie jest przechowywany w formacie MPEG-4 i kompresowany przy użyciu kodowania AAC. Plik M4B jest bardzo podobny do M4A, ale obsługuje funkcje związane z audiobookami, takie jak zakładki i podziały rozdziałów. Pliki M4B są dostępne zarówno w wersjach z obsługą DRM, jak i bez DRM. Audiobooki z kodowaniem DRM to zazwyczaj płatne audiobooki ze sklepu iTunes Store. Natomiast bez DRM można łatwo znaleźć w Internecie.

## Format pliku M4B

Pliki audiobooków zawierające metadane, obrazy, zakładki i hiperłącza można zapisać z rozszerzeniem .m4a, ale zazwyczaj podczas zapisywania używane jest rozszerzenie .m4b, aby określić, że plik ma format pliku audiobooka. Fairplay DRM (Digital Rights Management) jest używany przez aplikację do ochrony plików M4B. Tak więc pliki pobrane z iTunes można odtwarzać tylko na autoryzowanych urządzeniach lub komputerach.


## M4B kontra M4A

Zarówno M4B, jak i [MP3](https://docs.fileformat.com/audio/mp3/) to formaty plików wyłącznie audio.

**M4B**: Wygrywa w porównaniu z MP3 pod względem jakości, jeśli oba są kodowane z tą samą szybkością transmisji bitów. M4B to plik audiobooka skompresowany przy użyciu kodowania AAC. Zasadniczo jest kojarzony z „MPEG-4 Audio Layer”, pliki z rozszerzeniem .m4b są warstwą dźwiękową filmów MPEG-4, ale z dodatkowymi funkcjami związanymi z audiobookami. Jego celem jest wyprzedzenie MP3 i ustanowienie nowego standardu kompresji dźwięku. Pod wieloma względami jest bardzo zbliżony do MP3, ale został opracowany z myślą o lepszej jakości w tym samym lub nawet mniejszym rozmiarze pliku. Format M4B został po raz pierwszy wprowadzony przez firmę Apple. Typ formatu jest również realizowany jako bezstratny koder Apple (ALE).

Dlatego obecnie M4B nie mógł osiągnąć sukcesu głównego nurtu MP3, ponieważ format audio nie jest jeszcze powszechnie odtwarzany.

**Mp3**: Cyfrowy format audio, który jest dobrze wszystkim znany. Pierwszy format kompresji na scenie i stał się bardzo popularny wśród słuchaczy muzyki. Jego mainstreamowy sukces jest tak szybki, że typ pliku może być odtwarzany uniwersalnie i kompatybilny z prawie wszystkim, zarówno sprzętem, jak i oprogramowaniem. Ogólnie rzecz biorąc, M4A zapewni lepszą jakość dźwięku, ale wielu twierdzi, że niezależnie od tego, czy to prawda, czy nie, różnica dźwięku nie jest porównywalna, a próba konwersji plików MP3 do plików M4A byłaby stratą czasu. Wreszcie konwersja spowoduje utratę oryginalnej jakości dźwięku.

## Specyfikacja formatu pliku M4B

Podobnie jak [M4A](/pl/audio/m4a/), pliki M4B również składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek i jest podzielony jako:
- 4-bajtowy rozmiar porcji (big-endian, najpierw starszy bajt)
- 4-bajtowy typ chunka - jedna z predefiniowanych sygnatur: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "szeroki", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Podobnie jak w przypadku M4A, pierwsza porcja w M4B będzie typu „ftype” i ma podtyp o przesunięciu 8. M4B zdefiniowany przez podtyp, który musi być „M4B_”.

Powtarzanie porcji, aż do wykrycia porcji nieznanego typu, utworzy plik M4B (MPEG-4 Audio).

## Bibliografia

* [MPEG-4 część 14 – z Wikipedii](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format i przykład odzyskiwania](https://www.file-recovery.com/m4a-signature-format.htm)

