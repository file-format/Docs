{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aprenda sobre o formato de arquivo AC e APIs que podem criar e abrir arquivos ACCDB.",
  "title" : "Formato de arquivo AC - arquivo de script Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-pt",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## O que é um arquivo .AC?

O arquivo AC é o arquivo de script do Autoconf. **Autoconf** é um pacote extensível de macros M4 que produz scripts de shell para configurar automaticamente pacotes de código-fonte de software. Esses scripts podem adaptar os pacotes a muitos tipos de sistemas do tipo UNIX sem intervenção manual do usuário. O Autoconf cria um script de configuração para um pacote a partir de um arquivo de modelo que lista os recursos do sistema operacional que o pacote pode usar, na forma de chamadas de macro M4.

Producing configuration scripts using Autoconf requires GNU M4. Você deve instalar o GNU M4 (pelo menos a versão 1.4.6, embora 1.4.13 ou posterior seja recomendado) antes de configurar o Autoconf, para que o script de configuração do Autoconf possa encontrá-lo. Os scripts de configuração produzidos pelo Autoconf são independentes, portanto seus usuários não precisam ter o Autoconf (ou GNU M4).

## Como abrir o arquivo AC?

AC significa Configuração Automática. É um script gerado pelo GNU Autoconf que permite que o código-fonte do software seja adaptado a vários sistemas do tipo Posix, testando os recursos necessários no pacote. O script é chamado de arquivo AC.

## Principais componentes do Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools é uma coleção de pacotes relacionados que, quando usados em conjunto, eliminam grande parte da dificuldade envolvida na criação de software portátil. Essas ferramentas, juntamente com alguns arquivos de entrada relativamente simples fornecidos pelo upstream, são usadas para criar o sistema de compilação de um pacote.

**Uma visão geral básica de como os principais componentes do AutoTools se encaixam.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Em uma configuração simples:

- O programa `autoconf` produz um script de configuração de `configure.in` ou `configure.ac`.
- O programa `automake` produz um Makefile.in a partir de um Makefile.am.
- O script `configure` é executado para produzir um ou mais arquivos Makefile a partir de arquivos Makefile.in.
- O programa `make` usa o Makefile para compilar o programa.

## Referências
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Noções básicas de Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



