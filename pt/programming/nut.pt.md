{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "arquivo", "extensão", "formato de arquivo", "linguagem de programação NUT", "Guia de programação", "exemplo NUT", "formato de arquivo NUT", "linguagem esquilo", "arquivo de extensão .nut ", "arquivos NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Arquivo de linguagem do esquilo",
  "description":"Saiba mais sobre o formato de arquivo NUT e APIs que podem criar e abrir arquivos NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## O que é um arquivo NUT?

O NUT refere-se ao arquivo NUT Open Container Format. Este formato de arquivo NUT pertence à linguagem de programação conhecida como Esquilo. É uma linguagem de programação orientada a objetos, de alto nível e imperativa, usada principalmente em sistemas embarcados e videogames.

A linguagem squirrel é considerada uma linguagem de script leve que pode ser facilmente ajustada de acordo com o tamanho e a largura de banda. Envolve a vantagem da contagem automática de referência e o gerenciamento de lixo na memória.

A sintaxe da linguagem squirrel atrai os desenvolvedores, pois é semelhante a C e envolve o recurso de linguagem de script. Mas ainda assim, tem muito menos vantagens em comparação com outras linguagens de programação mais populares para esse fim.



## Breve história ##

Ela foi projetada por Alberto Demichelis em 2003. No entanto, uma versão estável dessa linguagem foi lançada em 2016. Ela foi projetada sob a licença de zlib/libpng. Em 2010 a licença foi alterada e transferida para o MIT. Esta linguagem é considerada uma versão inspirada de [LUA](/pt/programming/lua/) (linguagem de programação). Há uma lista de sugestões para o antigo idioma no site criado por Alberto para torná-lo mais vantajoso.


## Especificação técnica ##

O recurso e as especificações da linguagem do esquilo são múltiplos. Oferece a facilidade de tipagem dinâmica, propriedade de delegação, diversos usos de classes e interfaces. A sintaxe desta linguagem tem uma semelhança com a sintaxe da linguagem C. Aplicativos como Enduro/X (um servidor de aplicativos de cluster) usam essa linguagem. Como o Squirrel também é usado para videogames, alguns deles são OpenTTD, GTA IV, etc.

A versão estável da linguagem é 3.0.7. Um kit de ferramentas conhecido como MirthKit usa a linguagem de programação Squirrel para fornecer um código aberto e plataforma cruzada para jogos bidimensionais. A natureza dessa linguagem é dinâmica e a maioria dos recursos semelhantes a [Python](/pt/programming/py/), LUA, etc. Ela também envolve a implementação de VM baseada em registro. O desempenho do Squirrel é mais lento em comparação com o LUA.

Há também outro tipo de arquivo de extensão ".nut" e é por isso que você deve verificar o tamanho do arquivo para descobrir qual arquivo NUT você possui. Os arquivos NUT de script de esquilo são geralmente menores que 1 MB, enquanto os arquivos NUT de vídeo geralmente são maiores que 1 MB de tamanho.


## Exemplo de formato de arquivo NUT ##

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

## Referência ##

* [NUT - por Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



