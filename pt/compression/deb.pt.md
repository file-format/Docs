{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo deb", "formato de arquivo deb", "o que é um arquivo deb", "arquivo", "exemplo deb", "extensão de arquivo deb","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"Saiba mais sobre o formato de arquivo DEB e APIs que podem criar e abrir arquivos DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## O que é um arquivo DEB?

Um arquivo com extensão .deb é um formato de arquivo de pacote binário Debian disponível para distribuição de pacotes de software no sistema operacional Linux. Ele consiste em dois arquivos de arquivo [TAR](/pt/compression/tar/). O DPKG fornece o mecanismo para ler e instalar os pacotes DEB. Os pacotes DEB podem ser instalados usando a interface de gerenciamento de software do pacote APT. Arquivos DEB têm Internet Media Type como `application/vnd.debian.binary-package`.

## Formato de arquivo DEB

Um arquivo DEB consiste em dois arquivos de arquivo [TAR](/pt/compression/tar/). Um arquivo contém as informações de controle e outro contém os dados instaláveis.

### Organização do pacote

O arquivo DEB é um arquivo **ar** que tem um valor mágico de `!<arch> `. Desde o Debian 0.93, o mecanismo de arquivamento de arquivos DEB contém três arquivos em uma ordem específica.

1. `Debian Binary` - Destina-se a ter uma série de linhas, separadas por novas linhas. Atualmente, apenas uma única linha está presente que descreve o número da versão. O número da versão atual é 2.0.
1. `Control Archive` - Contém um arquivo control.tar que possui scripts de mantenedor e meta-informações sobre o pacote, como nome do pacote, versão, dependências e mantenedor.
1. `Arquivo de Dados` - É um arquivo tar chamado data.tar e contém os arquivos de mídia instaláveis reais. O arquivo pode ser compactado com gz, bz2, lzma ou xz, e a extensão do arquivo de dados muda de acordo.

### Arquivo de controle

O arquivo de controle pode incluir conteúdos como segue.

* `control` - Contém uma breve descrição do pacote bem como outras informações como suas dependências.
* `md5sums` - Contém checksums MD5 de todos os arquivos do pacote para detectar arquivos corrompidos ou incompletos.
* `conffiles` - Lista os arquivos do pacote que devem ser tratados como arquivos de configuração. Os arquivos de configuração não são substituídos durante uma atualização, a menos que especificado.
* `preinst`, postinst, prerm e postrm - Scripts opcionais que são executados antes ou depois de instalar ou remover o pacote
* `config` é um script opcional que suporta o mecanismo de configuração do debconf.
* `shlibs` - É uma lista de dependências de bibliotecas compartilhadas.

## Referências

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Formato do pacote binário Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

