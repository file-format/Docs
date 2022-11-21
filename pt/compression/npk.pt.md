{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo NPK",
  "description":"Saiba mais sobre o formato de arquivo NPK e APIs que podem criar e abrir arquivos NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## O que é um arquivo NPK?

Um arquivo NPK é um arquivo de pacote de atualização de software usado por roteadores **MikroTik** para atualização do sistema operacional do roteador. Ele vem como um arquivo binário compactado que é carregado no roteador para instalar atualizações de software. As informações contidas em um arquivo NPK incluem informações de rede, como endereço IP e serviço IP, informações de conectores (interfaces ethernet e porta serial), configuração de e-mail, configuração de ponte e gerenciamento de usuário local.

## Formato de arquivo NPK

Os arquivos NPK são armazenados como arquivo binário compactado. É um formato de arquivo fechado que é usado apenas pelo próprio MikroTik. Não se destina a criar complementos do RouterOS por meio de terceiros. Os arquivos NPK são mantidos pelo próprio MikroTik e versões atualizadas do mesmo podem ser baixadas nas seções de download do site [MikroTik](https://mikrotik.com/download).

Quando um arquivo NPK é carregado para um roteador, o sistema operacional do roteador não entra em vigor a menos que seja reinicializado. Portanto, uma reinicialização é necessária para que o SO do roteador seja atualizado.

## Referências

* [MikroTik - Atualizando o sistema operacional do roteador](https://mikrotik.com/download)
* [Como criar arquivos NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

