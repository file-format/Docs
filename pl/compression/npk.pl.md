{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku NPK",
  "description":"Dowiedz się o formacie pliku NPK i interfejsach API, które mogą tworzyć i otwierać pliki NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Czym jest plik NPK?

Plik NPK to plik pakietu aktualizacji oprogramowania używany przez routery **MikroTik** do aktualizacji systemu operacyjnego routera. Występuje jako skompresowane archiwum binarne, które jest ładowane do routera w celu zainstalowania aktualizacji oprogramowania. Informacje zawarte w plikach NPK obejmują informacje o sieci, takie jak adres IP i usługa IP, informacje o złączach (interfejsy Ethernet i port szeregowy), konfiguracja poczty e-mail, konfiguracja mostu i lokalne zarządzanie użytkownikami.

## Format pliku NPK

Pliki NPK są przechowywane jako skompresowane archiwum binarne. Jest to zamknięty format pliku, który jest używany tylko przez samą firmę MikroTik. Nie jest przeznaczony do tworzenia dodatków RouterOS za pośrednictwem stron trzecich. Pliki NPK są obsługiwane przez samą firmę MikroTik, a ich zaktualizowane wersje można pobrać z sekcji pobierania witryny [MikroTik](https://mikrotik.com/download).

Gdy plik NPK zostanie przesłany do routera, system operacyjny routera nie zacznie działać, dopóki nie zostanie ponownie uruchomiony. Dlatego ponowne uruchomienie jest wymagane, aby zaktualizować system operacyjny routera.

## Bibliografia

* [MikroTik - aktualizacja systemu operacyjnego routera](https://mikrotik.com/download)
* [Jak tworzyć pliki NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

