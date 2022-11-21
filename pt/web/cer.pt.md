{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extensão", "arquivo", "formato", "web", "certificado", "idioma" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Formato de arquivo de certificado",
  "description":"Saiba mais sobre o formato de arquivo CER e APIs que podem criar e abrir arquivos CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## O que é um arquivo CER? ##

Um arquivo com extensão .cer é responsável por armazenar algumas informações sobre o certificado do proprietário e a chave pública específica. Este formato de arquivos não pode armazenar as chaves privadas e tem capacidade para armazenar apenas um certificado que é x509. As autoridades de certificação especificamente protegidas são aquelas que pertencem ao HTTPS, um protocolo confiável e seguro para navegação
O CER é um certificado do seu servidor. Geralmente é recebido pela autoridade de certificação do domínio. O CER é considerado o mesmo que [CRT](/pt/web/crt/), embora ambos tenham o mesmo formato de certificado SSL, mas sejam extensões de nome de arquivo diferentes.
Eles podem ser usados em sistemas operacionais simplesmente abrindo um navegador e verificando a segurança do navegador ou site que está sendo usado.

## Breve história ##

Em 1995, Thawte tornou-se a primeira autoridade de certificação para resolver a questão de certificados SSL públicos (secured socket link) fora dos EUA. Depois disso, há uma série de tais autoridades que foram fundadas de 1995 a 2020.

## Formato de arquivo CER ##

Esses arquivos podem ser simplesmente
* O PKC S#7 compreende a codificação Base64 ASCII
* Suas extensões de arquivo são p7b ou p7cZ
* Para conteúdo binário, o certificado seria DER ou pkcs12/pfx.
Existem muitos tipos de arquivos de certificado com algumas especificações exclusivas:
* .pem, quando uma organização usa Thawteificate encadeando este formato é bem conhecido para criar certificados
* .arm, quando o método de extração de uma certificação auxilia autoassinado, é necessário, o formato especificado para este fim é .arm. É representado na codificação ASCII de base 64.
* .der, Consiste em dados binários. Isso significa que ele pode ser usado apenas para um único certificado
* .pfx (PKC512), Consiste em uma chave privada correspondente a um certificado emitido pela CA ou a um certificado autoassinado. Este formato é bem conhecido pela conversão de uma implementação SSL para outra.


