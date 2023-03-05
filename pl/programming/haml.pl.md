{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku HAML - Plik kodu źródłowego Haml",
  "description":"Dowiedz się o formacie pliku HAML i interfejsach API, które mogą tworzyć i otwierać plik HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Czym jest plik HAML?

Plik HAML to plik języka znaczników abstrakcji HTML, który zawiera kod źródłowy napisany w języku [Haml](https://haml.info/). Może być używany jako zamiennik ERB (skrypty szablonów Ruby). Plik HAML zawiera kod źródłowy szablonu, który służy do generowania kodu HTML dokumentu internetowego. Pliki ERB można zastąpić, po prostu zastępując te pliki w folderze app/views na Haml, zmieniając rozszerzenie pliku. Pliki HAML można otwierać za pomocą dowolnego edytora tekstu, takiego jak Microsoft Notepad, Notepad ++, Apple TextEdit,

## Format pliku HAML

Pliki HAML to pliki źródłowe zapisane na dysku jako zwykłe pliki tekstowe. Zawiera kod napisany w składni HAML. HAML zastępuje tagi **<>** znakiem ***%**, aby uprościć i ułatwić kod. Pliki ERB są zastępowane przez HAML, jak pokazano w poniższym prostym przykładzie.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Przykład HAML

Poniżej znajduje się przykład Hello World przykład HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
który renderuje do następującego wyjścia HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Bibliografia

* [HAML – Github](https://github.com/haml/haml)

