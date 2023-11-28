{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo SHSH - formato de arquivo SHSH Blob do iPhone/iPod Touch",
  "description":"Aprenda sobre o que é um arquivo SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## O que é um arquivo .SHSH?

Um arquivo SHSH, também conhecido como Signature HaSH, é uma assinatura digital usada pela Apple para autenticar e verificar atualizações de firmware para dispositivos iOS, como iPhones, iPads e iPods.

## Diferença entre formatos de arquivo SHSH e SHSH2

Assim como um arquivo SHSH2, o arquivo SHSH contém um identificador exclusivo para o dispositivo chamado "ECID" (Exclusive Chip ID), bem como informações sobre a versão do firmware instalada no dispositivo. No entanto, os arquivos SHSH eram usados em versões mais antigas do iOS (anteriores ao iOS 10) e desde então foram substituídos por arquivos SHSH2.

## Formato de arquivo SHSH – Mais informações

Os arquivos SHSH são salvos em disco em formato de arquivo binário. Os detalhes da estrutura interna do arquivo deste formato de arquivo não estão disponíveis publicamente.

Os arquivos SHSH são importantes para usuários que desejam fazer o downgrade do firmware de seus dispositivos para uma versão anterior que não seja mais assinada pela Apple. Ao salvar os arquivos SHSH para uma versão de firmware específica quando ela ainda está assinada pela Apple, os usuários podem usá-los posteriormente para ignorar a verificação de assinatura da Apple e instalar essa versão de firmware em seus dispositivos. Este processo também é conhecido como `jailbreaking`.

## Referências

* [SHSH Blob - Por Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Economia de TSS](https://tsssaver.1conan.com/v2/)

