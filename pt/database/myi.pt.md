---
date: 2020-11-11
keywords: myi, .myi, formato de arquivo myi, como abrir arquivos myi, extensão .myi, extensão myi
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo MYI
linktitle: MYI
description: "Saiba mais sobre o formato de arquivo MYI e as APIs que podem criar e abrir arquivos MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## O que é um arquivo MYI? ##

MYI também é conhecido como o arquivo MySQL MyISAM Index. Ele é usado para armazenar índices para a tabela MyISAM pelo MySQL. O índice do banco de dados MySQL define a estrutura da tabela e contém o mecanismo de controle para verificar a integridade das tabelas.

## Formato de arquivo MYI ##

O arquivo MYI tem duas partes, o cabeçalho e os valores-chave.

### Cabeçalho MYI ###

O cabeçalho contém informações sobre opções, tamanhos de arquivo e chaves. As chaves no MySQL são criadas com um comando como

```sql
CREATE [UNIQUE] INDEX.
```

Os arquivos que lêem e gravam arquivos MYI estão no diretório ./myisam. Possui os seguintes arquivos:

- mi_open.c: Este arquivo contém as rotinas que escrevem cada seção do cabeçalho.
- mi_create.c: Este arquivo contém as rotinas que chamam as rotinas mi_open.c.
- myisamdef.h: Este arquivo contém as definições da estrutura.

O cabeçalho tem as seguintes seções:

- estado: O estado é escrito por mi_open.c, mi_state_info_write(). Essa estrutura ocorre uma vez no arquivo.
- base: A base é escrita por mi_open.c, mi_base_info_write(). O MI_BASE_INFO é a estrutura correspondente para a base em myisamdef.h. Essa estrutura ocorre uma vez no arquivo.
- keydef: O keydef é escrito por mi_open.c, mi_keydef_write(). O MI_KEYDEF é a estrutura correspondente para o keydef em myisamdef.h. É uma estrutura de múltiplas ocorrências que aparece para cada índice.
- recinfo: O recinfo é escrito por mi_open.c, mi_recinfo_write(). O MI_COLUMNDEF é a estrutura correspondente para o recinfo em myisamdef.h. É uma estrutura de ocorrência múltipla que aparece uma vez de cada campo que aparece em uma chave.

### Valores-chave ###

As páginas no MySQL são chamadas de blocos. Os valores-chave estão em blocos. Um bloco contém informações de apenas um índice. Cada chave contém todo o conteúdo de todas as colunas. O comprimento normal do bloco é 0x0400 (1024) bytes. O ponteiro tem um número de tamanho fixo (4 bytes) para tabelas de linha fixa que contém um número de linha ordinal. Se a chave for nula, o byte será 0x00. Um bloco normal está pelo menos 65% cheio e normalmente 80% cheio.

O arquivo myisamdef.h contém as seguintes informações expressas em constantes. O número máximo de chaves é 32 (MI_MAX_KEY) e o número máximo de segmentos em uma chave é 16 (MI_MAX_KEY_SEG). O comprimento máximo da chave é 500 (MI_MAX_KEY_LENGTH). O comprimento máximo do bloco é 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referências ##

- [O arquivo .MYI](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

