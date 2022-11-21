---
date: 2019-10-11
keywords: step, .step, formato de arquivo de step, como abrir arquivos de step, extensão .step, extensão de step
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo STEP
linktitle: STEP
description: "Saiba mais sobre o formato de arquivo STEP e APIs que podem criar e abrir arquivos STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## O que é um arquivo STEP?

O arquivo STEP é um formato de troca de dados amplamente utilizado para design assistido por computador (CAD). Foi padronizado em 1994 pelo comitê ISO sob o nome de "ISO 10303-21". A ISO 10303-21 define o mecanismo de codificação para representar dados na linguagem de modelagem de dados EXPRESS. Um arquivo STEP também é conhecido como arquivo p21 e arquivo físico STEP. As extensões de arquivo usadas para o arquivo STEP são .stp e .step.

## Histórico básico

Em 1994, a especificação original da Parte 21 foi emitida. Tem alguns bugs que foram corrigidos pela rectificação técnica emitida em 1996. A segunda edição foi publicada em 2002 que incluía a rectificação e extensões para várias secções de dados. A terceira edição foi publicada em 2016 que adicionou seções de âncora e referência que permitiam que entidades e valores fossem armazenados em arquivos externos. Suporte UTF-8 foi adicionado de strings. Assinaturas digitais foram adicionadas para verificar o conteúdo do arquivo e validar as credenciais. O suporte para compactar e armazenar a estrutura de câmbio usando ZIP também foi adicionado.

## Formato de arquivo STEP

O formato de texto simples para um arquivo STEP consiste em uma sequência de registros. O conjunto de caracteres é definido como pontos de código da ISO 10646. "ISO-10303-21;" são os primeiros caracteres no primeiro registro. Os comentários são cercados pelos caracteres "/*" e "*/". O último registro contém "END-ISO-10303-21;" se o arquivo STEP estiver em conformidade com a versão 2002. Caso esteja em conformidade com a versão 2016, poderá haver uma ou mais assinaturas digitais após o "END-ISO-10303-21;" o Exterminador do Futuro. As quebras de linha são indicadas por "\N\" e as quebras de página são indicadas por "\F\".

O arquivo STEP é dividido em seções e seus nomes são termos reservados. Todas as seções terminam com o registro "ENDSEC" e devem estar na ordem mostrada abaixo.

- **CABEÇALHO**: Esta é uma seção obrigatória e não repetível. É composto pelas seguintes entidades:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ÂNCORA**: É uma seção opcional não repetitiva que foi introduzida na versão 2016. Ele define os nomes externos das instâncias para que possam ser referenciados.
- **REFERÊNCIA**: É uma seção opcional não repetitiva que também foi introduzida na versão 2016. Cada entrada nesta seção associa um nome de instância de entrada/valor a uma instância/valor em um arquivo externo.
- **DATA**: É uma seção repetível opcional que contém o conteúdo central da instância do modelo.
- **SIGNATURE**: É uma seção repetível opcional que foi introduzida na versão 2016. Ele contém a assinatura digital para verificar o conteúdo do arquivo ou validar credenciais.

## Referências

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

