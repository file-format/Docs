{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo rar", "formato de arquivo rar", "o que é um arquivo rar", "arquivo", "exemplo rar", "extensão de arquivo rar", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RARO",
  "description":"O que é uma extensão de arquivo RAR e APIs que podem criar e abrir arquivos RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo RAR?

Arquivos com extensão .rar são arquivos compactados criados para armazenar informações em formato compactado ou normal. RAR, que significa Roshal ARchive file format, é um formato de arquivo proprietário criado por Eugene Roshal em 1995, que era um engenheiro de software russo. O formato é usado para arquivar arquivos com diferentes métodos, incluindo várias técnicas de compactação. Existem vários softwares aplicativos disponíveis para Windows, Linux e MacOS para extração de arquivos RAR. O software WinRAR, da RARLab, é o utilitário de arquivamento de arquivos shareware (gratuito por 40 dias) para plataforma Microsoft Windows; o software foi portado para Linux (apenas como extrator) pelo mesmo autor, Eugene Roshal.

## Histórico de versões do formato de arquivo RAR

* v1.3 (original, não tem assinatura "Rar!")
* v1.5
* v2.0 - lançado com WinRAR 2.0 e Rar para MS-DOS 2.0
* v2.9 - lançado no WinRAR versão 3.00
* v5.0 - suportado pelo WinRAR 5.0 e posterior

## Principais recursos do formato RAR

O RAR está em campo há muito tempo e tem sido um dos formatos de arquivo de arquivamento favoritos. As principais características do formato RAR são:

**`Alta taxa de compressão:`** Superior em comparação com [ZIP](/pt/compression/zip/), comparável com o formato 7z e zipx.

**`Criptografia de arquivo forte por design:`** Arquivos RAR4 criptografados contam com criptografia baseada em AES-128, enquanto arquivos RAR5 criptografados contam com criptografia AES-256 com agendamento de chave aprimorado

**`Recursos avançados de correção de erros e recuperação de dados:`** registros de recuperação opcionais durante a criação do arquivo

**`Tamanho do arquivo:`** Mínimo de 20 bytes e máximo de 2^63 bytes de tamanho (8 exabytes do tamanho total do arquivo)

**`Arquivos RAR de vários volumes:`** Possibilidade de dividir arquivos grandes em vários arquivos menores para facilitar a transferência pela rede. Nesse caso, as extensões de arquivo são incrementadas em 1 para representar volumes divididos

## Formato de arquivo RAR

As especificações completas do formato RAR não estão disponíveis publicamente e é por isso que os detalhes sobre o formato não podem ser formulados de maneira concisa.

### Layout geral do arquivo

O layout geral de um formato de arquivo RAR introduzido na versão 5.0 é o seguinte:

|Formato de arquivo
---|
|Módulo de extração automática (opcional)
|Assinatura RAR 5.0
|Cabeçalho de criptografia de arquivo (opcional)
|Cabeçalho do Arquivo Principal
|Cabeçalho do serviço de comentários do arquivo (opcional)
Cabeçalho do arquivo 1
|Cabeçalhos de serviço (NTFS ACL, fluxos, etc.) para o arquivo anterior (opcional)
|...
| Cabeçalho do arquivo N
|Cabeçalhos de serviço (NTFS ACL, fluxos, etc.) para o arquivo anterior (opcional)
|Registro de recuperação (opcional)
|Fim do cabeçalho do arquivo

Informações sobre cada seção do arquivo RAR mencionada acima podem ser encontradas no documento [RAR 5.0 File Format Specifications](https://www.rarlab.com/technote.htm#arcstruct).

#### Arquivos RAR de extração automática

Se o próprio arquivo RAR for auto-extraível, as informações de auto-extração estarão contidas no início do arquivo que precede a assinatura do arquivo. Seu tamanho e conteúdo não estão definidos.

#### Assinatura RAR 5.0

A assinatura RAR é um cabeçalho de 8 bytes que consiste no seguinte número mágico:

0x 52 61 72 21 1A 07 00

Onde

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referências

* [Formato de arquivo RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - Por Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

