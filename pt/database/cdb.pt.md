{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "extensão", "arquivo cdb", "formato de arquivo cdb", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "o que é um arquivo cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo CDB e APIs que podem criar e abrir arquivos CDB.",
  "title" :"CDB - Arquivo de Banco de Dados Constante",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## O que é um arquivo CDB?
Os arquivos CDB são usados em aplicativos de missão crítica, como e-mail. O CDB significa "banco de dados constante", um pacote rápido, confiável e simples para criar ou ler bancos de dados constantes. A substituição do banco de dados é segura contra falhas do sistema. Os usuários não precisam pausar durante uma reescrita. O CDB funciona como uma matriz associativa (no disco), mapeando chaves para valores e permite que vários valores sejam armazenados em uma única chave.

## Formato de arquivo CDB
O formato de arquivo CDB armazena números, deslocamentos, comprimentos e valores de hash no formato little endian como inteiros de 32 bits sem sinal. Chaves e dados são considerados strings de bytes opacas sem tratamento especial. No início do banco de dados, o cabeçalho de tamanho fixo representa 256 tabelas de hash, listando sua posição dentro do arquivo e seu comprimento em slots. Normalmente, os dados são armazenados como uma sequência de registros, cada registro armazena o comprimento da chave, o comprimento dos dados, a chave e os dados. Não há regras de classificação ou alinhamento. Os registros são seguidos por um conjunto de 256 tabelas de hash de comprimentos variados. Como zero é um comprimento válido, pode haver menos de 256 tabelas de hash fisicamente armazenadas no banco de dados, mas não há nada considerado como 256 tabelas. As tabelas de hash consistem em uma série de slots, cada um contendo um valor de hash e um deslocamento de registro. "Slots vazios" têm um deslocamento de zero.

### Estrutura
O banco de dados CDB consiste em um conjunto de dados inteiro em um único arquivo de computador. Ele contém três partes:
- Um cabeçalho de tamanho fixo
- Dados
- Um conjunto de tabelas de hash.

As pesquisas estão disponíveis apenas para chaves exatas. As pesquisas agem usando o seguinte algoritmo:

- Hash a chave.
- Determine em qual tabela de hash e slot esse registro deve estar localizado.
- Teste o slot indicado na tabela de hash.

Para pesquisas de chaves com mais de um valor, valores adicionais podem ser encontrados simplesmente retomando a pesquisa no próximo slot.

#### Características

A estrutura do banco de dados CDB fornece vários recursos:

##### Pesquisas rápidas
Uma pesquisa bem-sucedida em um banco de dados enorme normalmente leva apenas dois acessos ao disco e uma pesquisa malsucedida leva apenas um.
##### Baixa sobrecarga
Um banco de dados usa 2048 bytes, 24 bytes por registro e o espaço para chaves e dados.
##### Sem limites aleatórios
O CDB pode gerenciar qualquer banco de dados de até 4 gigabytes. Como não há outras restrições, os registros nem precisam caber na memória. Os bancos de dados são armazenados em um formato independente de máquina.
##### Substituição rápida de banco de dados atômico
O comando **cdbmake** pode reescrever um banco de dados inteiro em duas ordens de grandeza, mais rápido que outros pacotes de hash.
##### Despejos rápidos de banco de dados
**cdbdump** pode imprimir o conteúdo de um banco de dados em formato compatível com cdbmake.


## Referências ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [especificação do CDB](http://cr.yp.to/cdb.html)

