{
  "date" : "2020-03-16",
  "keywords" :[ "Arquivo IFC", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo IFC e APIs que podem criar e abrir arquivos IFC.",
  "title" :"Formato de arquivo IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo IFC?

Arquivos com extensão IFC referem-se ao formato de arquivo Industry Foundation Classes (IFC) que estabelece padrões internacionais para importar e exportar objetos de construção e suas propriedades. Esse formato de arquivo fornece interoperabilidade entre diferentes aplicativos de software. As especificações para este formato de arquivo são desenvolvidas e mantidas pela buildingSMART International como seu padrão de dados. O objetivo final do formato de arquivo IFC é melhorar a comunicação, produtividade, tempo de entrega e qualidade ao longo do ciclo de vida de um edifício.

Devido aos padrões estabelecidos para objetos comuns na construção civil, reduz a perda de informações durante a transmissão de uma aplicação para outra. O IFC pode armazenar dados para geometria, cálculo, quantidades, gerenciamento de instalações, preços etc. para muitas profissões diferentes (arquiteto, elétrico, HVAC, estrutural, terreno etc.).

## Breve história ##

A iniciativa IFC foi tomada em 1994 pela Autodesk para apoiar o desenvolvimento integrado de aplicativos e incluiu empresas como Honeywell, Butler Manufacturing e AT&T. Em 1995, a associação foi aberta para qualquer pessoa e o nome foi alterado para International Alliance for Interoperability. A intenção da organização sem fins lucrativos era publicar a Industry Foundation Class (IFC) como um modelo de produto AEC. Em 2005, o nome foi novamente alterado e agora o buildSMART o mantém.

## Formato de arquivo IFC ##

O formato de arquivo IFC passou por várias mudanças no passado para alcançar as especificações de formato de arquivo v4. Várias pequenas alterações ocorreram de tempos em tempos, bem como as que passaram a fazer parte das especificações como adendos. A seguir está uma lista de diferentes versões de especificações de arquivo que foram tornadas públicas no passado.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (março de 2013) ifcXML2x3 (junho de 2007)
* IFC2x3 (fevereiro de 2006) ifcXML2 para IFC2x2 add1 (RC2)
* Adendo IFC2x2 1 (julho de 2004)ifcXML2 para IFC2x2 (RC1)
* IFC 2x2IFC 2x Adendo 1ifcXML1 para IFC2x e
* Adendo IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

As versões mais recentes das especificações de formato de arquivo IFC estão sempre disponíveis no site buildingSMART e o desenvolvedor deve consultá-las para qualquer tipo de aplicativo que planeja desenvolver. Ao escrever este artigo, as especificações da versão 4 são as mais recentes disponíveis online.

### Formatos de arquivo de dados IFC ###

O formato de arquivo IFF suporta a troca de dados entre aplicativos usando formatos diferentes, conforme listado abaixo:

**IFC:** Este é o formato de troca IFC padrão e usa a estrutura de arquivo físico STEP de acordo com a ISO 10303-21. Este formato de arquivo tem extensão de arquivo .ifc e é o formato IFC mais usado.

**IFC-XML:** É uma versão do formato de arquivo XML do IFC que pode ser gerada diretamente pelo aplicativo de envio conforme a estrutura ISO 10303-28, também chamada de STEP-XML. O formato de arquivo IFC-XML é considerado adequado para interoperabilidade entre ferramentas XML. Em comparação com o formato de arquivo IFC, o IFC-XML é 300-400% maior em tamanho.

**IFC-ZIP:** É uma versão compactada [ZIP](/pt/compression/zip/) do IFC ou IFC-XML onde um desses arquivos está no diretório principal do arquivo zip. Esse formato compacta um arquivo .ifc em 60-80% e um arquivo XML .ifc em 90-95%.

### Arquitetura IFC ###

A especificação IFC inclui termos, conceitos e itens de especificação de dados que se originam do uso em disciplinas, ofícios e profissões do setor da indústria de construção e gerenciamento de instalações. Termos e conceitos usam palavras simples em inglês, os itens de dados dentro da especificação de dados seguem uma convenção de nomenclatura.

os nomes dos itens de dados para tipos, entidades, regras e funções começam com o prefixo "Ifc" e continuam com as palavras em inglês na convenção de nomenclatura CamelCase (sem sublinhado, primeira letra da palavra em maiúscula); os nomes de atributos dentro de uma entidade seguem a convenção de nomenclatura CamelCase sem prefixo; as definições do conjunto de propriedades que fazem parte deste padrão começam com o prefixo "Pset_" e continuam com as palavras em inglês na convenção de nomenclatura CamelCase; as definições de conjuntos de quantidade que fazem parte deste padrão começam com o prefixo "Qto_" e continuam com as palavras em inglês na convenção de nomenclatura CamelCase.

A arquitetura do esquema de dados do IFC define quatro camadas conceituais, cada esquema individual é atribuído a exatamente uma camada conceitual.

**Camada de recursos** — a camada mais baixa inclui todos os esquemas individuais que contêm definições de recursos, essas definições não incluem um identificador globalmente exclusivo e não devem ser usadas independentemente de uma definição declarada em uma camada superior;

**Camada principal** — a próxima camada inclui o esquema do kernel e os esquemas de extensão do núcleo, contendo as definições de entidade mais gerais, todas as entidades definidas na camada principal ou acima carregam um id globalmente exclusivo e, opcionalmente, informações de proprietário e histórico;

**Camada de interoperabilidade** — a próxima camada inclui esquemas contendo definições de entidade que são específicas para uma especialização geral de produto, processo ou recurso usada em várias disciplinas; essas definições são normalmente utilizadas para troca entre domínios e compartilhamento de informações de construção;

**Camada de domínio** — a camada mais alta inclui esquemas contendo definições de entidade que são especializações de produtos, processos ou recursos específicos de uma determinada disciplina. Essas definições são normalmente utilizadas para troca e compartilhamento de informações entre domínios.

## Referências ##

* [Industry Foundation Classes - Por Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

