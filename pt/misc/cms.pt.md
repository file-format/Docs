{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo CMS - Arquivo de perfil de serviço do Gerenciador de conexões",
  "description":"Saiba mais sobre o arquivo CMS e as APIs que podem criar e abrir arquivos CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## O que é um arquivo CMS?

Um arquivo CMS é um arquivo de dados que contém informações de perfil usadas pelo Microsoft Windows Connection Manager. Ele permite que usuários remotos se conectem a uma rede usando essas informações de perfil. As informações armazenadas em um arquivo CMS incluem dados sobre o sistema operacional do usuário e as permissões usadas para estabelecer uma conexão entre um usuário remoto e a rede. Os administradores do CMS usam o Kit do Administrador do Gerenciador de Conexões (CMAK) para gerar arquivos do CMS.

## Formato de arquivo CMS - Mais informações

Os arquivos CMS não são encontrados comumente nas máquinas dos usuários. Como eles são usados especificamente para permitir que usuários remotos acessem uma rede, você os encontrará em computadores usados para se conectar a uma rede da empresa ou a algum escritório específico. Na maioria dos casos, ele é usado para se conectar a uma rede organizacional, como Virtual Private Network (VPN), dedicada apenas a uma empresa. Sendo um administrador de rede, você configurará o acesso a tal rede com o Connection Manager para permitir que ele acesse a rede da empresa a partir de um local remoto.

### O que é CMS independente?

Um arquivo de perfil CMS é criado usando o Connection Manager e é empacotado com outros arquivos de configuração antes de ser fornecido ao usuário remoto. Esses arquivos adicionais podem incluir um arquivo CMP e um arquivo INF que são empacotados em um arquivo [EXE](/pt/executável/exe/). Este pacote completo é fornecido ao usuário remoto para conexão à rede.

## Referências

* [Compreendendo e configurando o Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

