{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo VHDX e APIs que podem criar e abrir arquivos VHDX.",
  "title" :"Formato de arquivo VHDX - O que é um arquivo VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## O que é um arquivo VHDX?

Um arquivo VHDX é um arquivo de imagem de disco no formato de arquivo Virtual Hard Disk v2. Ele contém um sistema operacional inteiro que pode ser carregado e usado como qualquer máquina normal para teste de software ou software em execução que requer um sistema operacional específico. Um VHDX, apesar de ser uma imagem de disco completa, é armazenado em um único arquivo. O software de máquina virtual, como Parallels Desktop, Windows Virtual Machine e Virtual Box, pode carregar e abrir a imagem do disco.

O arquivo VHDX pode ser convertido em [VHD](/pt/disc-and-media/vhd/) com Hyper-V Manager, ou em [VDI](/pt/disc-and-media/vdi/) com VirtualBox.

## Formato de arquivo VHDX - Mais informações

Os detalhes do formato de arquivo VHDX estão completamente documentados e disponíveis online como [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) na Documentação da Microsoft. É uma extensão do formato VHD e inclui recursos aprimorados. O formato de arquivo VHDX fornece recursos adicionais que estão disponíveis no disco rígido virtual e nas camadas de arquivo do disco rígido virtual. É mais otimizado e oferece melhores resultados para configuração e recursos de hardware de armazenamento. Arquivos VHDX podem ser abertos

### Suporte para discos rígidos virtuais em VHDX

Ele suporta três tipos de discos rígidos virtuais.

1. **Disco Rígido Virtual Fixo** - Disco rígido virtual com tamanho de dados fixo alocado. O tamanho do disco rígido virtual não muda com a adição ou remoção de dados.

1. **Disco Rígido Virtual Dinâmico** - Disco rígido virtual com tamanho de disco dinâmico. Seu tamanho a qualquer momento é tão grande quanto os dados reais gravados nele e os metadados. O tamanho do arquivo aumenta dinamicamente à medida que os dados são adicionados ou removidos dele.

1. **Disco rígido virtual diferenciado** - Representa a corrente do disco rígido virtual como um conjunto de blocos modificados em comparação com um arquivo de disco rígido virtual pai.

## Referências

* [Especificações de formato de arquivo VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - por Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

