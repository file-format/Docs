{
  "date" : "2021-06-24",
  "keywords" :["CZĘŚĆ", "częściowe", "rozszerzenie", "plik", "format", "sieć", "pobrane"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CZĘŚĆ - Częściowo pobrany plik",
  "description":"Dowiedz się o formacie pliku PART i interfejsach API, które mogą tworzyć i otwierać pliki PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Czym jest plik PART? ##

Plik części lub rozszerzenie .part to częściowo pobrany plik. Jest używany, gdy pobieranie jest w toku lub zostało przerwane z powodu jakiegokolwiek problemu, dając menedżerowi pobierania możliwość wznowienia pobierania, gdy tylko jest to możliwe.
Oznacza to, że przeglądarka, taka jak Firefox lub programy do przesyłania plików, takie jak eMule, eMule plus, FlashGet itp. przechowuje część pliku, zwaną plikiem części, podczas gdy pobieranie odbywa się na urządzeniu. Ten plik części pokaże, czy pobieranie jest w toku, czy zostało przerwane przed zakończeniem. Nie tylko to, ale plik PART przechowuje wszystkie dane do zakończenia pobierania, dlatego niektóre z nich można później wznowić, jeśli chcesz ponownie rozpocząć pobieranie.

## Format pliku CZĘŚCI ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
