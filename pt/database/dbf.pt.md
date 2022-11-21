{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extensão", "arquivo dbf", "formato de arquivo dbf", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "o que é um arquivo dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DBF e APIs que podem criar e abrir arquivos DBF.",
  "title" :"DBF - Arquivo de banco de dados dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## O que é um arquivo DBF?
O arquivo com extensão .dbf é um arquivo de banco de dados usado por um aplicativo de sistema de gerenciamento de banco de dados chamado **dBASE**. Inicialmente, o banco de dados dBASE foi nomeado como Project Vulcan; iniciado por **Wayne Ratliff** em 1978. O tipo de arquivo DBF foi introduzido com o dBASE II em 1983. Ele organiza vários registros de dados com campos do tipo Array. O software de banco de dados **xBase**, que é pupular devido à sua compatibilidade com uma ampla variedade de formatos de arquivo; também suporta os arquivos DBF.

## Formato de arquivo DBF
O formato de arquivo DBF pertence ao sistema de gerenciamento de banco de dados dBASE, mas pode ser compatível com xBase ou outros softwares DBMS. A versão inicial do arquivo dbf consistia em uma tabela simples que poderia ter dados adicionados, modificados, excluídos ou impressos usando o conjunto de caracteres ASCII. Com o passar do tempo, o .dbf foi aprimorado e arquivos adicionais foram adicionados para aumentar os recursos e capacidades do sistema de banco de dados.

No dBASE moderno, um arquivo DBF consiste em um cabeçalho, os registros de dados e o marcador EOF (End of File)

- O cabeçalho contém informações sobre o arquivo, como a quantidade de registros e a quantidade de tipos de campos utilizados nos registros.
- Os registros contêm os dados reais.
- O final do arquivo é marcado por um único byte, com valor 0x1A.

### Cabeçalho do arquivo
O layout do cabeçalho do arquivo no dBase é fornecido na tabela a seguir:

| Byte | Conteúdo | Significado |
---|---|---|
| 0 | 1 byte | dBASE válido para arquivo DOS; os bits 0–2 indicam o número da versão, o bit 3 indica a presença de um arquivo memo dBASE para DOS, os bits 4–6 indicam a presença de uma tabela SQL, o bit 7 indica a presença de qualquer arquivo memo (dBASE m PLUS ou dBASE para DOS) |
| 1–3 | 3 bytes | Data da última atualização; formatado como AAMMDD |
| 4–7 | número de 32 bits | Número de registros no arquivo de banco de dados |
| 8–9 | número de 16 bits | Número de bytes no cabeçalho |
| 10–11 | número de 16 bits | Número de bytes no registro |
| 12–13 | 2 bytes | Reservado; preencha com 0 |
| 14 | 1 byte | Sinalizador que indica transação incompleta[nota 1] |
| 15 | 1 byte | Sinalizador de criptografia[nota 2] |
| 16–27 | 12 bytes | Reservado para dBASE para DOS em um ambiente multiusuário |
| 28 | 1 byte | Sinalizador de arquivo .mdx de produção; 1 se houver um arquivo .mdx de produção, 0 se não houver |
| 29 | 1 byte | ID do driver de idioma |
| 30–31 | 2 bytes | Reservado; preencha com 0 |
| 32–n [nota 3][nota 4] | 32 bytes cada | array de descritores de campo (veja abaixo o layout dos descritores) |
| n + 1 | 1 byte | 0x0D como o terminador de matriz do descritor de campo |

- A função ISMARKEDO verifica este sinalizador (BEGIN TRANSACTION define-o como 1, END TRANSACTION e ROLLBACK redefine-o para 0).
- Se este sinalizador for definido como 1, a mensagem Banco de dados criptografado será exibida.
- O número máximo de campos é 255.
- n significa o último byte na matriz do descritor de campo.

### Matriz do descritor de campo
Layout dos descritores de campo no dBASE:

| Byte | Conteúdo | Significado |
---|---|---|
| 0–10 | 11 bytes | Nome do campo em ASCII (preenchido com zero) |
| 11 | 1 byte | Tipo de campo. Valores permitidos: C, D, F, L, M ou N (consulte a próxima tabela para significados) |
| 12–15 | 4 bytes | Reservado |
| 16 | 1 byte | Comprimento do campo em binário (máximo 254 (0xFE)). |
| 17 | 1 byte | Contagem decimal de campo em binário |
| 18–19 | 2 bytes | ID da área de trabalho |
| 20 | 1 byte | Exemplo |
| 21–30 | 10 bytes | Reservado |
| 31 | 1 byte | Sinalizador de campo MDX de produção; 1 se o campo tiver uma marca de índice no arquivo MDX de produção, 0 se não |

### Registros do banco de dados
Cada registro começa com um sinalizador de exclusão (1 byte). Os campos são agrupados em registros sem separadores de campo. Todos os dados de campo são ASCII. Dependendo do tipo de campo, o aplicativo impõe outras restrições. Aqui estão os tipos de campo no dBase:

| Tipo de campo | Mnemônico | O que aceita |
-------|-----|----|
| C | Personagem | Qualquer texto ASCII (preenchido com espaços até o comprimento do campo) |
| D | Data | Números e um caractere para separar mês, dia e ano (armazenados internamente como 8 dígitos no formato AAAAMMDD) |
| F | Ponto flutuante | -, ., 0–9 (justificado à direita, preenchido com espaços em branco) |
| L | Lógico | Y, y, N, n, T, t, F, f, ou ? (quando não inicializado) |
| M | Memorando | Qualquer texto ASCII (armazenado internamente como 10 dígitos representando um número de bloco .dbt, justificado à direita, preenchido com espaços em branco) |
| N | Numérico | -, ., 0–9 (justificado à direita, preenchido com espaços em branco) |









## Referências ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

