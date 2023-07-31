{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extensão", "arquivo udl", "formato de arquivo udl", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "o que é um arquivo udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo UDL e APIs que podem criar e abrir arquivos UDL.",
  "title" :"UDL - Arquivo de Link de Dados Universal da Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## O que é um arquivo UDL?
O arquivo com extensão .udl é chamado de arquivo Microsoft Universal Data Link; especificando atributos de conexão; usado por aplicativos do Windows para estabelecer uma conexão com o banco de dados. O arquivo UDL contém a cadeia de conexão para uma fonte de dados OLE DB; com nome de usuário e senha e propriedades essenciais da cadeia de conexão. Para evitar a especificação manual direta das propriedades em uma string de conexão, uma caixa de diálogo Data Link Properties pode ser usada para salvar as informações de conexão em um arquivo .udl como alternativa.

## Formato de arquivo UDL
Basicamente, um arquivo UDL (Universal Data Link) é um arquivo de texto simples que consiste em uma string de conexão de banco de dados com atributos ou propriedades particulares. Depois que o arquivo UDL é criado, ele pode ser testado usando o SQL Server Management Studio para verificar a conectividade.

### Propriedades da cadeia de conexão
As seguintes propriedades podem ser definidas em um UDL para garantir a conectividade adequada:

- **Nome do Servidor**: localização do servidor onde está localizado o banco de dados que você deseja acessar.
- **Opções de autenticação**
- **Autenticação do Windows**: Autenticação para o SQL Server usando as credenciais da conta do Windows do usuário conectado no momento.
- **Autenticação do SQL Server**: Autenticação usando ID de logon e senha.
- **Active Directory - Integrado**: Autenticação integrada com uma identidade Azure Active Directory; também pode ser usado para autenticação do Windows no SQL Server.
- **Active Directory - Senha**: autenticação de ID de usuário e senha com uma identidade do Azure Active Directory.
- **Active Directory - Universal com suporte a MFA**: autenticação interativa com uma identidade do Azure Active Directory.
- **Active Directory - Entidade de Serviço**: Autenticação com uma entidade de serviço do Azure Active Directory.
- **SPN do servidor**: se você usar uma conexão confiável, poderá especificar um nome principal de serviço (SPN) para o servidor.
- **Nome de usuário**: digite a ID de usuário a ser usada para autenticação ao entrar na fonte de dados.
- **Senha**: digite a senha a ser usada para autenticação ao entrar na fonte de dados.
- **Senha em branco**: Quando marcada, permite que o provedor especificado use uma senha em branco na cadeia de conexão.
- **Permitir salvar senha**: Permite que a senha seja salva com a string de conexão.
- **Use criptografia forte para dados**: os dados que passam pela conexão serão criptografados.
- **Certificado do servidor de confiança**: O certificado do servidor será validado.
- **Banco de dados**: Nome do banco de dados que você deseja acessar.
- **Anexar um arquivo de banco de dados como um nome de banco de dados**: Especifica o nome do arquivo principal para um banco de dados anexável.

## Referências ##

* [Componentes de acesso a dados da Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Configuração do Universal Data Link (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

