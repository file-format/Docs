{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Arquivo de configuração",
  "description":"Saiba mais sobre o formato de arquivo CONFIG com exemplo de CONFIG e APIs que podem criar e abrir arquivos CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo CONFIG?
Um arquivo CONFIG é conhecido como arquivo de configuração; usado para configurar os parâmetros e configurações primárias para vários softwares de computador. Alguns softwares apenas leem seus **arquivos de configuração** na inicialização. Outros verificam os arquivos de configuração para alterações periodicamente.

## Formato do arquivo CONFIG
O **formato de arquivo CONFIG** é usado para processos do servidor, aplicativos de software e configurações do sistema operacional. Um programador pode escrever código para instruir um software a ler os arquivos de configuração repetidamente após um determinado período de tempo e aplicar as alterações ao processo atual. Não há padrões definitivos ou convenções fortes para a sintaxe do arquivo CONFIG. Por exemplo, o arquivo Web.config da Microsoft pertence ao formato de arquivo CONFIG, que consiste em conjuntos de tags baseados em [XML](/web/xml/); pode ser editado com o Microsoft Visual Studio ou qualquer outro editor de texto.

## Exemplos de arquivos de configuração:
Como os arquivos de configuração não são criados seguindo nenhuma regra, padrão ou convenção, esses arquivos podem ter sido gravados usando formatos diferentes. Um arquivo .config pode ser baseado em XML, [JSON](/web/json/) ou qualquer outro formato. A seguir estão os exemplos de arquivos de configuração para sistemas operacionais e softwares conhecidos:

### Arquivos de configuração no Linux
Todo programa Linux é um arquivo executável que mantém a lista de **opcodes** que a CPU executa para realizar operações típicas. As operações de quase todos os programas podem ser personalizadas de acordo com suas necessidades alterando seus arquivos de configuração. Vários arquivos de configuração no sistema Linux estão no diretório /etc. Os arquivos de configuração podem ser classificados nas seguintes categorias:
|Categoria|Exemplo| Comentários|
---|---|---|
|Acessar arquivos|/etc/host.conf|Informa ao servidor de domínio de rede como procurar nomes de host.|
|Inicializando e login/logout|/etc/rc.d/rc.local|Não oficial. Pode ser chamado de rc, rc.sysinit ou /etc/inittab.|
|Sistema de arquivos|/etc/mtools.conf|Configuração para todas as operações (mkdir, copiar, formatar, etc.) em um sistema de arquivos do tipo DOS.|
|Administração do sistema|/etc/shells|Mantém a lista de possíveis “shells” disponíveis para o sistema.|
|Rede|/etc/gated.conf|Configuração para gated. Usado apenas pelo daemon fechado.|
|Comandos do sistema|/etc/logrotate.conf|Configuração para o Dynamic Linker.|
|Daemons|/etc/httpd.conf|O arquivo de configuração para Apache, o servidor Web. Este arquivo normalmente não está em /etc.|
|Programas do usuário| /etc/lynx.cfg| Configurações de proxy|
### Exemplo de arquivo AWS CONFIG
As definições de configuração e credenciais usadas com frequência podem ser salvas em arquivos CONFIG mantidos pela AWS CLI. O arquivo CONFIG deve ser um arquivo de texto simples que usa o seguinte formato:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Exemplo de arquivo SSH CONFIG
O arquivo de configuração do lado do cliente OpenSSH é denominado CONFIG e é armazenado no diretório .ssh. O arquivo SSH CONFIG consiste na seguinte estrutura:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Exemplo de arquivo CONFIG Python
Um arquivo Python CONFIG pode ter esta aparência:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Referências

* [Compreendendo os arquivos de configuração do Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Configurações e configurações do arquivo de credenciais](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Arquivos de configuração em Python](https://martin-thoma.com/configuration-files-in-python/)

