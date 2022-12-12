{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku FZPZ - Plik części Fritzing",
  "description":"Dowiedz się, co to jest plik FZPZ i interfejsy API, które mogą tworzyć i otwierać pliki FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Czym jest plik FZPZ?

Plik FZPZ to komponent/część używana w projektowaniu obwodów elektronicznych utworzonych za pomocą aplikacji do prototypowania obwodów i projektowania **Fritzing**. Jest to skompresowane archiwum zawierające plik [FZP](/pl/cad/fzp/) i cztery obrazy [SVG](/pl/image/svg/) opisujące całość we Fritzing. Zaletą korzystania z tych plików jest to, że użytkownicy mogą udostępniać swoje pliki FZPZ każdemu z punktu widzenia ponownego użycia. Udostępnianie części FZPZ pomaga w integracji części obwodów w celu szybkiego tworzenia większych projektów PCB.

## Format pliku FZPZ — więcej informacji

Pliki FZPZ są zapisywane na dysku jako skompresowane archiwa [ZIP](/pl/compression/zip/). Możesz zmienić nazwę rozszerzenia z .fzpz na .zip i użyć dowolnego standardowego narzędzia do dekompresji, takiego jak WinZIP, aby wyodrębnić pliki z archiwum.

### Informacje o strukturze pliku FZPZ

Jak wspomniano, plik FZPZ to plik archiwum, który zawiera wiele plików do reprezentacji części używanej na płytce drukowanej. FZPZ zawiera następujące pliki:

* `Cztery pliki SVG` - reprezentujące płytkę prototypową części, schematy, PCB i obrazy ikon
* `Plik FZP` — plik XML zawierający informacje o właściwościach części, złączach i magistralach

Pliki są zwykle nazywane w następujący sposób.

* część.plik.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematyczny.plik.svg

## Bibliografia ##

* [Nowe części z rozszerzeniem fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

