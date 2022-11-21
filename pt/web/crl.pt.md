{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo CRL - Lista de revogação de certificados",
  "description":"Saiba mais sobre o formato de arquivo CRL e APIs que podem criar e abrir arquivos CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## O que é um arquivo CRL?

Um arquivo CRL (Certificate Revocation List) é uma lista negra de certificados digitais X.509 que uma autoridade de certificação (CA) revoga antes da data de revogação atribuída. Ele contém informações sobre o problema e a data de revogação que permite que os administradores de segurança bloqueiem os certificados digitais afetados. A CRL não inclui certificados expirados, pois seu objetivo principal é notificar sobre os certificados não confiáveis e inválidos.

Os aplicativos que podem **abrir arquivos CRL** incluem OpenSSL, Microsoft IIS Server e Citrix NetScaler.

## Formato de arquivo CRL - Mais informações

Os arquivos CRL contêm informações no padrão X.509 que também define sua semântica para compartilhar informações de chave pública. Outras informações contidas em um arquivo CRL podem incluir o limite de tempo para o qual os certificados foram revogados, motivo da revogação, número de série do certificado revogado e carimbo de data/hora.


### Principais motivos para a adição de certificados à CRL

Pode haver vários motivos para que o certificado do seu site seja revogado e adicionado à CRL. Alguns deles poderiam ser;

1. A chave privada do seu certificado foi comprometida
1. Seu certificado não é válido ou foi emitido incorretamente pela CA
1. Os detalhes organizacionais associados ao certificado são alterados e a CA emite um novo certificado
1. Qualquer outro motivo inevitável pelo qual o certificado foi revogado

## Referências

* [Instituto Nacional de Padrões e Tecnologia (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Lista de revogação de certificação](https://en.wikipedia.org/wiki/Certificate_revocation_list)

