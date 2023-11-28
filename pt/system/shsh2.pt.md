{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo SHSH2 - formato de arquivo iOS SHSH Blob",
  "description":"Aprenda sobre o que é um arquivo SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## O que é um arquivo .SHSH2?

Um arquivo SHSH2, também conhecido como blob SHSH ou ECID SHSH, é uma assinatura digital usada pela Apple para autenticar e verificar atualizações de firmware para dispositivos iOS, como iPhones, iPads e iPods. Ele contém um identificador exclusivo para o dispositivo conhecido como ECID (Exclusive Chip ID). Também contém informações sobre a versão do firmware instalada no dispositivo.

## Formato de arquivo SHSH2 – Mais informações

Os arquivos SHSH2 são salvos em disco em formato de arquivo binário e os detalhes da estrutura interna desse formato de arquivo não estão disponíveis publicamente.

Quando uma nova versão do iOS é instalada em um dispositivo Apple como iPhone, iPad ou Mac, um arquivo SHSH2 é gerado. Este arquivo SHSH2 é enviado aos servidores Apple que lêem e verificam este arquivo de assinatura digital. Com base nessas informações, o servidor permite ou impede a instalação.

O mesmo acontece quando uma atualização é solicitada. Quando um usuário solicita uma atualização ou restauração de seu dispositivo por meio do iTunes ou outro software, os servidores da Apple verificarão se o arquivo SHSH2 corresponde ao ECID e à versão do firmware do dispositivo antes de permitir que a atualização prossiga.

## Referências

* [SHSH Blob - Por Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Economia de TSS](https://tsssaver.1conan.com/v2/)

