{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik HDMP - Format pliku zrzutu sterty systemu Windows",
  "description":"Dowiedz się o formacie plików HDMP i interfejsach API, które mogą tworzyć i otwierać pliki HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Czym jest plik HMP?

Plik HDMP to nieskompresowany zrzut pamięci, gdy aplikacja lub program ulega awarii z powodu błędu. Jest tworzony tylko przez Windows XP/Vista i zawiera zrzut stanu aplikacji w momencie jej awarii. Nieskompresowane pliki HDMP zajmują więcej miejsca na dysku w porównaniu z plikami Minidump [MDMP](/pl/system/mdmp/), które są kompresowane do celów raportowania.

Aplikacje, których można używać do **otwierania** lub analizowania plików HDMP, obejmują Microsoft Visual Studio z narzędziami do debugowania dla systemu Windows.

## Format pliku HDMP

Pliki HDMP są zapisywane na dysku jako pliki binarne i nie przynoszą żadnych korzyści, jeśli są otwierane bez odpowiednich aplikacji. Zawierają one odpowiednie dane systemowe zarejestrowane w momencie wystąpienia błędu.

### Różnica między formatami plików HDMP i MDMP

HDMP to nieskompresowane pliki zrzutu pamięci. W przeciwieństwie do tego, MDMP to mini pliki zrzutu, które są kompresowane w celu zmniejszenia rozmiaru pliku i wysyłane do firmy Microsoft w celu zgłoszenia problemu.

## Odniesienie ##

* [DMP — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

