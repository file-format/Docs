---
date: 2019-10-11
keywords: json, .json, formato de arquivo json, como abrir arquivos json, notação de objeto javascript, formato de dados json, formato de arquivo .json
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo JSON - O que é um arquivo JSON?
linktitle: JSON
description: "Saiba mais sobre o formato de arquivo JSON e as APIs que podem criar e abrir arquivos JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## O que é um arquivo JSON?

JSON (JavaScript Object Notation) é um formato de arquivo padrão aberto para compartilhamento de dados que usa texto legível para armazenar e transmitir dados. Os arquivos JSON são armazenados com a extensão .json. JSON requer menos formatação e é uma boa alternativa para [XML](/pt/web/xml/). JSON é derivado do JavaScript, mas é um formato de dados independente de linguagem. A geração e análise de JSON é suportada por muitas linguagens de programação modernas. *application/json* é o tipo de mídia usado para JSON.

## Formato de arquivo JSON - Breve histórico

Havia uma necessidade de comunicação em tempo real do servidor para o cliente que levou à criação do JSON. O formato JSON foi especificado pela primeira vez por Douglas Crockford em março de 2001. JSON foi baseado no padrão ECMA-262 3ª Edição—Dezembro de 1999, que é um subconjunto de JavaScript.

A primeira edição do padrão JSON ECMA-404 foi publicada em outubro de 2013 pela Ecma International. A RFC 7159 tornou-se a principal referência para usos de Internet do JSON em 2014. Em novembro de 2017, a ISO/IEC 21778:2017 foi publicada como padrão internacional. O RFC 8259 foi publicado em 13 de dezembro de 2017 pela Internet Engineering Task Force, que é a versão atual do Internet Standard STD 90.

## Estrutura do arquivo JSON

Os dados JSON são gravados em pares **chave/valor**. A chave e o valor são separados por dois pontos (:) no meio, com a chave à esquerda e o valor à direita. Diferentes pares de chave/valor são separados por uma vírgula(,). A chave é uma string cercada por aspas duplas, por exemplo, "nome". Os valores podem ser dos seguintes tipos.

- `Número`
- `String`: Sequência de caracteres Unicode entre aspas duplas.
- `Boolean`: Verdadeiro ou Falso.
- `Array`: Uma lista de valores entre colchetes, por exemplo

``` json
[ "Maçã", "Banana", "Laranja" ]
```

- `Object`: Uma coleção de pares chave/valor cercados por chaves, por exemplo

``` json
{"name": "Jack", "age": 30, "favoriteSport" : "Futebol"}
```

Os objetos JSON também podem ser aninhados para representar a estrutura dos dados. Abaixo está um exemplo de um objeto JSON.

### Exemplo de formato JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Qual é o tamanho máximo do arquivo JSON?

Praticamente não há limite para o tamanho máximo de um arquivo JSON. Pode ser tão longo quanto o espaço requerido pelo conteúdo a ser armazenado.

Quando se trata de usar o formato de arquivo JSON para transferir dados pela internet, é preciso ter cuidado com os recursos disponíveis do computador. Se grandes dados JSON forem transferidos, a transferência será afetada se o navegador do cliente tiver memória limitada.


Não há limite rígido definido por especificação, mas você precisa ter cuidado para não esgotar os recursos nos computadores de seus usuários, pois isso degradará rapidamente a experiência do usuário e eles provavelmente abandonarão seu aplicativo.

## JSON x XML

**XML** é outro formato de arquivo comum e amplamente usado para troca de dados pela Internet. Quando se trata de troca de dados entre aplicativos, os desenvolvedores têm a opção de usar os formatos de arquivo XML e JSON. No entanto, o JSON é adotado como a maneira mais conveniente de troca de dados entre aplicativos pela Internet devido aos seguintes motivos.

1. O JSON oferece uma visão clara e fácil de ler dos dados em comparação com os formatos de arquivo XML
1. JSON reduz a sobrecarga de transferência de dados pela Internet, pois possui menos caracteres para definir o mesmo conjunto de dados em comparação com XML
1. As linguagens de programação modernas fornecem analisadores integrados para analisar a resposta JSON na web.

## Você sabia?

Você pode se tornar um colaborador em FileFormat.com para manter a comunidade de formatos de arquivo atualizada com suas descobertas. Se você precisar compartilhar algo sobre formatos de arquivo JSON ou Web, poderá postar suas descobertas na seção [Notícias sobre formato de arquivo da Web](https://news.fileformat.com/t/Web) para que as pessoas aprendam mais sobre eles.

## Referências

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Uma introdução ao JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

