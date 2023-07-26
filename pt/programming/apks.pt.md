
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo APKS - Arquivo de conjunto de APKs",
  "description":"Saiba mais sobre o que é um arquivo APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## O que é um arquivo APKS?

Um arquivo com extensão .apks é um arquivo compactado que é uma coleção de arquivos **APK** do pacote Android. Cada arquivo APK individual no arquivo APKS é gerado tendo em vista vários aspectos dos dispositivos. Isso inclui arquitetura, idioma, densidade da tela e outros recursos do dispositivo. Os arquivos APKS são gerados por **bundletool**. Ele é usado para criar o Android App Bundle e converter o pacote de aplicativos em diferentes APKs para implantação em dispositivos.

## Formato de arquivo APKS - Mais informações

Os arquivos APKS são salvos como arquivos compactados usando o formato de arquivo [ZIP](/pt/compression/zip/).

## Como gerar um arquivo APKS?

Quando o Android App Bundle (AAB) estiver pronto, seu comportamento na Google Play Store poderá ser testado para implantação em um dispositivo. Arquivos APKS podem ser gerados, para isso, a partir de arquivos AAB e instalados em dispositivos de teste usando o Android [bundletool](https://developer.android.com/tools/bundletool) do Google. Ele fornece ferramentas de linha de comando para criar o arquivo APKS de APKs usando o comando a seguir.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Para implantar os APKs em um dispositivo, o arquivo APKS pode ser assinado com as informações de assinatura do dispositivo conforme a seguir.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referências

* [bundletool - linha de comando](https://developer.android.com/tools/bundletool)

