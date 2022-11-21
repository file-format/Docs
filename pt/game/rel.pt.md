{
  "date" : "2021-09-08",
  "keywords" :[ "arquivo rel", "formato de arquivo rel", "o que é um arquivo rel", "arquivo", "exemplo rel", "extensão de arquivo rel", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo REL e APIs que podem criar e abrir arquivos REL.",
  "title" :"REL - Arquivo de Módulo Relocável",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## O que é um arquivo REL?
Um arquivo com extensão .rel pode ser utilizado para diversos fins. Portanto, em termos de classificação de jogos, é conhecido como um arquivo de módulo relocável usado por alguns jogos do Nintendo Wii, como Brawl, Super Smash Bros e Mario Kart Wii. Ele compreende os dados de jogabilidade, incluindo modelos de personagens e estágios. Os arquivos REL funcionam de maneira semelhante aos arquivos .DLL usados pelo Microsoft Windows.

## Formato de arquivo REL
Em um formato de arquivo REL, o arquivo é dividido em várias seções, agrupadas por acesso semelhante, por exemplo, dados somente leitura em uma seção, todo o código executável é colocado em outra, etc. O arquivo começa com uma seção de cabeçalho, seguida por:
- Tabela contendo informações da seção.
- Os dados da seção.
- Informações de realocação.

### Cabeçalho do arquivo
O arquivo começa com um cabeçalho de até 0x4C bytes:
| Deslocamento | Tamanho | Nome do campo | Descrição |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | identificação | Número de identificação arbitrário. Deve ser único entre todos os RELs usados por um jogo. Não deve ser 0. |
| 0x04 | 4 | próximo | Ponteiro para o próximo módulo, preenchido em tempo de execução. |
| 0x08 | 4 | anterior | Ponteiro para o módulo anterior, preenchido em tempo de execução. |
| 0x0c | 4 | numSecções | Número de seções no arquivo. |
| 0x10 | 4 | seçãoInfoOffset | Deslocamento para o início da tabela de seção. |
| 0x14 | 4 | nomeDeslocamento | Deslocamento para string ASCII contendo o nome do módulo. Pode ser NULO. Relativo ao início do arquivo REL. |
| 0x18 | 4 | nomeTamanho | Tamanho do nome do módulo em bytes. |
| 0x1c | 4 | versão | Número da versão do formato de arquivo REL. |
| 0x20 | 4 | bssTamanho | Tamanho da seção '.bss'. |
| 0x24 | 4 | relOffset | Deslocamento para a tabela de realocação. |
| 0x28 | 4 | impOffset | Deslocamento para a tabela imp. |
| 0x2c | 4 | impSize | Tamanho da tabela imp em bytes. |
| 0x30 | 1 | prólogoSeção | Índice na tabela de seção a qual prólogo é relativo. Ignore se este campo for 0. |
| 0x31 | 1 | epilogSecção | Índice na tabela de seção a qual epílogo é relativo. Ignore se este campo for 0. |
| 0x32 | 1 | Seção não resolvida | Índice na tabela de seção à qual não resolvido é relativo. Ignore se este campo for 0. |
| 0x33 | 1 | bssSeção | Índice na tabela de seção à qual bss é relativo. Preenchido em tempo de execução! |
| 0x34 | 4 | prólogo | Desloque na seção especificada da função _prolog. |
| 0x38 | 4 | epílogo | Desloque na seção especificada da função _epilog. |
| 0x3c | 4 | não resolvido | Desloque na seção especificada da função _unresolved. |
| 0x40 | 4 | alinhar | Versão ≥ 2 apenas. Restrição de alinhamento em todas as seções, expressa como potência de 2. |
| 0x44 | 4 | bssAlinhar | Versão ≥ 2 apenas. Restrição de alinhamento em toda a seção '.bss', expressa como potência de 2. |
| 0x48 | 4 | fixSize | Versão ≥ 3 apenas. Se REL estiver vinculado a OSLinkFixed (em vez de OSLink), o espaço após esse endereço pode ser usado para outros fins (como BSS). |

### Tabela de informações da seção
A tabela de informações da seção contém entradas **numSections**, cada uma com 0x8 bytes de comprimento:
| Deslocamento | Tamanho | Descrição |
-------|------------|-------------|
| 0x0 | 30 bits | Offset do início do REL para a seção. Se for zero, a seção é uma seção não inicializada (ou seja, .bss). |
| 0x3.6 | 1 bit | Desconhecido. |
| 0x3,7 | 1 bit | Sinalizador executável; se for 1, a seção é executável. |
| 0x4 | 4 | Comprimento em bytes da seção. Se for zero, esta entrada será ignorada. |
| 0x8 | Próxima entrada | Próxima entrada |

### Dados de realocação
Os dados de realocação são uma ou mais listas de estruturas de 0x8 bytes. O final de cada lista é marcado pelo código de tipo especial 203:
| Deslocamento | Nome | Tamanho | Descrição |
-------|------------|------------|-----|
| 0x0 | deslocamento | 2 | Deslocamento em bytes da realocação anterior para esta. Se esta for a primeira realocação na seção, isso é relativo ao início da seção. |
| 0x2 | tipo | 1 | O tipo de realocação. Descrito abaixo. |
| 0x3 | seção | 1 | A seção do símbolo para a qual se deslocar. Para o tipo de realocação especial 202, este é o número da seção neste arquivo à qual as seguintes entradas de realocação se aplicam. |
| 0x4 | adendo | 4 | Deslocamento em bytes do símbolo para realocar, em relação ao início de sua seção. Este é um endereço absoluto para realocações em relação a main.dol. |
| 0x8 | Próxima entrada | Próxima entrada | Próxima entrada |


 




## Referências


* [Formato do módulo de objeto realocável](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


