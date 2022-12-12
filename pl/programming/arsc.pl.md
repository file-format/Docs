{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "co to jest plik arsc", "jak otworzyć plik arsc", "rozszerzenie", "plik", "plik arsc", "format pliku arsc", "rozszerzenie pliku arsc" ,"Przykład pliku arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - plik tabeli zasobów pakietu Android",
  "description":"Poznaj format pliku ARSC i interfejsy API, które mogą tworzyć i otwierać plik ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Czym jest plik ARSC?

Plik ARSC to plik tabeli zasobów systemu Android, który zawiera listę zasobów aplikacji w formacie tabeli. Zawiera informacje, takie jak nazwy zasobów, właściwości i identyfikatory. Pliki ARSC są częścią pakietów APK używanych do instalowania tych aplikacji na Androida. Wszystkie zasoby, takie jak obrazy, układy, style i ciągi znaków w aplikacji na Androida są konwertowane na pliki binarne podczas generowania pliku APK. W tym samym czasie generowany jest również plik ARSC, zawierający listę wszystkich skompilowanych zasobów programu i ich identyfikatory.

## Format pliku ARSC

Pliki z rozszerzeniem .arsc to pliki binarne generowane po tym, jak kompilator, taki jak ANT (Eclipse) lub Gradle (AS), kompiluje kod aplikacji systemu Android w celu utworzenia pliku [APK](/pl/compression/apk/). Możesz wyodrębnić plik APK za pomocą dowolnego narzędzia do archiwizacji, takiego jak WinZip, aby wyświetlić jego zawartość, którą są skompilowane pliki klas java, tj.classs.dex. Oprócz tego zawiera również ten plik ARSC, który zawiera metainformacje o:

* Węzły XML
* Atrybuty
* Identyfikatory zasobów

Zasoby w pliku APK są określane przez identyfikatory zasobów, podczas gdy atrybuty są rozpoznawane na wartości w czasie wykonywania. Narzędzie Android aapt zbiera wszystkie zasoby zdefiniowane w plikach w czasie kompilacji i przypisuje im identyfikatory zasobów. Po nadaniu identyfikatorów skompilowanym zasobom z kodu źródłowego oraz pliku resources.arsc generowany jest plik R.java.

## Bibliografia

* [Struktura tabeli zasobów binarnych] (https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

