---
date: 2019-10-11
keywords: toml, .toml, formato de arquivo toml, como abrir arquivos toml, extensão .toml, extensão toml
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo TOML
linktitle: TOML
description: "Saiba mais sobre o formato de arquivo TOML e as APIs que podem criar e abrir arquivos TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## O que é um arquivo TOML? ##

TOML (Tom's Obvious Minimal Language) é um formato de arquivo de configuração mínima que usa a extensão .toml. O TOML visa ser fácil de ler, mapear sem ambiguidade para dicionários e ser fácil de analisar diferentes estruturas de dados. TOML tem uma especificação de código aberto que recebeu contribuições da comunidade. TOML é suportado por muitas linguagens de programação como C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. O tipo MIME para arquivos TOML é *application/toml*.


## Formato de arquivo TOML ##

Os arquivos TOML consistem principalmente em pares de chave/valor, seções/tabelas, comentários e devem ser um documento Unicode codificado em UTF-8 válido. O TOML suporta os tipos de dados String, Integer, Float, Boolean, Datetime, Array e Table (tabela de hash/dicionário). TOML é uma linguagem que diferencia maiúsculas de minúsculas.

### Sintaxe ###

- **Pares de valores-chave**: os pares de valores-chave são separados por um sinal de igual (=). Cada par deve estar em uma nova linha.

```tom
primeiro = "Tom"
last = "Preston-Werner"
```

- **Comentários**: Os comentários começam com o símbolo de hash (#).

```tom
# Este é um documento TOML.
```

- **Strings**: as strings estão entre aspas ("").

```tom
string = "String de exemplo"
```

- **Strings de várias linhas**: Strings de várias linhas são cercadas por três aspas (""").

```tom
[endereço residencial]
rua = """123 Tornado Alley
Suíte 16"""
cidade = "East Centerville"
estado = "KS"
```

- **Inteiros/Floats**

```tom
inteiro = 20
flutuar = 20,5
```

- **Booleanos**: Booleanos são sempre minúsculos.

```tom
bool1 = verdadeiro
bool2 = falso
```

- **Date-Time**: Para DateTime, você pode usar uma data e hora formatada em RFC 3339, conforme mostrado no exemplo abaixo.

```tom
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
data_local = 27-05-1979
local_time = 07:32:00
```

- **Matrizes**: As matrizes são cercadas por colchetes com elementos separados por vírgulas (,).

```tom
cores = [ "vermelho", "amarelo", "verde" ]
```

- **Tabelas**: as tabelas são coleções de pares de chave/valor que são definidos por cabeçalhos em uma nova linha entre colchetes ([]). A tabela termina quando um novo cabeçalho é fornecido ou quando o arquivo termina.

```tom
[endereço residencial]
rua = """123 Tornado Alley
Suíte 16"""
cidade = "East Centerville"
estado = "KS"

[Endereço do escritório]
rua = """123 Tornado Alley
Suíte 16"""
cidade = "East Centerville"
estado = "KS"
```

As tabelas inline são cercadas por chaves ({}) com cada par de chave/valor separado por vírgula (,).

```tom
nome = { primeiro = "Tom", último = "Pitt" }
```

## Referências ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

