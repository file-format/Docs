{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo aba", "formato de arquivo aba", "o que é um arquivo aba", "arquivo", "exemplo aba", "extensão de arquivo aba", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Formato de arquivo CemText",
  "description":"Saiba mais sobre o formato de arquivo ABA e APIs que podem criar e abrir arquivos ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## O que é um arquivo ABA?

Um arquivo com extensão .aba é um formato de arquivo da Australian Bankers Association (ABA) ou [Cemtext](https://www.cemtexaba.com/) usado pelos bancos para transações em lote. É usado pela maioria dos bancos para manutenção de registros financeiros. Também conhecido como arquivo de entrada direta, o formato de arquivo ABA foi adotado pela maioria dos bancos australianos como formato padrão para transações em lote. Ainda não foi reconhecido como formato padrão, apesar de ter sido usado pelo Bank of Queensland, NAB e Westpac. Os arquivos ABA podem ser abertos com qualquer editor de texto, como o Notepad++.


## Formato de arquivo ABA

Um arquivo ABA usa o formato ASCII para armazenar dados para encaminhamento ou carregamento em sistemas bancários. O formato foi mantido simples para facilitar a integração no próprio sistema financeiro das empresas para processar lotes de transações. Por exemplo, em um sistema de folha de pagamento, um lote de transações pode ser carregado para ser processado em uma única ocorrência. As especificações do formato de arquivo ABA estão disponíveis como transcrição completa no site [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) e podem ser consultadas para referência de desenvolvedores .

Um arquivo ABA consiste em várias linhas onde cada linha é conhecida como um `registro`. Existem três registros principais em um arquivo ABA:

* Registro Descritivo
* Registro de detalhes
* Registro Total do Arquivo

### Registro Descritivo

Um 'Registro Descritivo' contém informações como Número de Sequência do Carretel, Nome da Instituição Financeira do Usuário, Nome de Uso do arquivo de fornecimento e outras informações.

### Registro de detalhes

O tipo 'Registro Detalhado' inclui informações como Número do Banco/Estado/Agência, Número da Conta a ser creditada/debitada, Indicador, Código da Transação, Valor e outras informações.

### Registro Total do Arquivo

O tipo "Registro total do arquivo" inclui Tipo de registro 7, Preenchimento de formato BSB, Valor total líquido do arquivo (usuário), Valor total do crédito do arquivo (usuário), Valor total do débito do arquivo (usuário) e outras informações.

### Códigos de transação

Uma lista de códigos de transação válidos é a seguinte. Na maioria das vezes, o código "53 - Pagar" é usado em arquivos ABA. Esses códigos de transação abrangem débitos, créditos e impostos retidos na fonte.

|Código|Descrição da transação|
---|---|
|13|Itens de débito iniciados externamente|
|50|Itens de crédito iniciados externamente, com exceção daqueles com Códigos de Transação|
|51|Interesse de segurança do governo australiano|
|52|Bolsa Família|
|53|Pagar|
|54|Pensão|
|55|Atribuição|
|56|Dividendo|
|57|Debêntures/Juros de Notas|

## Exemplo de arquivo ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referências

* [Cemtext ABA](https://www.cemtexaba.com/)

