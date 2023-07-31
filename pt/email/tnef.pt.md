{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Saiba mais sobre o formato de arquivo TNEF e APIs que podem criar e abrir arquivos TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo TNEF?

O Transport Neutral Encapsulation Format (TNEF) é um formato proprietário da Microsoft, para encapsular anexos de e-mail com base na Messaging Application Programming Interface (**MAPI**). Microsoft Outlook e Microsoft Exchange Server, suportam totalmente TNEF enquanto mais tarde decodifica TNEF em MAPI e exibe os e-mails formatados. Um anexo de email com codificação TNEF tem um tipo MIME de MS-TNEF e é armazenado como winmail/win.dat. O anexo em winmail .dat encapsula as seguintes informações:


|Mensagem|Objetos OLE|Recursos do Outlook
---|---|---|
|<ul><li> Anexos de mensagens originais</li><li> Versão original formatada</li><li> fontes, tamanhos de texto e cores de texto</li></ul> |<ul><li> fotos incorporadas</li><li> documentos do Office incorporados</li></ul> |<ul><li> formulários personalizados</li><li> botões de votação</li><li> solicitações de reunião</li></ul>


Outros serviços de e-mail que não suportam TNEF apresentam texto simples para mensagens formatadas em TNEF. O Outlook incorpora um formato avançado da mensagem em arquivos TNEF (OLE) ou recursos específicos do Outlook (formulários, botões de sondagem e solicitações de conferência). Não é possível sancionar a codificação TNEF explícita no cliente de e-mail do Outlook, no entanto, optar pelo formato RTF para despachar um e-mail facilita implicitamente a codificação TNEF.

## Formato de arquivo TNEF

O algoritmo de dados TNEF estabelece uma estrutura achatada de propriedades de mensagens hierárquicas ricas. Essas estruturas achatadas são usadas para representar um fluxo de dados serial composto de propriedades específicas.

Em algumas situações, onde as propriedades ocorrem em grupos ou possuem valores múltiplos, o fluxo pode incluir contagens e preenchimentos para impor alinhamentos de dados específicos. Uma situação distinta em que o uso desse algoritmo é vantajoso é em um ambiente de mensagens sem suporte. Nesses ambientes, uma propriedade de mensagem avançada é codificada em um fluxo de dados serial por um gravador TNEF. Além disso, as propriedades que não pertencem ao TNEF subjacente podem ser encapsuladas durante a transmissão. Essas propriedades encapsuladas são então disponibilizadas pela decodificação por meio de um TNEF para garantir a disponibilidade de todas as propriedades da mensagem original para o aplicativo cliente.

No TNEF, todos os tipos de dados numéricos são little-endian e seu tamanho é maior que um byte. A manipulação desses valores numéricos em plataformas não-little-endian requer realizar as transformações apropriadas para obter os valores corretos. Os valores de string são representados no formato Augmented Backus-Naur Form (ABNF) de acordo com as especificações [RFC5234]. Quando a string termina com um caractere nulo, ela também é incluída; por exemplo, "trabalhador@especimen.com" %x00.

{{< figure src="../TNEF.png" alt="Formato de arquivo TNEF" >}}

## Atributos TNEF e regras de processamento ##

O fluxo de dados no TNEF começa com um número de versão herdada, uma assinatura, um valor de chave primitivo e uma página de código de representação de atributo. Esta página de código é gerada quando o codificador registra atributos e propriedades ANSI. Depois disso, o fluxo se tornou uma série de atributos nos quais os atributos de mensagem eram alinhados primeiro e depois seguidos pelos atributos de anexo. Diferentes características de mensagens e anexos estão contidas em atributos especiais como attMsgProps, attAttachment e attRecipTable. Os atributos que aparecem no fluxo TNEF contêm a estrutura, as propriedades da mensagem e as conversões necessárias para envolvê-los com as propriedades da mensagem. Cada atributo consiste em um ID, tamanho e dados do atributo, uma soma de verificação e um nível de acordo com sua aplicação.

## Relação com Protocolos e Outros Algoritmos ##

Os sistemas que têm mecanismo ruim para exibir formato de mensagem rico nativamente precisam do algoritmo de dados TNEF para transporte. Usando o tipo de mídia ms-TNEF, a saída do algoritmo consiste em um arquivo anexo (winmail.dat) e uma parte do corpo do MIME especificado em [RFC2045]. O corpo da mensagem de texto simples é transmitido usando UUENCODE de acordo com a especificação [MSDN-UAF] e este corpo da mensagem ou método equivalente decodificado na extremidade do destinatário. Além disso, o TNEF pode transmitir dados de mensagens usando diferentes protocolos de internet como SMTP, POP3, IMAP4 e os que integram MIME de acordo com o padrão RFC2045.

## Declaração de Aplicabilidade ##

Além da transmissão simples de mensagens, o aplicativo original do TNEF deveria ser criado para usar classes de mensagens e suportar recursos adicionais que não possuem suporte original no protocolo de transporte. Esse aplicativo foi refinado ainda mais para a transmissão de propriedades de mensagens ricas e propriedades nomeadas que os clientes de mensagens modernos usam hoje em dia. Para conformidade com a implementação original, a sintaxe do atributo original é mantida e um atributo especial mantém as novas propriedades da mensagem separadamente.

## Referências

* [Formato de encapsulamento neutro de transporte](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Endereços de e-mail e catálogos de endereços no Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Algoritmo de dados de formato de encapsulamento neutro de transporte (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

