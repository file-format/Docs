{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Arquivo de Relatórios do Microsoft Access",
  "keywords" :[ "mar", "arquivo mar", "formato de arquivo mar", "o que é relatório de acesso", "relatório de acesso", "relatório de acesso microsoft"],
  "description":"Saiba mais sobre o formato de arquivo do Acess Report (MAR) usado pelo software Microsoft Access para criar um atalho ou link para o Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## O que é o Relatório de Acesso (arquivo MAR)? ##
Um arquivo criado pelo Microsoft Access como atalho de seu relatório é salvo com extensão de arquivo .mar. Um **relatório do Microsoft Access** oferece uma maneira de formatar, exibir e resumir as informações no banco de dados do Microsoft Access. Esses relatórios permitem que você formate seus dados em um layout preciso e informativo para visualização na tela ou impressão. O relatório apenas exibe os dados estáticos, o que significa que não podemos alterar os dados nas tabelas ao visualizar o relatório do Access. O relatório exibe os dados mais recentes quando é aberto.

## Formato de arquivo do Microsoft Access Report (MAR)

O formato de arquivo MAR é usado pelo software Microsoft Access para criar um atalho ou link para o Microsoft Access Report que é um objeto de banco de dados que se torna útil quando você precisa apresentar as informações em seu banco de dados para qualquer um dos seguintes usos:

- Exibir um resumo dos dados.
- Arquivos instantâneos dos dados.
- Exibir detalhes sobre registros individuais.
- Criar rótulos.

## Partes do Relatório de Acesso
O design de um relatório do Access é dividido em diferentes seções que podem ser visualizadas no modo Design. A tabela a seguir explica como cada seção funciona e pode ajudá-lo a criar relatórios.
| Seção | Como a seção é exibida quando impressa | Onde a seção pode ser usada |
---------|----|------|
| Cabeçalho do Relatório | No início do relatório. | Use o cabeçalho do relatório para obter informações que normalmente aparecem em uma folha de rosto, como um logotipo, um título ou uma data. Quando você coloca um controle calculado que usa a função de agregação Soma no cabeçalho do relatório, a soma calculada é para todo o relatório. O cabeçalho do relatório é impresso antes do cabeçalho da página. |
| Cabeçalho da página | No topo de cada página. | Use um cabeçalho de página para repetir o título do relatório em todas as páginas. |
| Cabeçalho do Grupo | No início de cada novo grupo de registros. | Use o cabeçalho do grupo para imprimir o nome do grupo. Por exemplo, em um relatório agrupado por produto, use o cabeçalho do grupo para imprimir o nome do produto. Quando você coloca um controle calculado que usa a função agregada Sum no cabeçalho do grupo, a soma é para o grupo atual. Você pode ter várias seções de cabeçalho de grupo em um relatório, dependendo de quantos níveis de agrupamento você adicionou. Para obter mais informações sobre como criar cabeçalhos e rodapés de grupo, consulte a seção Adicionar agrupamento, classificação ou totais. |
| Detalhe | Aparece uma vez para cada linha na fonte de registro. | É aqui que você coloca os controles que compõem o corpo principal do relatório. |
| Rodapé do Grupo | Ao final de cada grupo de registros. | Use um rodapé de grupo para imprimir informações resumidas de um grupo. Você pode ter várias seções de rodapé de grupo em um relatório, dependendo de quantos níveis de agrupamento você adicionou. |
| Rodapé da página | No final de cada página. | Use um rodapé de página para imprimir números de página ou informações por página. |
| Rodapé do Relatório | No final do relatório. Observação: no modo de design, o rodapé do relatório aparece abaixo do rodapé da página. No entanto, em todas as outras visualizações (exibição de layout, por exemplo, ou quando o relatório é impresso ou visualizado), o rodapé do relatório aparece acima do rodapé da página, logo após o último rodapé do grupo ou linha de detalhe na página final. | Use o rodapé do relatório para imprimir os totais do relatório ou outras informações de resumo de todo o relatório. |






## Referências ##

- [Introdução aos relatórios no Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Projetando relatórios no Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

