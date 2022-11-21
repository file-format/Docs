{
  "date" : "2021-08-30",
  "keywords" :[ "arquivo ipa", "formato de arquivo ipa", "o que é um arquivo ipa", "arquivo", "exemplo ipa", "extensão de arquivo ipa", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo IPA e APIs que podem criar e abrir arquivos IPA.",
  "title" :"IPA - Arquivo de pacote de aplicativos iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## O que é um arquivo IPA?
Um arquivo com extensão .ipa pertence ao iOS e é conhecido como arquivo de pacote de aplicativos. Este é um arquivo compactado (compactado usando compressão [ZIP](/pt/compression/zip/)) que armazena um aplicativo iOS, mas esse aplicativo só pode ser instalado em dispositivos MacOS baseados em iOS ou ARM, como iPad, iPhone ou Toque do iPod. Principalmente, iTunes, Apple Configurator 2 ou qualquer software de terceiros podem ser usados para instalar arquivos IPA.

## Formato de arquivo IPA
Os desenvolvedores do IOS que estão desenvolvendo os aplicativos usando o Apple Xcode estão bem familiarizados com os arquivos IPA porque precisam empacotar seus aplicativos desenvolvidos como arquivos IPA para testar a implantação da loja de aplicativos. Embora os arquivos IPA sejam instalados como aplicativos iOS, no entanto, você também pode descompactá-los para visualizar os dados do aplicativo contidos. Como um arquivo IPA contém apenas um binário para a arquitetura ARM de telefones celulares e não contém um binário para a arquitetura x86, muitos arquivos .ipa não podem ser instalados no iPhone Simulator.
### Estrutura de um arquivo .ipa
O exemplo a seguir mostra a estrutura de uma IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
O acima é uma estrutura interna para reconhecimento do iTunes e da App Store. De acordo com esta estrutura:
- O diretório Payload contém todos os dados do aplicativo.
- O arquivo de arte do iTunes é uma imagem PNG de 512 × 512 pixels, contendo o ícone do aplicativo para exibição no iTunes e no aplicativo App Store no iPad.
- O iTunesMetadata.plist contém várias informações, desde o nome e ID do desenvolvedor, informações de direitos autorais, identificador do pacote, nome do aplicativo, gênero, data de lançamento, data de compra etc.
- A pasta META-INF contém apenas metadados sobre qual programa foi usado para criar o IPA.


## Referências

* [.ipa - por Wikipedia](https://en.wikipedia.org/wiki/.ipa)


