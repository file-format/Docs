{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","arquivo", "formato", "tipo de arquivo", "extensão","o que é um arquivo 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo 3DS e as APIs que podem abrir e criar arquivos 3DS.",
  "title" :"Formato de arquivo 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é arquivo 3DS?

Um arquivo com extensão .3ds representa o formato de arquivo de malha 3D Sudio (DOS) usado pelo Autodesk 3D Studio. O Autodesk 3D Studio está no mercado de formatos de arquivo 3D desde a década de 1990 e agora evoluiu para o 3D Studio MAX para trabalhar com modelagem, animação e renderização 3D. Um arquivo 3DS contém dados para representação 3D de cenas e imagens e é um dos formatos de arquivo populares para importação e exportação de dados 3D. Ele considera informações como locais de câmera, dados de malha, informações de iluminação, configurações de viewport, dados de grupo de suavização, referências de bitmap e atributos para criar vértices e polígonos para renderizar uma cena.

## Formato de arquivo 3DS - Mais informações
Em sua base, o 3DS é um formato de arquivo binário e segue uma estrutura predefinida para armazenamento e recuperação de dados. O formato de arquivo binário permite que o formato de arquivo 3DS seja menor em comparação com os formatos de arquivo baseados em texto. Os dados dentro de um arquivo 3DS são armazenados na forma de pedaços.

### Parte 3DS

Cada pedaço em um arquivo 3DS é um bloco de dados que contém um ID, comprimento do bloco para localização do próximo bloco e os próprios dados. O ID do bloco permite que os leitores de formato de arquivo 3DS ignorem os blocos que não reconhecem. Também ajuda na extensibilidade do formato. Cada pedaço armazena informações relacionadas a formas, iluminação e informações de visualização que, juntas, renderizam a cena. Os pedaços são organizados em uma estrutura hierárquica em um arquivo 3DS e se assemelham a uma árvore de Objeto de Documento XML na representação.

**Chunk ID:** os primeiros dois bytes de um chunk representam um identificador de chunk que permite que o leitor do arquivo decida se deve considerá-lo durante a leitura ou ignorá-lo.

**Comprimento do fragmento:** o ID do fragmento é seguido por um inteiro de 4 bytes (em little-endian) que representa o comprimento do fragmento. Esse comprimento também inclui o comprimento dos dados, o comprimento de seus sub-blocos e o cabeçalho de 6 bytes.

**Carga útil:** o comprimento do bloco é seguido por bytes reais de dados para o bloco, seguidos por seus subpedaços na mesma estrutura hierárquica que pode ser estendida para vários níveis de profundidade.

### Estrutura de um pedaço

A estrutura hierárquica de um bloco simples é mostrada abaixo:

**Um pedaço**

|início|fim|tamanho|nome
--- | --- | --- | ---
|0|1|2|ID do bloco
|2|5|4|Próximo pedaço

Os pedaços têm uma hierarquia imposta a eles que é identificada por seu ID. Um arquivo 3ds tem o ID de bloco primário 4D4Dh. Este é sempre o primeiro pedaço do arquivo. Com no pedaço primário estão os pedaços principais.

**Pedaços Principais**

|id|Descrição
--- | ---
|3D3D|Início dos dados da malha do objeto.
|B000|Início dos dados do keyframer.

O ponteiro Next Chunk após o bloco de ID aponta para o próximo bloco principal.
Diretamente após um pedaço principal há outro pedaço. Isso pode ser qualquer outro tipo de pedaço permitido dentro de seu escopo de pedaços principais.
Para a descrição da malha (3D3D), eles podem ser múltiplos de.

**Subchunks of 3D3D - Mesh Block**


|id|Descrição
--- | ---
|1100|desconhecido
|1200|Cor de fundo.
|1201|desconhecido
|1300|desconhecido
|1400|desconhecido
|1420|desconhecido
|1450|desconhecido
|1500|desconhecido
|2100|Bloco de cor ambiente
|2200|nevoeiro?
|2201|nevoeiro?
|2210|nevoeiro?
|2300|desconhecido
|3000|desconhecido
|4000|Bloco de Objetos
|7001|desconhecido
|AFFF|desconhecido

**Subchunks of 4000 - Object Description Block**
O primeiro item do Subchunk 4000 é uma string ASCIIZ do nome dos objetos.
Lembre-se de que um objeto pode ser uma malha, uma luz ou uma câmera.

|id|Descrição
--- | ---
|4010|desconhecido
|4012|sombra?
|4100|Objeto Polígono Triangular
|4600|Luz
|4700|Câmera

## Referências

* [Formatos de arquivo de geometria - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS - Por Wikipedia](https://en.wikipedia.org/wiki/.3ds)

