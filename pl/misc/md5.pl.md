{
  "date" : "2021-07-29",
  "keywords" :["plik md5", "format pliku md5", "co to jest plik md5", "plik", "przykład md5", "rozszerzenie pliku md5", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Plik Sumy Kontrolnej MD5",
  "description":"Poznaj plik MD5 i interfejsy API, które mogą tworzyć i otwierać pliki MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Czym jest plik MD5?

Plik MD5 to plik sumy kontrolnej używany do weryfikacji integralności pliku. Jest podobny do odcisku palca dla powiązanego pliku i jest generowany w unikalny sposób przy użyciu algorytmu, który wykorzystuje liczbę bitów w pliku. Służy do weryfikacji pliku za pomocą oprogramowania takiego jak [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Jedną z zalet korzystania z plików MD5 jest sprawdzenie, czy pobrane pliki nie są uszkodzone.

## Format pliku MD5 — więcej informacji

Zwykle plik MD5 jest zapisywany pod tą samą nazwą, co oryginalna nazwa pliku, ale z rozszerzeniem .md5. Na przykład, jeśli skojarzona nazwa pliku to `abc_987_123456.grb`, odpowiednia nazwa pliku MD5 będzie miała postać `abc_987_123456.grb.md5`. Pliki MD5 pomagają zidentyfikować, czy otrzymany lub pobrany plik nie jest uszkodzony ani nie ma na niego wpływu złośliwa zawartość. Krótko mówiąc, pliki MD5 gwarantują kompletność pliku.


## Jak sprawdzić sumę kontrolną MD5?

Pojedynczy plik można sprawdzić/zweryfikować pod kątem MD5 za pomocą narzędzia [md5sum](https://en.wikipedia.org/wiki/Md5sum) w następujący sposób.

```
md5sum -c abc_987_123456.grb.md5
```

## Bibliografia

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

