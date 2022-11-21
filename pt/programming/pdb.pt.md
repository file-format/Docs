{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PDB - um arquivo de banco de dados do programa",
  "description":"Saiba mais sobre o formato de arquivo PDB e APIs que podem criar e abrir arquivos PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo PDB?

Um arquivo com extensão .pdb é um arquivo de banco de dados de programa que contém informações de depuração para um executável compilado (EXE/DLL). Os arquivos PDB são gerados por compiladores da Microsoft quando um programa de aplicativo é compilado no modo de depuração. A presença do arquivo PDB pode ajudar na engenharia reversa de um executável, pois contém informações significativas sobre todos os símbolos dos módulos. É por esse motivo que esses arquivos são mantidos separados do executável final. A [API DgbHelp] da Microsoft (https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) pode abrir um arquivo PDB para obter informações como públicos e exportações, símbolos globais, símbolos locais, tipo de dados, arquivos de origem e números de linha.

## Formato de arquivo PDB

PDB é o formato de arquivo proprietário da Microsoft e ainda não foi documentado oficialmente em nenhum lugar. No entanto, uma documentação inicial está disponível [aqui](https://github.com/Microsoft/microsoft-pdb) e pode ser referenciada.

### Fluxos PDB

Os arquivos PDB consistem em vários fluxos em que cada fluxo atua como um arquivo individual virtual e contém informações. Os gravadores de arquivos PDB podem gravar nesses arquivos e o arquivo é finalizado somente após a emissão de um commit explícito. Um compilador pode continuar gravando em um arquivo PDB, mas confirmar apenas se todo o código do usuário for compilado com êxito. Um arquivo PDB consiste nos seguintes fluxos:

|Número do fluxo |Conteúdo |Descrição curta|
---|---|---|
|1| Pdb (header) |Informações de versão e informações para conectar este PDB ao EXE|
|2| Tpi (Gerenciador de tipos) |Todos os tipos usados no executável.|
|3| Dbi (Informações de depuração) |Retém contribuições de seção e lista de 'Mods'|
|4| NomeMapa| Contém uma tabela de strings com hash|
|4-(n+4)| n Mod's (informações do módulo)| Cada stream Mod contém símbolos e números de linha para um compiland|
|n+4| Símbolo global hash| Um índice que permite pesquisar em símbolos globais por nome|
|n+5| Hash de símbolo público| Um índice que permite pesquisar em símbolos públicos por endereços|
|n+6| Registros de símbolos| Registros de símbolos reais de símbolos globais e públicos|
|n+7| Digite hash| Hash usado pelo fluxo TPI.|

Cada fluxo em um arquivo PDB é composto por várias páginas que não são necessariamente numeradas consecutivamente.

### Cabeçalho do PDB

Um arquivo PDB começa com um Header que consiste em uma assinatura para identificar e validar o formato específico. O comprimento da assinatura depende do formato PDB. O cabeçalho pode ser maior que uma única página.

### Metadados PDB
Os metadados do PDB são responsáveis por reconhecer todos os fluxos componentes, fornecendo o comprimento e a sequência de páginas de cada fluxo. Ordens são dadas aos streams consecutivamente; começando com 0. Há também um fluxo raiz não ordenado, que contém alguns dos metadados.

## Referências
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

