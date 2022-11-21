{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo mpx", "formato de arquivo mpx", "o que é um arquivo mpx", "arquivo", "exemplo mpx", "extensão de arquivo mpx","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Formato de arquivo do Microsoft Project Exchange",
  "description":"Saiba mais sobre o formato de arquivo MPX e APIs que podem criar e abrir arquivos MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## O que é um arquivo MPX? ##

Um arquivo com extensão .mpx é um formato de arquivo do Microsoft Exchange. Um formato de arquivo MPX foi desenvolvido pelo Microsoft Project (MSP) para facilitar a troca de informações do projeto entre o MSP e outros aplicativos que suportam o formato de arquivo MPX, incluindo Primavera Project Planner, Sciforma e Timerline Precision Estimating. Usando os arquivos MPX, você pode transferir todos os tipos de informações de um projeto para um sistema diferente, como informações detalhadas de atribuição de recursos, informações de calendário ou informações da caixa de diálogo Informações do projeto.

O Microsoft Project 4.0 introduziu suporte para a criação e leitura de formatos de arquivo MPX que continuaram a ser usados no Microsoft Project 98. No entanto, o suporte para a criação de arquivos MPX descontinuou o lançamento do Microsoft Project 2000 e as versões até o Microsoft Project 2010 suportam apenas a leitura MPX. O formato de arquivo MPX não é compatível com versões posteriores ao MSP 2010.

## Formato de arquivo MPX ##

Uma visão geral das especificações do arquivo MPX é fornecida nesta seção. As especificações completas podem ser encontradas nesta [Base de Conhecimento](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artigo e pode ser consultado para detalhes.

### Registros ###

Um Registro do arquivo MPX consiste em informações para o projeto. Existem diferentes tipos de registros onde cada registro tem sua própria ordem. Cada tipo de registro é identificado por seu número de registro. Para um arquivo MPX, é necessário conter o tipo de registro File Creation. Outros tipos de registros não são obrigatórios. A tabela a seguir mostra todos os tipos de registro, seus números de registro e o número de registros que cada tipo pode conter no arquivo MPX. A inclusão do registro no arquivo MPX deve seguir a ordem da tabela, com os comentários inseridos em qualquer lugar.

|Nome do registro|Número do registro|Número máximo de registros
---|---|---|
|Criação de arquivo (obrigatório)|nenhum|1
|Configurações de moeda|10|1
|Configurações padrão|11|1
|Configurações de data e hora|12|1
|Definição do calendário base|20|250
|Horário base do calendário|25| 7 por registro de definição de calendário base
|Exceção do calendário base|26| 250 por registro de definição de calendário base
|Cabeçalho do Projeto|30|1
|Definição de tabela de recursos de texto|140|1- (Ou você pode usar o registro de definição de tabela de recursos numéricos)
|Definição da tabela de recursos numéricos|41|1
|Recurso|50|9.999
|Notas do recurso|51| 1 por registro de recurso
|Definição do calendário de recursos|55| 1 por registro de recurso
|Horas do Calendário de Recursos|56| 7 por calendário de recursos
|Exceção de calendário de recursos| 57|250 por calendário de recursos
|Definição da Tabela de Tarefas de Texto|60|1 (Ou você pode usar o registro Definição da Tabela de Tarefas Numéricas)
|Definição da Tabela Numérica de Tarefas|61|1
|Tarefa|70|9
|Anotações de Tarefa|71| 1 por registro de tarefa
|Tarefa recorrente|72| 1 por registro de tarefa
|Atribuição de recursos|75| 100 por registro de tarefa
|Campos do Grupo de Trabalho de Atribuição|76| 1 por registro de Atribuição
|Nomes de Projeto|80|500
|Links de clientes DDE e OLE|81|500
|Comentários|0|ilimitado

### Estrutura do arquivo ###

Um arquivo MPX consiste nos registros mencionados acima que são organizados de maneira pré-definida dentro do arquivo. Os detalhes sobre esses tipos de registro são discutidos a seguir:

**File Creation Record (FCR):** Este é um registro obrigatório que tem como objetivo identificar:

* Formato de arquivo (MPX)
* Caractere separador de lista usado no arquivo
* Programa e número de versão usados para criar o arquivo
* Número da versão do formato de arquivo MPX usado no arquivo
* Página de código usada para criar o arquivo

Este deve ser o primeiro registro no arquivo. Ao exportar do Microsoft Project, o caractere separador de lista é especificado no item Configurações Regionais no Painel de Controle do Windows. Um registro FCR inclui os seguintes campos:

* MPX seguido imediatamente pelo caractere separador de lista
* Nome/Identificador do Programa
* Número da versão do arquivo
* Página de código (850, 437, MAC, ANSI)

Por exemplo, o registro pode conter informações **MPX, Microsoft Project, 3.0**, que especifica que uma vírgula é usada como o caractere separador de lista nesse arquivo MPX. A versão do formato MPX usada no arquivo é exportada do Microsoft Project versão 3.0.

**Configurações de moeda** Este registro, com o número de registro 10, especifica as configurações para as opções de moeda na caixa de diálogo Opções. Se esse registro não for incluído, as configurações atuais na caixa de diálogo Opções serão usadas. Os separadores de Milhares e Decimais são especificados no item Configurações Regionais no Painel de Controle do Windows.
Os campos incluídos neste registro são:

* Símbolo da moeda
* Posição do símbolo (0 # depois, 1 # antes, 2 # depois com um espaço, 3 # antes com um espaço)
* Dígitos da moeda (0,1,2)
* Separador de milhares
* Separador decimal

**Exemplo:** 10,$,1,2,",",.
Este exemplo especifica que os valores de moeda incluem um cifrão ($) antes deles, que dois dígitos são incluídos após o ponto decimal, que uma vírgula é usada para separar milhares e que um ponto é usado como ponto decimal. Como o caractere separador de lista está incluído no campo Separador de Milhares, o campo é colocado entre aspas.

**Configurações padrão:** Este registro, com o número de registro 11, especifica as configurações para as opções padrão na caixa de diálogo Opções. Se uma duração não for especificada, a Unidade de duração padrão precisa ser definida para cálculos corretos da unidade de duração. Se esse registro não for incluído, as configurações atuais na caixa de diálogo Opções serão usadas.
Os campos incluídos neste registro são:

* Unidades de duração padrão (0 # minutos, 1 # horas, 2 # dias, 3 # semanas)
* Tipo de duração padrão (0 # não fixo, 1 # fixo)
* Unidades de trabalho padrão (0 # minutos, 1 # horas, 2 # dias, 3 # semanas)
* Horas/dia padrão
* Horas/semana padrão
* Taxa Padrão Padrão
* Taxa de horas extras padrão
* Atualizando o Status da Tarefa Atualiza o Status do Recurso (0 # não, 1 # sim)
* Dividir tarefas em andamento (0 # não, 1 # sim)

**Configurações de data e hora:** Este registro, com o número de registro 12, especifica as configurações para as opções de data e hora na caixa de diálogo Opções e a opção Formato de data do texto de barra na caixa de diálogo Layout. Se esse registro não for incluído, as configurações atuais na caixa de diálogo Opções serão usadas.
\\Os campos incluídos neste registro são:

* Ordem de Data (0 # mês/dia/ano, 1 # dia/mês/ano, 2 # ano/mês/dia)
* Formato de hora (0 # 12 horas, 1 # 24 horas)
* Hora padrão (número de minutos após a meia-noite)
* Separador de data
* Separador de tempo
* 0:00 às 11:59 Texto
* 12:00 às 23:59 Texto
* Formato de data (0 -14)*
* Formato de data de texto de barra (0 -194)*

**Definição do Calendário Base:** Esses registros, tendo o registro número 20, definem os calendários base e seus dias úteis e não úteis da semana. As configurações padrão são usadas se não houver entrada para um dia. As configurações padrão são de segunda a sexta-feira para dias úteis e sábado e domingo para dias não úteis. Neste registro, o campo Nome é obrigatório. Para cada um dos dias, uma entrada de 0 indica que o dia não é útil e uma entrada de 1 indica que o dia é um dia útil.
Os campos incluídos neste registro são:

* Nome
* Domingo
* Segunda-feira
* Terça-feira
* Quarta-feira
* Quinta-feira
* Sexta-feira
* Sábado

**Horário base do calendário:** Esses registros, com o número de registro 25, especificam as horas de trabalho para os dias da semana, caso sejam diferentes das configurações padrão. O horário de trabalho padrão é das 8h00 às 12h00 e das 13h00 às 17h00. Cada registro de Horas do Calendário Base refere-se ao registro de Definição do Calendário Base anterior. Até sete desses registros podem seguir cada registro de Definição de Calendário Base.

* Dia da Semana (1 - 7, sendo 1 # domingo e 7 # sábado)
* A partir do tempo 1
* Para o tempo 1
* A partir do tempo 2
* Para o tempo 2
* A partir do tempo 3
* Para o tempo 3

**Exceção de calendário base:** Esses registros, com o número de registro 26, definem as exceções aos dias e horas especificados nos dois tipos de registro anteriores. Até 250 desses registros podem seguir cada registro de Definição de Calendário Base. Esses registros devem ser listados em ordem cronológica. Se uma exceção for de um dia, você pode deixar o campo Até a data vazio. Se nenhum horário for indicado, serão usados os horários padrão de 8h às 12h e de 13h às 17h.
Os campos incluídos neste registro são:

* Da data
* Até a presente data
* Não trabalhando/Trabalhando (0 # não trabalhando, 1 # trabalhando)
* A partir do tempo 1
* Para o tempo 1
* A partir do tempo 2
* Para o tempo 2
* A partir do tempo 3
* Para o tempo 3

**Cabeçalho do projeto:** esse registro, com valor de registro 30, define campos globais do projeto, como a data de início do projeto e a data de término do projeto. Os campos neste registro correspondem às informações nas caixas de diálogo Informações do Projeto e Estatísticas.
Os campos e abas incluídos neste registro são:

* Aba Projeto
* Companhia
* Gerente
* Calendário (padrão usado se não houver entrada)
* Data de início (este campo ou o próximo campo é calculado para um arquivo importado, dependendo da configuração Agendar de)
* Data de término
* Agendar de (0 # início, 1 # fim)
* Data atual*
* Comentários
* Custo
* Custo de linha de base
* Custo real
* Trabalhar
* Trabalho de linha de base
* Trabalho atual
* Trabalhar
* Duração*
*Duração da linha de base*
* Duração real
* Porcentagem concluída
* Início da linha de base
* Acabamento da linha de base
* Início real
* Acabamento real
* Iniciar variação
* Variação de acabamento
* Sujeito
* Autor
* Palavras-chave

**Definição da Tabela de Recursos de Texto**: Este registro lista os campos de recursos, em ordem, que estão sendo importados ou exportados. Para arquivos importados, os nomes devem corresponder aos nomes de campo usados no Microsoft Project. Para arquivos exportados, esse registro vem da tabela Exportação de recursos. Este registro ou o registro de Definição da Tabela de Recursos Numéricos deve ser usado. Ao exportar do Microsoft Project, esses dois registros são incluídos.

**Definição da tabela de recursos numéricos:** usando números em vez de nomes, este registro lista os campos de recursos, em ordem, que estão sendo importados ou exportados. Este é um método alternativo para identificar os campos de recurso incluídos em cada registro de recurso e é útil ao definir um arquivo MPX criado por um produto de idioma estrangeiro.

**Recurso:** esses registros contêm as informações de cada recurso importado ou exportado. Cada registro de recurso descreve um recurso. Quando você importa informações, os campos incluídos são definidos pelo registro Definição da Tabela de Recursos de Texto ou pelo registro Definição da Tabela de Recursos Numéricos. Ao exportar informações, os campos incluídos são os listados na tabela Exportação de recursos.

**Observações do recurso:** esses registros contêm notas sobre o registro do recurso imediatamente anterior. Para uma nova linha dentro da nota, o caractere ASCII 127 é usado. Se a nota incluir o caractere separador de lista, coloque a nota entre aspas.

**Definição do calendário do recurso:** esses registros definem os dias úteis para o recurso especificado no registro do recurso imediatamente anterior. Para arquivos importados, se não houver entrada para o campo Nome do Calendário Base, Padrão será usado. Nenhuma entrada para o dia específico indica que o dia está definido para o padrão (2). Se não houver registros de definição de calendário do recurso, o padrão será usado como o calendário base para o recurso, com o padrão usado para os dias. Para cada um dos dias, uma entrada de 0 indica que o dia não é útil, 1 indica que o dia é um dia útil e 2 especifica que o padrão é usado.

**Horas do calendário do recurso:** esses registros definem as horas de trabalho do recurso que diferem do calendário base usado pelo recurso. Esses registros se aplicam ao registro Definição de Calendário de Recurso imediatamente anterior a esse registro. Até sete desses registros podem seguir cada registro de definição de calendário de recursos.

**Exceção de calendário de recursos:** esses registros definem as exceções aos dias e horas especificados nos dois tipos de registro anteriores. Até 250 desses registros podem seguir cada registro de definição de calendário de recursos. Esses registros devem ser listados em ordem cronológica. Se a exceção for de apenas um dia, você pode deixar o campo Até a data vazio. Se nenhum horário for indicado, serão usados os horários padrão de 8h às 12h e de 13h às 17h.

**Definição da Tabela de Tarefas de Texto:** Este registro lista os campos de tarefas, em ordem, que estão sendo importados ou exportados. Para arquivos importados, os nomes devem corresponder aos nomes de campo usados no Microsoft Project. Se o arquivo estiver sendo exportado, esse registro vem da tabela Exportação de tarefas. Ao exportar do Microsoft Project, esses dois registros são incluídos. Campos que são calculados pelo Microsoft Project, como Início agendado e Término agendado, são ignorados se importados. Se você tiver datas de início ou término de tarefas fixas, use os campos Tipo de Restrição e Data de Restrição.

**Definição da tabela de tarefas numéricas:** usando números em vez de nomes, este registro lista os campos de tarefas, em ordem, que estão sendo importados ou exportados. Este é um método alternativo para identificar os campos de tarefa incluídos em cada registro de tarefa e é útil ao definir um arquivo MPX criado por um produto de idioma estrangeiro.

**Tarefa:** esses registros contêm as informações de cada tarefa que está sendo importada ou exportada. Cada registro de Tarefa descreve uma tarefa. Quando você importa informações, os campos incluídos são definidos pelo registro Text Task Table Definition ou pelo registro Numeric Task Table Definition. Ao exportar informações, os campos incluídos são os listados na tabela Exportar tarefas.

**Anotações de Tarefa:** Esses registros contêm notas sobre o registro de Tarefa imediatamente anterior. Use o caractere ASCII 127 para indicar uma nova linha dentro da nota. Se a nota incluir o caractere separador de lista, coloque a nota entre aspas.

**Atribuição de Recurso**: Esses registros listam informações sobre os recursos atribuídos à tarefa que foi definida no registro de Tarefa anterior. Se você estiver mesclando arquivos e desejar que as informações de atribuição de recursos sejam mantidas, será necessário incluir as informações no arquivo MPX. Se você mesclar, todas as atribuições existentes nas tarefas mescladas serão excluídas. Se você estiver mesclando arquivos com base em IDs exclusivos, os recursos serão atribuídos usando os IDs exclusivos de recurso em vez de IDs.

**Campos de grupo de trabalho de atribuição de recursos:** esses registros listam as informações armazenadas com cada atribuição para os recursos de grupo de trabalho do Microsoft Project 4.0 e 4.1. Se você estiver usando os recursos do Grupo de Trabalho, precisará incluir esse registro para garantir que nenhuma informação seja perdida.

**Nomes de Projetos:** Esses registros listam todos os nomes de links DDE armazenados no projeto.

**Links de cliente DDE e OLE:** Esses registros listam os links DDE no projeto.

**Comentários:** Esses registros podem ser usados para adicionar comentários ao arquivo e podem aparecer em qualquer posição no arquivo. Cada registro de Comentários deve começar com um "0".

## Problemas para abrir um arquivo MPX ##

Aqui está a lista de alguns problemas comuns que podem surgir e causar mau funcionamento do formato MPX:

* Ausência de software de apoio
* Arquivo corrompido
* Arquivo infectado devido a vírus
* Sem direito de acesso no sistema para abrir os arquivos
* Unidade desatualizada em seu sistema
* A extensão do arquivo é renomeada

## Referências ##

* [MPX - Base de Conhecimento da Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

