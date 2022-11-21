{
  "date" : "2021-08-13",
  "keywords" :[ "arquivo sdi", "formato de arquivo sdi", "o que é um arquivo sdi", "arquivo", "exemplo sdi", "extensão de arquivo sdi", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo SDI e APIs que podem criar e abrir arquivos SDI.",
  "title" :"SDI - Arquivo de imagem de implantação do sistema Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## O que é um arquivo SDI?
O arquivo com extensão .sdi contém um blob de carregamento, um blob de inicialização e um blob parcial; comumente usado pelo Windows Embedded Studio para criar discos de RAM ou discos de inicialização para carregar e instalar o Windows. O SDI é abreviado para System Deployment Image. O Windows Embedded Studio é um programa usado para criar imagens de disco para Windows. Na verdade, este programa contém o programa SDI File Manager e uma ferramenta de linha de comando chamada **sdimgr.exe**, ambos podem ser usados para implantar, criar e editar imagens SDI.

## Formato de arquivo SDI
O formato de arquivo SDI é amplamente utilizado para permitir o uso de um disco virtual para inicializar um sistema. Algumas versões do Microsoft Windows habilitam **inicialização de RAM**, o que é importante para carregar um arquivo SDI na memória e inicializar a partir dele. O formato de arquivo SDI também se habilita para inicialização de rede usando o PXE (Preboot Execution Environment). Ele também está sendo usado para imagens de disco rígido.
### Seções do arquivo SDI
O próprio arquivo SDI pode ser subdividido nas seguintes seções:
- **Boot BLOB**: Contém o programa de inicialização real, STARTROM.COM. Isso é análogo ao setor de inicialização de um disco rígido.
- **Carregar BLOB**: normalmente contém NTLDR e é iniciado pelo BLOB de inicialização.
- **Part BLOB**: Contém o tempo de execução de inicialização real; também inclui os arquivos boot.ini e ntdetect.com que devem estar localizados no diretório raiz do tempo de execução.
- **Disk BLOB**: Esta é uma imagem de HDD plana começando com um MBR. Ele é usado para imagens do disco rígido em vez de inicializar. Além disso, apenas BLOBs de disco podem ser montados com os utilitários da Microsoft.


## Referências

* [Imagem de implantação do sistema - pela Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


