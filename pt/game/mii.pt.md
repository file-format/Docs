{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo MGX do Age of Empires 2 Expansion Replay e as APIs que podem criar e abrir arquivos MGX.",
  "title" : "Arquivo MII - formato de arquivo de avatar virtual do Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-pt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## O que é um arquivo .MII?

Um arquivo MII é um formato de arquivo de avatar virtual usado para armazenar avatares virtuais no console de jogos Nintendo Wii. Esses arquivos contêm informações como aparência, movimentos e animações do avatar. Eles podem ser usados em jogos, aplicativos de redes sociais e outros softwares no Wii. Um arquivo MII também contém outros recursos sobre o avatar, como sexo, cor do cabelo, cor da pele, características faciais e tipo de olho.

Você pode abrir um arquivo MII usando o [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Formato de arquivo MII

O formato do arquivo MII é definido detalhadamente em [Wii Brew](https://wiibrew.org/wiki/Mii_data). As strings em um arquivo MII são armazenadas no formato Unicode (UTF-16), big-endian.

### Bloco MI

Os dados do arquivo MII são armazenados no Wiimote em dois blocos. Cada bloco tem 750 bytes de comprimento, com CRC de 2 bytes, perfazendo um total de 752 bytes. Cada bloco começa com um valor de 4 bytes ('RNCD') que parece ser o número mágico para o formato de arquivo MII.

## Como criar arquivos MII?

Existem algumas maneiras diferentes de criar avatares para o Nintendo Wii:

1. `Usando o canal Mii integrado no Wii:` Este canal permite que você crie avatares personalizados usando uma variedade de ferramentas, incluindo características faciais, formato do corpo e roupas. Depois de criar seu avatar, você pode salvá-lo como um arquivo Mii e usá-lo em jogos e outros softwares no Wii.

1. `Usando o aplicativo Mii Maker no Nintendo 3DS:` O aplicativo Mii Maker permite que você crie avatares personalizados usando a tela sensível ao toque e a câmera do seu Nintendo 3DS. Depois de criar seu avatar, você pode salvá-lo como um arquivo Mii e transferi-lo para o Wii através de uma conexão sem fio.

1. `Usando software de terceiros:` Alguns desenvolvedores criaram software que permite criar avatares personalizados para o Wii. Este software normalmente é projetado para uso em um computador e pode exigir etapas adicionais para transferir o avatar para o seu Wii.

1. `Usando avatares pré-fabricados:` Alguns jogos e outros softwares no Wii podem vir com avatares pré-fabricados que você pode usar.

Em todos os casos, você precisa ter uma conta Nintendo para criar e salvar seu avatar no Wii.

## Referências

* [Meu Editor de Avatar](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


