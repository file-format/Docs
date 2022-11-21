{
  "date" : "2021-08-10",
  "keywords" :[ "arquivo .ovf", "formato de arquivo", "o que é um arquivo .ovf", "arquivo", "extensão de arquivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o que é um formato de arquivo .ovf e APIs que podem criar e abrir arquivos OVF.",
  "title" :"Formato de arquivo OVF - Abrir arquivo de virtualização",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## O que é um arquivo OVF?

Um arquivo OVF é um arquivo de texto que contém informações sobre o empacotamento e distribuição de um software executado em uma máquina virtual. Ele é formatado de acordo com as [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) que descreve todos os requisitos (como segurança, portabilidade, eficiência e extensibilidade) para executar aplicativos em máquinas virtuais. A Organização Internacional para Padronização (ISO) adotou o OVF como padrão ISO 17203.

## Breve História do Formato de Arquivo OVF

O formato de arquivo OVF foi introduzido pelo DMTF (Distributed Management Task Force) que cria padrões abertos de gerenciamento. É independente de qualquer hypervisor ou arquitetura de conjunto de instruções em particular. O pacote OVF contém um ou mais sistemas virtuais, cada um dos quais pode ser implantado em uma máquina virtual.

## Formato de arquivo OVF - Mais informações

Um pacote OVF consiste em vários arquivos colocados em um único diretório. Entre estes, contém exatamente um arquivo descritor OVF (com extensão .ovf) que é armazenado no formato de arquivo [XML](/pt/web/xml/). Ele descreve as informações da máquina virtual empacotada e informações de metadados sobre o pacote OVF, como:

* nome
* requisitos de hardware
* referências a outros arquivos no pacote OVF, e
* descrições legíveis por humanos

Outros arquivos que podem ser encontrados em um pacote OVF incluem uma ou mais imagens de disco e, opcionalmente, arquivos de certificado e outros arquivos auxiliares.

## Referências

* [Formato de virtualização aberta - DMTF](https://www.dmtf.org/standards/ovf)
* [Especificações de formato de arquivo OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

