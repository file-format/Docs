{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "soubor", "přípona", "formát souboru", "jazyk programování NUT", "Průvodce programováním", "příklad NUT", "formát souboru NUT", "jazyk veverky", "soubor s příponou .nut", "soubory NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Squirrel Language File",
  "description":"Další informace o formátu souboru NUT a rozhraních API, která mohou vytvářet a otevírat soubory NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Co je soubor NUT?

NUT odkazuje na soubor NUT Open Container Format. Tento formát souboru NUT patří do programovacího jazyka, který je známý jako Squirrel. Jedná se o objektově orientovaný, na vysoké úrovni a imperativní programovací jazyk, který se používá převážně ve vestavěných systémech a videohrách.

Jazyk squirrel je považován za lehký skriptovací jazyk, který lze snadno upravit podle velikosti a šířky pásma. Zahrnuje výhodu automatického počítání referencí a správy odpadků v paměti.

Syntaxe jazyka squirrel přitahuje vývojáře, protože je podobná C a zahrnuje rys skriptovacího jazyka. Ale přesto má mnohem méně výhod ve srovnání s jinými populárnějšími programovacími jazyky pro tento účel.



## Stručná historie ##

Byl navržen Albertem Demichelisem v roce 2003. V roce 2016 však byla vydána stabilní verze tohoto jazyka. Byl navržen pod licencí zlib/libpng. V roce 2010 byla licence změněna a převedena na MPO. Tento jazyk je považován za inspirovanou verzi [LUA](/cs/programming/lua/) (Programovací jazyk). Na webových stránkách navržených Albertem, aby byl výhodnější, je seznam návrhů pro dřívější jazyk.


## Technické specifikace ##

Funkce a specifikace jazyka veverek jsou četné. Poskytuje možnost dynamického psaní, vlastnost delegování, několik použití tříd a rozhraní. Syntaxe tohoto jazyka je podobná syntaxi jazyka C. Aplikace jako Enduro/X (klastrový aplikační server) používají tento jazyk. Protože se Squirrel používá i pro videohry, některé z nich jsou OpenTTD, GTA IV atd.

Stabilní verze jazyka je 3.0.7. Sada nástrojů známá jako MirthKit používá programovací jazyk Squirrel k poskytování open-source a multiplatformních dvourozměrných her. Povaha tohoto jazyka je dynamická a většina funkcí je podobná [Pythonu](/cs/programming/py/), LUA atd. Zahrnuje také implementaci VM založených na registrech. Výkon Squirrel je pomalejší ve srovnání s LUA.

Existuje také další typ souboru s příponou ".nut", proto byste se měli podívat na velikost souboru, abyste zjistili, který soubor NUT máte. Soubory Squirrel script NUT jsou většinou menší než 1 MB, zatímco soubory NUT videa jsou obvykle větší než 1 MB.


## Příklad formátu souboru NUT ##

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

## reference ##

* [NUT – z Wikipedie](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



