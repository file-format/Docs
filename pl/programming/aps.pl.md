{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Plik zasobów Visual C++",
  "description":"Poznaj format pliku APS z przykładem APS i interfejsami API, które mogą tworzyć i otwierać pliki APS.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Co to jest format pliku APS?
Plik APS jest tworzony przez Visual C++, aplikację do tworzenia oprogramowania firmy Microsoft. Zapisuje binarną reprezentację zasobu włączoną do projektu i pozwala aplikacji na szybsze ładowanie zasobów. Możesz łatwo znaleźć te pliki z rozszerzeniem .aps. W rzeczywistości edytory zasobów nie odczytują bezpośrednio plików resource.h, dlatego kompilator zasobów kompiluje je w pliki .aps, które są używane przez edytory zasobów.

## Format pliku APS
Format pliku APS to tylko krok kompilacji i przechowuje tylko dane symboliczne. Informacje niesymboliczne, takie jak komentarze, są odrzucane podczas procesu kompilacji. Na przykład podczas zapisywania edytor zasobów zastępuje plik skryptu zasobu i plik zasobu.h. Wszelkie zmiany w samych zasobach pozostają uwzględnione w pliku skryptu zasobów, ale komentarze zawsze zostaną utracone po zastąpieniu pliku skryptu zasobów.


## Bibliografia

* [Pliki zasobów (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


