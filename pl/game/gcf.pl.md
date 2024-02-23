{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku GCF i interfejsach API, które umożliwiają tworzenie i otwieranie plików GCF.",
  "title" : "Plik GCF — format GCF gry Nadeo",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-pl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Czym jest plik GCF?

Plik .gcf to plik pamięci podręcznej gry używany przez platformę gier Steam. Zawiera dane gry, takie jak tekstury, modele i inne pliki używane przez grę. Pliki te są przechowywane na komputerze użytkownika i służą do zmniejszenia ilości danych, które należy pobrać podczas aktualizacji lub instalacji gry. Plików .gcf można także używać do tworzenia kopii zapasowych instalacji gry lub do przesyłania gry między komputerami.

Pliki GCF można odczytywać i zapisywać za pomocą biblioteki programowania Open Source C++, **HLLib**.

## Format pliku GCF

Pliki GCF są zapisywane na dysku jako pliki binarne. GCF był pierwotnie używany jako akronim pliku Grid Cache File (wczesna nazwa kodowa Steam brzmiała Grid), ale później został przyjęty jako Game Cache File. Plik GCF to plik archiwum przechowujący gry Steam. Cała oficjalna zawartość jest pobierana jako pliki GCF. Pliki GCF można również udostępniać między grami.

UWAGA: GCF jest poprzednikiem [VPK file format](/game/vpk/).
## Bibliografia

* [Oprogramowanie Valve](https://www.valvesoftware.com/en/)

* [Format pliku GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib — biblioteka programowania C++ typu open source do odczytu plików GCF](https://developer.valvesoftware.com/wiki/HLLib)


