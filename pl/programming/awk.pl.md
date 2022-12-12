{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku AWK - Plik skryptu AWK",
  "description":"Dowiedz się o formacie pliku AWK i interfejsach API, które mogą tworzyć i otwierać pliki AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Czym jest plik AWK?

Plik AWK to plik skryptu utworzony dla aplikacji do przetwarzania tekstu **AWK**, który jest dostarczany w pakiecie z systemami operacyjnymi Unix i Linux. Zawiera logiczne instrukcje wykonywania działań na tekście lub zawartości pliku, takich jak dopasowywanie, zastępowanie i drukowanie tekstu. Pomaga to generować raporty i sformatowany tekst z pliku wejściowego. Narzędzie awk zwykle znajduje się w /usr/bin/awk w większości dystrybucji linux/unix.

## Jak utworzyć skrypt AWK?

Plik AWK można utworzyć lub otworzyć w dowolnym edytorze tekstu w systemie operacyjnym Linux/Unix. Nowy plik skryptu AWK można utworzyć w następujący sposób.

```
$ vi script.awk
```

Spowoduje to otwarcie pliku AWK w edytorze tekstu. Wprowadź kilka instrukcji w edytorze tekstu w następujący sposób.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Pierwszy wiersz tej treści tekstowej jest wyjaśniony w następujący sposób.

* \#! – określany jako „Shebang”, który określa interpreter instrukcji w skrypcie
* /usr/bin/awk – jest interpreterem
* -f – opcja interpretera, używana do odczytu pliku programu

## Jak wykonać skrypt AWK?

Zapisz plik i spraw, aby skrypt był wykonywalny, wydając poniższe polecenie:
```
$ chmod +x script.awk
```

Skrypt można następnie uruchomić w następujący sposób.

```
$ ./script.awk
```

co skutkuje następującym wyjściem.

```
Writing my first Awk executable script!
```

## Odniesienie ##

* [Pisanie skryptów przy użyciu języka programowania Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

