{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Formato de Troca de Material",
  "keywords" :[ "MXF", "matroska video", "formato mkv", "como reproduzir arquivos MXF", "SMPTE", "multimídia", "vídeo" ],
  "description":"Saiba mais sobre o formato de arquivo MXF e APIs que podem criar e abrir arquivos MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## O que é um arquivo MXF?

Um arquivo com extensão .mxf é um formato de contêiner multimídia que contém vídeo digital e mídia de áudio junto com informações de metadados sobre o arquivo. Ele segue o padrão SMPTE (Society of Motion Picture and Television Engineers) que é uma associação global de profissionais de engenharia, tecnologia e executivos que trabalham na indústria de mídia e entretenimento. Os arquivos MXF podem ser convertidos em outros formatos de arquivo, como [AVI](/pt/video/avi/) ou [MOV](/pt/video/mov/).

## Formato de arquivo MXF

Os arquivos MXF são, na verdade, arquivos binários que consistem em uma sequência de bytes em um formato definido. Os aplicativos de decodificação devem estar em conformidade com esse formato para entendê-lo e extrair informações dele. O formato permite adicionar novos itens sem quebrar a compatibilidade com versões anteriores usando a codificação KLV descrita abaixo.

* Chave – o identificador do elemento, um SMPTE Universal Label (UL)
* Comprimento – o comprimento dos dados que é a codificação de comprimento variável usada para reduzir a quantidade de espaço necessária para este item
* Valor – o valor real do elemento.

### Especificações do formato SMPTE

O formato de arquivo MXF foi definido pelas seguintes especificações SMPTE.

* SMPTE ST 377-1:2011. Televisão — Formato de Troca de Material (MXF) — Especificação de Formato de Arquivo
* SMPTE ST 377-2 (trabalho em andamento em janeiro de 2012). Sintaxe de extensão codificada KLV para MXF.
* SMPTE ST 378:2004 (arquivado em 2010). Televisão — Formato de Troca de Material (MXF) — Padrão Operacional 1a (Item Único, Pacote Único)
* SMPTE ST 379-1:2009. Formato de Troca de Material (MXF) — Contêiner Genérico MXF
* SMPTE ST 379-2:2010. Formato de troca de material (MXF) -- Contêiner genérico restrito a MXF
* SMPTE ST 380:2004. Televisão — Formato de Troca de Material (MXF) — Esquema de Metadados Descritivos-1 (Padrão, Dinâmico)
* SMPTE ST 381-1:2005. Televisão — Formato de troca de material (MXF) — Mapeamento de fluxos MPEG no contêiner genérico MXF (dinâmico)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — Mapeamento de fluxos MPEG no contêiner genérico restrito MXF
* SMPTE ST 382:2007. Formato de troca de material (MXF) — Mapeamento de fluxos AES3 e áudio de onda de transmissão para o contêiner genérico MXF
* SMPTE ST 383:2008. Televisão — Formato de troca de material (MXF) — Mapeamento de dados DV-DIF para o contêiner genérico MXF
* SMPTE ST 384:2005. Televisão — Formato de troca de material (MXF) — Mapeamento de imagens não compactadas no contêiner genérico MXF
* SMPTE ST 385:2004. Televisão — Formato de troca de material (MXF) — Mapeamento de essência e metadados SDTI-CP no contêiner genérico MXF
* SMPTE ST 386:2004 (arquivado em 2010). Televisão — Formato de Troca de Material (MXF) — Mapeamento de Dados de Essência Tipo D-10 para o Contêiner Genérico MXF
* SMPTE ST 387:2004 (arquivado em 2010). Televisão — Formato de Troca de Material (MXF) — Mapeamento de Dados de Essência Tipo D-11 para o Contêiner Genérico MXF
* SMPTE ST 388:2004 (arquivado em 2010). Televisão — Formato de troca de material (MXF) — Mapeamento de áudio codificado de lei A no contêiner genérico MXF
* SMPTE ST 389:2005. Televisão — Formato de troca de material (MXF) — Elemento de sistema de reprodução reversa de contêiner genérico MXF
* SMPTE ST 390:2011. Televisão — Formato de Troca de Material (MXF) — Padrão Operacional Especializado "Atom" (Representação Simplificada de um Único Item)
* SMPTE ST 391:2004 (arquivado em 2010). Televisão — Formato de Troca de Material (MXF) — Padrão Operacional 1b (Item Único, Pacotes Agrupados)
* SMPTE ST 392:2004. Televisão — Formato de Troca de Material (MXF) — Padrão Operacional 2a (Itens da Play-List, Pacote Único)
* SMPTE ST 393:2004. Televisão — Formato de Troca de Material (MXF) — Padrão Operacional 2b (Itens da Play-List, Pacotes Agrupados)
* SMPTE ST 394:2006. Televisão — Formato de Troca de Material (MXF) — Esquema de Sistema 1 para o Contêiner Genérico MXF
* SMPTE ST 405:2006. Televisão — Formato de Troca de Material (MXF) — Elementos e Itens de Dados Individuais para o Esquema 1 do Sistema de Contêiner Genérico MXF
* SMPTE ST 407:2006. Televisão — MXF — Padrões Operacionais 3a e 3b
* SMPTE ST 408:2006. Televisão — MXF — Padrões Operacionais 1c, 2c e 3c
* SMPTE ST 410: 2008. Formato de Troca de Material - Partição de Fluxo Genérico.
* SMPTE ST 422:2006. Formato de troca de material — Mapeando fluxos de código JPEG2000 no contêiner genérico MXF
* SMPTE ST 429.4:2006. Embalagem D-Cinema — Aplicação MXF JPEG 2000
* SMPTE ST 429.5:2006. Embalagem D-Cinema — Arquivo de trilha de texto cronometrado
* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption
* SMPTE ST 434:2006. Formato de Troca de Material — Codificação XML para Metadados e Informações de Estrutura de Arquivos
* SMPTE ST 436:2006. Televisão — Mapeamentos MXF para Linhas VBI e Pacotes de Dados Auxiliares
* SMPTE ST 2019-4:2009. Mapeando Unidades de Codificação VC-3 no Contêiner Genérico MXF
* SMPTE ST 2037:2009. Mapeando VC-1 no contêiner genérico MXF
* SMPTE RP 2008:2008. Formato de troca de material — Mapeando fluxos AVC no contêiner genérico MXF
* SMPTE RP 2057:2011. Transporte de metadados baseado em texto em MXF
* SMPTE EG 41:2004. Formato de Troca de Material (MXF) — Diretriz de Engenharia. Nota: Este documento não estava mais listado no site do SMPTE quando consultado em janeiro de 2012.
* SMPTE EG 42:2004. Formato de Troca de Material (MXF) — Metadados Descritivos MXF
* SMPTE RDD 3:2008. Especificação de interoperabilidade e-VTR MXF
* SMPTE RDD 9-2009. Especificação de interoperabilidade MXF dos produtos Sony MPEG Long GOP
* Menu de planilha de registro de metadados SMPTE.

### Metadados Estruturais MXF

Os metadados estruturais são fundamentais em um arquivo MXF, pois contêm informações úteis sobre o conteúdo do arquivo. Os metadados MXF contêm informações como taxa de quadros, tamanho do quadro, data de criação do arquivo e data de modificação personalizada. Os metadados estruturais descrevem a estrutura e os recursos de um arquivo MXF que inclui descrever tecnicamente os vários componentes essenciais e transmitir como a linha do tempo de saída é composta.

## Referências

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Relatório de progresso](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Biblioteca OpenSource C++ para MXF](http://www.freemxf.org/)

