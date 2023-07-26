{
  "date" : "2021-07-29",
  "keywords" :[ "arquivo shx", "formato de arquivo shx", "o que é um arquivo shx", "arquivo", "exemplo shx", "extensão de arquivo shx", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile Shape Index Format",
  "description":"Saiba mais sobre o formato de arquivo SHX e APIs que podem criar e abrir arquivos SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## O que é um arquivo SHX?
O arquivo SHX pertence ao formato de índice de forma, que é um índice posicional da geometria do recurso para permitir a busca para frente e para trás rapidamente. O SHX é um arquivo de deslocamento de acesso direto. Não há dados neste arquivo, apenas uma cópia duplicada dos primeiros cem bytes, número do registro e deslocamento para o byte inicial desse registro no shp. Observe que o arquivo com extensão .shx não vincula o [SHP](/pt/gis/shp/) e o [DBF](/pt/database/dbf/).

## Formato de arquivo SHX
O formato SHX contém o índice posicional da geometria do recurso e o cabeçalho de 100 bytes semelhante ao arquivo SHP, seguido por qualquer número de registros de comprimento fixo de 8 bytes que contêm os dois campos a seguir:
| Bytes | Tipo | Endianidade | Uso |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | grande | Deslocamento de registro (em palavras de 16 bits) |
| 4–7 | int32 | grande | Comprimento do registro (em palavras de 16 bits) |

Este índice torna possível buscar para trás no shapefile, primeiro, buscando para trás no índice de forma e depois lendo o deslocamento do registro. Esse deslocamento pode ser usado para buscar a posição correta no arquivo SHP. Você também pode buscar para a frente; um número arbitrário de registros usando o mesmo método. Embora seja possível gerar um índice completo junto com um arquivo SHP, mas pode aumentar as chances de corromper o arquivo SHP rapidamente.


## Referências

* [Shapefile - por Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


