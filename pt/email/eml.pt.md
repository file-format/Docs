{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Mensagem de e-mail",
  "description":"Saiba mais sobre o formato de arquivo EML e APIs que podem criar e abrir arquivos EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## O que é um arquivo EML?

O formato de arquivo EML representa mensagens de email salvas usando o Outlook e outros aplicativos relevantes. Quase todos os clientes de e-mail suportam esse formato de arquivo por sua conformidade com o padrão de formato de mensagem da Internet RFC-822. O Microsoft Outlook é o software padrão para abrir tipos de mensagens EML. Os arquivos EML podem ser usados para salvar em disco, bem como enviar para destinatários usando protocolos de comunicação.

## Breve História da EML

As especificações de formato de arquivo EML estão disponíveis de acordo com o formato padrão [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). Antes do RFC-822, o RFC-733 governava as regras de troca de mensagens de rede até que em 1982, o primeiro foi criado como uma melhoria ao lateral ao estabelecer padrões ARPA. Ao mesmo tempo, a Microsoft criou seus próprios módulos COM para o desenvolvimento de seu próprio cliente de e-mail, ou seja, Outlook Express. O RFC-822 tomou o caminho para se estabelecer como um formato proprietário quando a Microsoft se desviou do padrão aberto e criou o formato de arquivo [PST](/pt/email/pst/) onde os emails são salvos em um formato de banco de dados altamente estruturado. Isso resultou em problemas para usuários de clientes de e-mail que não são da Microsoft quando os e-mails foram encaminhados do Microsoft Outlook.

Foi em 2001, quando o padrão 822 foi aprimorado para 2822 - Internet Message Format, que está atualmente em uso para criar, ler e enviar mensagens EML no formato MIME RFC-822.

## Especificações de formato de arquivo EML

Os arquivos EML são compostos por duas seções distintas:

* Cabeçalhos - Contém informações sobre o cabeçalho da mensagem
* Corpo da mensagem - Contém uma série de informações que podem incluir o conteúdo da mensagem, imagens incorporadas e anexos

### Informações de cabeçalhos ###

Um arquivo EML consiste em informações de cabeçalhos e, opcionalmente, no corpo da mensagem. Cada linha de cabeçalho no EML tem duas partes separadas por dois pontos ":". O primeiro é chamado de Nome do Cabeçalho e o que segue os dois pontos é o corpo do cabeçalho. Por exemplo, esses cabeçalhos incluem:

* Endereço de e-mail do remetente
* Endereço de e-mail do destinatário
* Assunto do e-mail
* Carimbo de data e hora da mensagem

**Exemplo de cabeçalho**

A partir de:<John@bmw.eml.light.com>

Para:<Andy@fileformat.com>

Data: Qui, 8 de março de 2018 10:43:37 +0100

Assunto: bmw eml light

### Corpo da mensagem ###

O corpo da mensagem EML contém as informações primárias do e-mail na forma de texto, hiperlinks e anexos. O corpo do e-mail pode conter texto legível, mas não é necessário. Nesse caso, o corpo da mensagem pode estar vazio ou conter dados de anexos codificados.

O conteúdo do corpo da mensagem é descrito pelo seu Content-Type que permite que os aplicativos de leitura leiam as informações nos respectivos formatos. Na verdade, representa a natureza e o formato de um documento. A estrutura de um tipo MIME ou tipo de conteúdo é muito simples; consiste em um tipo e um subtipo, duas strings, separadas por um '/'. Nenhum espaço é permitido. O `type` representa a categoria e pode ser do tipo discreto ou de várias partes. O `subtipo` é específico para cada tipo. A lista de tipos, que se enquadram na categoria Content-Type, é longa, mas alguns tipos de conteúdo importantes são os seguintes:


|**Tipo**|**Descrição**|**Exemplo de subtipos**
---|---|---|
|text|Representa o formato que pode ser lido por humanos|text/plain, text/html, text/css, text/javascript
|imagem|Representa imagem de qualquer tipo, exceto vídeos|imagem/bmp, imagem/png, imagem/jpg, imagem/gif
|áudio|Representa qualquer formato de arquivo de áudio|áudio/mdi, áudio/wav
|application|Representa qualquer tipo de dados binários|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Representação do Anexo no Corpo EML ###

O corpo EML contém limites para cada tipo de conteúdo que ele contém. O anexo no corpo da mensagem é identificado por seu Content-Type e Content-Disposition, conforme mostrado no exemplo a seguir:

Tipo de conteúdo: texto/simples; charset#"windows-1252"; name#"apple app store.txt"
Conteúdo-Disposição: anexo; filename#"apple app store.txt"
Codificação de Transferência de Conteúdo: base64
X-Attachment-Id: f_jkhztmd02

Como pode ser visto, o Content-Disposition definido como attachment permite que os aplicativos de leitura obtenham informações do anexo, como o nome do arquivo do anexo e a codificação de transferência. As informações do cabeçalho do anexo são seguidas pelo conteúdo do anexo codificado que deve ser lido.

#### Exemplo de planilha como anexo ####

Tipo de conteúdo: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Conteúdo-Disposição: anexo; filename#"english_spodr.xlsx"
Codificação de Transferência de Conteúdo: base64
X-Attachment-Id: f_jkhztmd43

## Referências

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

