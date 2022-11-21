{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "arquivo", "extensão", "formato de arquivo", "Valores separados por vírgula", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo CSV e as APIs que podem criar e abrir arquivos CSV.",
  "title" :"Formato de arquivo CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo CSV?

Arquivos com extensão .csv (valores separados por vírgula) representam arquivos de texto simples que contêm registros de dados com valores separados por vírgula. Cada linha em um arquivo CSV é um novo registro do conjunto de registros contido no arquivo. Esses arquivos são gerados quando a transferência de dados é pretendida de um sistema de armazenamento para outro. Como todos os aplicativos podem reconhecer registros separados por vírgula, a importação desses arquivos de dados para o banco de dados é feita de forma muito conveniente. Quase todos os aplicativos de planilhas, como o Microsoft Excel ou o OpenOffice Calc, podem importar CSV sem muito esforço. Os dados importados desses arquivos são organizados em células de uma planilha para representação ao usuário.

## Breve história ##

A seguir estão alguns fatos rápidos sobre a origem e o histórico do formato de arquivo CSV.

* 1972 - O compilador IBM Fortran (nível H estendido) os suportava no OS/360

* 1978 - A entrada/saída direcionada por lista foi suportada pelo FORTRAN 77 que usava vírgulas e espaços para delimitadores

* 2005 - CSV foi padronizado com [RFC4180](https://tools.ietf.org/html/rfc4180) como um tipo de conteúdo MIME.

* 2013 - As deficiências do RFC4180 foram tratadas por uma recomendação do W3C

* 2015 - W3C fez os primeiros rascunhos de recomendações para padrões de metadados CSV, que começaram como recomendação em dezembro de 2015

## Converter arquivos CSV ##

Os arquivos CSV podem ser convertidos em vários formatos de arquivo diferentes usando os aplicativos que podem abrir esses arquivos. Por exemplo, o Microsoft Excel pode importar dados do formato de arquivo CSV e salvá-los em XLS, [XLSX](/pt/spreadsheet/xlsx/), [PDF](/pt/pdf/), [TXT](/pt/word-processing/txt/) , XML e formatos de arquivo [HTML](/pt/web/html/). Da mesma forma, outros serviços de desktop e online oferecem a capacidade de exportar arquivos CSV para HTML, ODS e [RTF](/pt/word-processing/rtf/).

## Formato de arquivo CSV ##

O formato de arquivo CSV é conhecido por ser especificado em [RFC4180](https://tools.ietf.org/html/rfc4180). Ele define qualquer arquivo para ser compatível com CSV se:

* Cada registro está localizado em uma linha separada, delimitada por uma quebra de linha (CRLF). Por exemplo:
*aaa,bbb,cc CRLF
* zzz,yyy,xxx CRLF
* O último registro no arquivo pode ou não ter uma quebra de linha final. Por exemplo:
*aaa,bbb,cc CRLF
* zzz, aaaa, xxx
* Pode haver uma linha de cabeçalho opcional aparecendo como a primeira linha do arquivo com o mesmo formato das linhas de registro normais. Este cabeçalho conterá nomes correspondentes aos campos do arquivo e deverá conter o mesmo número de campos que os registros do restante do arquivo (a presença ou ausência da linha do cabeçalho deverá ser indicada através do parâmetro opcional "header" deste tipo MIME). Por exemplo:
* field_name,field_name,field_name CRLF
*aaa,bbb,cc CRLF
* zzz,yyy,xxx CRLF
* ﻿Dentro do cabeçalho e de cada registro, pode haver um ou mais campos, separados por vírgulas. Cada linha deve conter o mesmo número de campos em todo o arquivo. Os espaços são considerados parte de um campo e não devem ser ignorados. O último campo do registro não deve ser seguido de vírgula. Por exemplo:
*aaa,bb,cc
* Cada campo pode ou não estar entre aspas duplas (no entanto, alguns programas, como o Microsoft Excel, não usam aspas duplas). Se os campos não estiverem entre aspas duplas, as aspas duplas podem não aparecer dentro dos campos. Por exemplo:\
* "aaa","bbb","ccc" CRLF
* zzz, aaaa, xxx
* Os campos contendo quebras de linha (CRLF), aspas duplas e vírgulas devem ser colocados entre aspas duplas. Por exemplo:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz, aaaa, xxx
* Se aspas duplas forem usadas para incluir campos, as aspas duplas que aparecem dentro de um campo devem ser precedidas por outra aspa dupla. Por exemplo:
* "aaa","b""bb","ccc"

No entanto, à luz do uso moderno, o delimitador não se limita apenas à vírgula e também pode ser ponto e vírgula, tabulação ou espaços. Aplicativos como o Microsoft Excel oferecem a opção de especificar o caractere delimitador para importar registros de um arquivo CSV.

## Referências

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

