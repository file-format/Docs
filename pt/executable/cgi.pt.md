{
  "date" : "2021-06-28",
  "keywords" :[ "arquivo cgi", "o que é um arquivo cgi", "arquivo", "exemplo cgi", "extensão de arquivo cgi", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo CGI e APIs que podem criar e abrir arquivos CGI.",
  "title" :"CGI - Arquivo de script de interface de gateway comum",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## O que é um arquivo CGI?
Um arquivo CGI é conhecido como um script Common Gateway Interface que é usado por um servidor da Web para executar um programa externo para processar solicitações de usuários. O script que foi salvo em um arquivo com extensão .cgi é tipicamente escrito em linguagens de programação C ou Perl. O foi introduzido desde os primeiros dias da Web, quando os desenvolvedores da Web queriam conectar bancos de dados a seus servidores Web. Um servidor que suportasse um gateway comum entre o servidor Web e os bancos de dados era adequado para executar o código CGI.

## Formato de arquivo CGI
Os scripts CGI são usados pelo servidor Web para facilitar ao proprietário configurar como uma URL será tratada. O procedimento geralmente é feito marcando um novo diretório (onde os documentos estão localizados principalmente) como contendo scripts CGI; seu nome comumente conhecido é cgi-bin. Por exemplo, /usr/local/apache/htdocs/cgi-bin pode ser escolhido como um diretório CGI no servidor Web. Quando um navegador da Web solicita uma URL que aponta para um arquivo dentro do diretório CGI, em vez de simplesmente enviar esse arquivo (/pt/usr/local/apache/htdocs/cgi-bin/printenv.pl) para o navegador da Web, o HTTP servidor executa o script especificado e retorna a saída do script para o navegador da Web. Em suma, qualquer coisa que o script CGI seja enviado para a saída padrão é transferido para o cliente Web em vez de ser mostrado em um terminal de janela.

### Exemplo CGI

Segue script CGI escrito em Perl que mostra todas as variáveis de ambiente passadas pelo servidor Web:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

A saída será como a seguinte:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Usos de scripts CGI
Os arquivos CGI que contêm os scripts CGI geralmente são usados para processar dados de entrada do usuário e produzir os dados de saída relevantes. A implementação de um wiki é um dos exemplos de programa CGI. Se o agente do usuário enviar uma solicitação para o nome de uma entrada, o servidor Web executará o programa CGI. O programa CGI obtém a fonte da página dessa entrada, converte-a em HTML e imprime o resultado. O servidor Web recebe a saída do programa CGI e a devolve ao agente do usuário. Então, se o agente do usuário chamar a função de edição clicando no botão "Editar página", o programa CGI mostrará uma área de texto HTML ou outro controle de edição com o conteúdo da página. Finalmente, se o agente do usuário clicar no botão "Publicar página", o programa CGI converte o HTML atualizado na fonte da página dessa entrada e a salva.



## Referências

* [Common Gateway Interface - por Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

