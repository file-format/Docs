{
  "date" : "2020-03-16",
  "keywords" :[ "Arquivo PAT", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo PAT e APIs que podem criar e abrir arquivos PAT.",
  "title" :"Formato de arquivo PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## O que é um arquivo PAT?

Um arquivo com extensão .pat é um arquivo CAD usado pelo software AutoCAD. Os aplicativos que podem abrir arquivos PAT usam o padrão de hachura armazenado nesses arquivos para obter informações sobre a textura/preenchimento de uma área. Os padrões contidos fornecem informações sobre a aparência do material para objetos desenhados. Os arquivos PAT podem ser abertos em aplicativos como Autodesk AutoCAD, CorelDRAW Graphics Suite e Ketron Software. Os arquivos PAT podem ser convertidos em diferentes formatos de imagem, como JPG, PNG, BMP, etc.

## Formato de arquivo PAT

Os arquivos PAT são escritos em formato de texto simples e podem ser abertos em qualquer editor de texto. Os padrões de hachura nesses arquivos são baseados em vetores e seguem a sintaxe descrita pela documentação do AutoCAD.

Todos os padrões começam no ponto 0,0, o padrão é calculado para cobrir o limite de hachura.

### Definição de padrão

Todas as definições de padrão consistem nos seguintes campos:
* Uma liderança '\*'
* Um nome - O nome não pode ter espaços, sinais de pontuação, parênteses ou barras.
* Uma descrição

O formato padrão para padrões de hachura é `<\*><name> <, descrição>`. O nome e a descrição são separados por uma vírgula e as descrições não podem exceder o comprimento da linha de oitenta caracteres. Os padrões de hachura são definidos após esta informação.

### Exemplos de padrões de hachura
A seguir está um exemplo de padrão quadrado
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Outro exemplo que mostra o padrão de paralelogramo é o seguinte.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referências ##

* [Padrões de hash da Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

