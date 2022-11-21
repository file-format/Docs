{
  "date" : "2021-09-08",
  "keywords" :[ "arquivo pcc", "formato de arquivo pcc", "o que é um arquivo pcc", "arquivo", "exemplo pcc", "extensão de arquivo pcc", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo Mass Effect PCC e APIs que podem criar e abrir arquivos PCC.",
  "title" :"PCC - Arquivo de pacote de efeito de massa",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## O que é um arquivo PCC?

Um arquivo com .pcc é um arquivo [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) que contém dados do jogo para modificar o conteúdo do jogo, como modelos, texturas e quartos. Mass Effect 2 e 3 são os primeiros jogos de tiro baseados no motor de jogo Unreal Engine 3. O jogo foi desenvolvido inicialmente pela [Bioware](https://www.bioware.com/about/) que manteve a maioria dos recursos do jogo em seu formato de arquivo PCC proprietário. A Bioware foi adquirida pela Electronic Arts, uma editora líder global de entretenimento interativo.

## Formato de arquivo PCC - Mais informações

Os arquivos PCC contêm estruturas compactadas e/ou não compactadas que contribuem para a organização geral do arquivo.

### Estrutura de PCC compactada

Um arquivo PCC compactado é composto por tabelas e dados que são segmentados em partes. Cada pedaço contém um número variável de blocos compactados.

* `Chunks Header` - Um cabeçalho comum de 16 bytes, contendo informações sobre os pedaços.
* `Chunk Header` - Um cabeçalho de 16 bytes contendo informações sobre os dados brutos compactados contidos no formulário de bloco.

### Estrutura PCC não compactada

Os arquivos PCC não compactados são divididos nas cinco partes a seguir.

* `Header` - contém informações básicas sobre a estrutura do arquivo PCC.
* `Tabela de Nomes` - contém o nome encontrado dentro do pacote, incluindo classes de importação, exportações e propriedades de exportação.
* `Import Table` - contém todas as classes e objetos importados pelo PCC.
* `Export Table` - contém todos os objetos armazenados no pacote. Cada exportação pode variar em tamanho.

## Referências

* [Me3Explorer - Formato de arquivo PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Jogo Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

