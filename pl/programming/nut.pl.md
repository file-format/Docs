{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "plik", "rozszerzenie", "format pliku", "język programowania NUT", "Przewodnik po programowaniu", "przykład NUT", "format pliku NUT", "język wiewiórki", "plik rozszerzenia .nut ", "Pliki NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Wiewiórczy Plik Językowy",
  "description":"Poznaj format plików NUT i interfejsy API, które mogą tworzyć i otwierać pliki NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Czym jest plik NUT?

NUT odnosi się do pliku formatu otwartego kontenera NUT. Ten format pliku NUT należy do języka programowania znanego jako Wiewiórka. Jest to zorientowany obiektowo, imperatywny język programowania wysokiego poziomu, który jest używany głównie w systemach wbudowanych i grach wideo.

Język wiewiórki jest uważany za lekki język skryptowy, który można łatwo dostosować do rozmiaru i przepustowości. Wiąże się to z zaletą automatycznego liczenia referencji i zarządzania śmieciami w pamięci.

Składnia języka squirrel przyciąga programistów, ponieważ jest podobna do języka C i zawiera cechy języka skryptowego. Ale nadal ma znacznie mniej zalet w porównaniu z innymi bardziej popularnymi językami programowania do tego celu.



## Krótka historia ##

Został zaprojektowany przez Alberto Demichelisa w 2003 roku. Jednak stabilna wersja tego języka została wydana w 2016 roku. Został on zaprojektowany na licencji zlib/libpng. W 2010 roku licencja została zmieniona i przeniesiona do MIT. Ten język jest uważany za inspirowaną wersję [LUA](/pl/programming/lua/) (język programowania). Na stronie zaprojektowanej przez Alberto znajduje się lista sugestii dotyczących poprzedniego języka, aby uczynić go bardziej korzystnym.


## Specyfikacja techniczna ##

Cech i specyfikacji języka wiewiórki jest wiele. Zapewnia łatwość dynamicznego pisania, właściwość delegowania, kilka zastosowań klas i interfejsów. Składnia tego języka jest podobna do składni języka C. Aplikacje takie jak Enduro/X (serwer aplikacji klastrowych) używają tego języka. Ponieważ Wiewiórka jest również używana w grach wideo, niektóre z nich to OpenTTD, GTA IV itp.

Stabilna wersja języka to 3.0.7. Zestaw narzędzi znany jako MirthKit wykorzystuje język programowania Squirrel, aby zapewnić otwarte źródło i wieloplatformowość dla gier dwuwymiarowych. Natura tego języka jest dynamiczna, a większość funkcji podobna do [Python](/pl/programming/py/), LUA itp. Obejmuje również implementację VM opartego na rejestrach. Wydajność Squirrel jest wolniejsza w porównaniu do LUA.

Istnieje również inny typ pliku z rozszerzeniem „.nut”, dlatego powinieneś spojrzeć na rozmiar pliku, aby dowiedzieć się, który plik NUT posiadasz. Pliki Squirrel script NUT są przeważnie mniejsze niż 1 MB, podczas gdy pliki wideo NUT są zwykle większe niż 1 MB.


## Przykład formatu pliku NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Odniesienie ##

* [NUT – z Wikipedii](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



