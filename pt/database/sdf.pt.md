{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "arquivo sdf", "o que é arquivo sdf", "como abrir um arquivo sdf", "extensão", "arquivo", "formato de arquivo sdf", "tipo de arquivo de banco de dados", "formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo SDF e APIs que podem criar e abrir arquivos SDF.",
  "title" :"SDF - Arquivo de banco de dados compacto do SQL Server",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## O que é um arquivo SDF?
Um arquivo com extensão .sdf contém o banco de dados Microsoft SQL Server Compact (SQL CE), também conhecido como banco de dados relacional compacto; produzidos pela Microsoft para os aplicativos feitos para dispositivos móveis e desktops. Ele suporta sistemas operacionais de 32 e 64 bits e o conteúdo completo do banco de dados está incluído em um único arquivo SDF e pode ocupar mais de 4 GB de espaço em disco. Para fins de segurança, um arquivo .sdf pode ser criptografado com criptografia de 128 bits. O tempo de execução do SQL CE estabelece o acesso multiusuário paralelo ao arquivo .sdf. O arquivo SDF pode ser copiado via **QuickOnce** ou simplesmente pode ser copiado para o destino para implantação do sistema.

## Formato de arquivo SDF
Um arquivo SDF contém um banco de dados que geralmente é chamado de banco de dados relacional compacto. Um arquivo SDF contém todas as informações relacionadas ao banco de dados e o SQL Server Compact é um mecanismo de banco de dados leve e gratuito que é usado para gerenciar os arquivos .sdf. O tamanho do arquivo .sdf não deve exceder o limite de 4 GB de tamanho. Os arquivos SDF não armazenam as informações sobre stored procedures, triggers ou views. Os aplicativos que usam um banco de dados SQL CE não precisam especificar o caminho para um arquivo SDF na cadeia de conexão ADO.NET, em vez disso, ele pode ser mencionado como |DataDirectory|\database_name.sdf, definindo o diretório de dados que está sendo definido no manifesto do assembly para o aplicativo
A convenção de nomenclatura .sdf é opcional e qualquer extensão pode ser usada para salvar o arquivo. A configuração de uma senha para o arquivo de banco de dados é uma etapa opcional. Para compactar ou reparar o banco de dados o arquivo deve ser salvo com a opção do **base de dados compactado/reparado**.

## Referências

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Usando o SQL Server Compact para aplicativos Web ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


